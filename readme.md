������Ҫ��һ������ˢ�µ�Ч��,�Ͱٶ�����,д��Ч��.
���ڵĿ��:iscroll,
��ʼ���򵥵�html:
 <div class="wrapper">
   <ul>
   </ul>
</div>
��ʼ��Iscroll:
let myScroll =  new IScroll(".wrapper",{
            probeType: 2,//probeType��1������û��Ӱ�졣�ڹ����¼�������ʱ���������ǲ���æ�������Ķ�����probeType��2��ִ�й�����������ͷ�����������е��¼�����������ԭ����onscroll�¼���probeType��3�����Ĺ����¼��뵽�����ؾ��ȡ�ע�⣬��������requestAnimationFrame������useTransition���٣���  
            scrollbars: true,//�й�����  
            mouseWheel: true,//�����ֹ���  
            fadeScrollbars: false,//����ʱ��ʾ��������Ĭ��Ӱ�أ������ǵ�������Ч��  
            bounce:true,//�߽練��  
            interactiveScrollbars:true,//�����������϶�  
            shrinkScrollbars:'scale',// �������߽�֮��Ĺ���������������������'clip' or 'scale'.  
            click: true ,// �������¼�  
            keyBindings:true,//����ʹ�ð�������  
            momentum:true// �����й��Ի���  
        });
��Ҫע�������: ��ʼ����ʱ�����д��onload �¼�����,��ҳ����ȫ��Ⱦ���ٳ�ʼ��,��Ȼ����ɸ߶ȵļ������.��myScroll.refresh()��ʱ��Ҳ��Ҫ����window.setTimeout .
����ģ��ԭ����Ч��:��Ҫ����ͷ���Ͷ���д��������Ԫ��,text Ϊ�������ظ���....,����ˢ��...����ȡ���Զ�λ�ķ�ʽ,���䴦�ڸ���һ���߶�,���������Ϳ��Կ���,Ȼ������һ���ӵĸ߶�ʱ,�������صĿ鼶Ԫ�س���,�������� "�ɿ���ʼˢ��/����"  �þ��Զ�λ������.�ɿ��ֺ�����Ӧ�߼�����,���ָ���ʼ��css.