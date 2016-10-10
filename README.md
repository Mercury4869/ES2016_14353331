# DOL开发环境配置
### Description

DOL 是基于数据流处理网络的平台无关的 MPSoC 编程环境。

### How to install

1.下载文件
```
    sudo wget http://www.accellera.org/images/downloads/standards/systemc/systemc-2.3.1.tgz
    sudo wget http://www.tik.ee.ethz.ch/~shapes/downloads/dol_ethz.zip   
```

2.解压文件

```
	$ sudo mkdir dol 
	$ sudo unzip dol_ethz.zip -d dol 
	$ sudo tar -zxvf systemc-2.3.1.tgz
```

3.编译systemc

```
    $ cd systemc-2.3.1
    $ mkdir objdir 
    $ cd objdir
    $ ../configure CXX=g++ --disable-async-updates
    $ make install
```

下图为运行configure的截图

![build settings](https://ooo.0o0.ooo/2016/10/10/57fb7306aee0a.png)

编译完后文件目录如下($ cd .. $ ls

![2](https://ooo.0o0.ooo/2016/10/10/57fb732c9a10a.jpg)

4.编译dol

进入刚刚dol的文件夹

```
	$ cd ../dol
```

修改build_zip.xml文件 找到下面这段话,就是说上面编译的systemc位置在哪里, 

    ＃<property name="systemc.inc" value="YYY/include"/>
    ＃<property name="systemc.lib" value="YYY/lib-linux/libsystemc.a"/> 

把YYY改成上页pwd的结果(注意,对于 64位 系统的机器,lib-linux要改成lib-linux64)
然后是编译

```
	$ant -f build_zip.xml all
```

成功会显示build successful
Run example1:

```
$ cd dol/build/bin/main
$ ant -f runexample.xml -Dnumber=1
```

成功结果如图

![3](https://ooo.0o0.ooo/2016/10/10/57fb734d5b3a7.png)

###Experimental experience
通过本次试验我学会了在虚拟机上配置dol环境；了解了Github仓库的建立；对markdown的语法进行了初步学习，很方便好用。
