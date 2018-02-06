近期需要做一个上拉刷新的效果,就百度了下,写了效果.
基于的框架:iscroll,
初始化简单的html:
 <div class="wrapper">
   <ul>
   </ul>
</div>
初始化Iscroll:
let myScroll =  new IScroll(".wrapper",{
            probeType: 2,//probeType：1对性能没有影响。在滚动事件被触发时，滚动轴是不是忙着做它的东西。probeType：2总执行滚动，除了势头，反弹过程中的事件。这类似于原生的onscroll事件。probeType：3发出的滚动事件与到的像素精度。注意，滚动被迫requestAnimationFrame（即：useTransition：假）。  
            scrollbars: true,//有滚动条  
            mouseWheel: true,//允许滑轮滚动  
            fadeScrollbars: false,//滚动时显示滚动条，默认影藏，并且是淡出淡入效果  
            bounce:true,//边界反弹  
            interactiveScrollbars:true,//滚动条可以拖动  
            shrinkScrollbars:'scale',// 当滚动边界之外的滚动条是由少量的收缩。'clip' or 'scale'.  
            click: true ,// 允许点击事件  
            keyBindings:true,//允许使用按键控制  
            momentum:true// 允许有惯性滑动  
        });
需要注意的事项: 初始化的时候最好写在onload 事件里面,等页面完全渲染了再初始化,不然会造成高度的计算错误.在myScroll.refresh()的时候也需要利用window.setTimeout .
做出模拟原生的效果:主要是在头部和顶部写了两个块元素,text 为上拉加载更多....,下拉刷新...并采取绝对定位的方式,让其处于负的一个高度,正常拉动就可以看到,然后当拉到一格子的高度时,就让隐藏的块级元素出现,文字内容 "松开开始刷新/加载"  让绝对定位的隐藏.松开手后做相应逻辑处理,并恢复初始的css.