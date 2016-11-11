# Robot operation system
### Description

Robot operation system，一套框架，底层提供硬件驱动，软件层面支持通用的文件格式，我们这次的实验是要安装ROS


### 具体修改的方法
Setup your sources.list
```
    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" >/etc/apt/sources.list.d/ros-latest.list'
```

Set up your keys
```
    sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116
```


安装
```
   sudo apt-get update
   sudo apt-get install ros-jade-desktop-full
```
![build settings](https://ooo.0o0.ooo/2016/11/11/582593c2bb63a.jpg)

初始化
```
    sudo rosdep init
    rosdep update
```
![build settings](https://ooo.0o0.ooo/2016/11/11/582594d35098d.jpg)

环境设置
```
   echo "source /opt/ros/jade/setup.bash" >> ~/.bashrc
   source ~/.bashrc
```
rosinstall
```
   sudo apt-get install python-rosinstall
```

![build settings](https://ooo.0o0.ooo/2016/11/11/58259571dd26b.jpg)



这样，我们就安装好ros了 。
### 实验感想
本次实验只是简单的安装一下ros，并没有什么感想





