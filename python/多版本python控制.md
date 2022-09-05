# 背景

* 在实际使用中，我们可能还想要使用oython2或者python3

* 但是安装好的linux系统通常默认只附带一种python

* 很不巧的是python2和python3是不兼容的

## 更换apt-get源

* 这里用的是ubuntu20.04

* 源文件是/etc/apt/sources.list

* 备份一份，把阿里云和清华源放进去

```
#添加阿里源
deb http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse
#添加清华源
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse
# deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ focal-security main restricted universe multiverse multiverse
```

* 把源换好之后，进行源更新（更新源软件版本表）
  
  ```sudo
  sudo apt-get update
  ```

* 如果出现依赖问题，解决方法如下

```
sudo apt-get -f install
```

* 更新软件（本地软件和源仓库表里面的软件对比版本号，进行升级）

```
sudo apt-get upgrade
```

## 注意点

* ubuntu20.04就想要更换20.04的源仓库地址，不能乱更新，版本号对不上，下载的依赖可能会出问题，（依赖包版本不一样，会找不到相关依赖，服务报错）

* 在Settings里的最后一栏About,最后一栏Software Updates,里面有个Download from,从这里找到中国,然后直接自动测试连接最快的服务器就可以了

## 安装python2

```
apt install python3-pip
```

* 安装完成后我们可以使用如下命令来检查目前可用的 Python 版本：

```
ls /usr/bin/python*
```

可以看到，我可用的 Python 版本有如上几个…

* 设置默认方式(替代版本)

```
sudo update-alternatives --list python
```

若是报错update-alternatives: error: no alternatives for python则说明没有配置默认版本

* 我们设置默认版本

```
sudo update-alternatives --install /usr/bin/python python /usr/bin/python2 1
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 2
```

* 进行切换和xuanz

```
sudo update-alternatives --config python
```

## 安装pip

### python3

* 下载文件进行安装

```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```

apt install python3-pip

### python2

* 下载文件进行安装

```
 https://bootstrap.pypa.io/pip/2.7/get-pip.py
```

### 安装命令

* 就是使用对应版本的python执行对应get-pip.py文件

### pip换源

```
mkdir ~/.pip
sudo gedit ~/.pip/pip.conf
```

* 文件配置

```
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
[install]
trusted-host=mirrors.aliyun.com
```



## 参考

[pip参考链接]([Ubuntu 下安装 pip_搬砖-工人的博客-CSDN博客_ubuntu如何安装pip](https://blog.csdn.net/My_CSDN_IT/article/details/113892209))

[python参考链接]([在 Ubuntu20.04 上安装 python2 并设置为默认方式_搬砖-工人的博客-CSDN博客_ubuntu 安装python2](https://blog.csdn.net/My_CSDN_IT/article/details/114323834))
