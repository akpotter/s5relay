

����˵����

V0.2
1.ʹ����֧�ֶ�ͻ������ӣ�
2.����Makfile

socks5tran V0.1��

0.������socks5����˺�htran��slave���ܣ����Ľ��������շ�ģ�ͣ�
1.�������g++ socks5tran.cpp -o st -lpthread , stΪ��ִ���ļ�����
2.ִ��st����ʹ��˵����
3.ʾ���� ./st ip1  port1  port2 ,����ip1��port1Ϊ�����ӵ�lcx��IP�Ͷ˿ڣ�port2Ϊ����socks5�����ʹ�õĶ˿ڣ�����Ϊ����δ��ռ�õĶ˿ںţ�
4.��������ʾ��Ȩ�ޣ�����rootȨ��ִ�����
5.socks�û�����������ʱд��Ϊuser= 111111 ,psw= 222222  ��

�������
make
������
make clean

�ɸ�����Ҫ�޸�Makefile�ļ�ͷ�ı���ʵ�ֲ�ͬ�������
Makefile�޸Ĳ���˵����
DEBUG=1  ����ʱ������Բ���
DEBUG=0  ����ʱ��������Բ����ҳ�����O2�����Ż�
STATIC=1 �����Ծ�̬��ʽ����
STATIC=0 ��Ĭ�϶�̬��ʽ����

����STATIC��ʽ���룬���о��棬���Ƽ�ʹ�á�
���棺
warning: Using 'XXXXXX' in statically linked applications requires at runtime the shared libraries from the glibc version used for linking
ԭ��
1.glibc��Щ��̬��Ĵ��ڱ����Ŀ�ľ���Ϊ��������һ̨�����ϱ���õĿ��ܹ��ȽϷ�����Ƶ�����Ļ����ϣ���̬������������������ƫ����ԣ�
2.�������Ͼ���ԭ�������������̵�һЩ�ӿڻ�����Ҫ��̬���֧�ֲſ������У����glibc�ĺ������������������⣻
3.��һЩ���������߲��Ѻã���valgrind�ڴ�й¶��⹤�ߣ�
4.Ӱ��ĳЩ������ܡ�


����ת�����̣�

real server  <-->  socks server  <--> tran(slave) <--> tran(listen) <--> socks client


