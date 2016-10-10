# DOL������������
### Description

DOL �ǻ������������������ƽ̨�޹ص� MPSoC ��̻�����

### How to install

1.�����ļ�
```
    sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
    sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip   
```

2.��ѹ�ļ�

```
	$ sudo mkdir dol 
	$ sudo unzip dol_ethz.zip -d dol 
	$ sudo tar -zxvf systemc-2.3.1.tgz
```

3.����systemc

```
    $ cd systemc-2.3.1
    $ mkdir objdir 
    $ cd objdir
    $ ../configure CXX=g++ --disable-async-updates
    $ make install
```

��ͼΪ����configure�Ľ�ͼ

![build settings](https://ooo.0o0.ooo/2016/10/10/57fb7306aee0a.png)

��������ļ�Ŀ¼����($ cd .. $ ls

![2](https://ooo.0o0.ooo/2016/10/10/57fb732c9a10a.jpg)

4.����dol

����ո�dol���ļ���

```
	$ cd ../dol
```

�޸�build_zip.xml�ļ� �ҵ�������λ�,����˵��������systemcλ��������, 

    ��<property name="systemc.inc" value="YYY/include"/>
    ��<property name="systemc.lib" value="YYY/lib-linux/libsystemc.a"/> 

��YYY�ĳ���ҳpwd�Ľ��(ע��,���� 64λ ϵͳ�Ļ���,lib-linuxҪ�ĳ�lib-linux64)
Ȼ���Ǳ���

```
	$ant -f build_zip.xml all
```

�ɹ�����ʾbuild successful
Run example1:

```
$ cd dol/build/bin/main
$ ant -f runexample.xml -Dnumber=1
```

�ɹ������ͼ

![3](https://ooo.0o0.ooo/2016/10/10/57fb734d5b3a7.png)

###Experimental experience
ͨ������������ѧ�����������������dol�������˽���Github�ֿ�Ľ�������markdown���﷨�����˳���ѧϰ���ܷ�����á�
