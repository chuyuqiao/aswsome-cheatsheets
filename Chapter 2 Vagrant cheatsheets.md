#How To Use Vagrant

----------

#安装 virtualbox 和 vagrant ##
到[virtualbox的下载页面](https://www.virtualbox.org/wiki/Downloads)下载virtualbox进行安装，到[vagrant的下载页面](https://www.vagrantup.com/downloads.html)下载vagrant进行安装。

到终端中，执行

vagrant -v

如果看到输出，表示已经装好了。

##到 vagrantcloud 上找一个 box

更新： vagrantcloud.com 现在已经合并到了[hashicorp](https://atlas.hashicorp.com)。

就找一个干净的 ubuntu14.04 系统就行。使用 [ubuntu/trusty64](https://vagrantcloud.com/ubuntu/boxes/trusty64)。

这个就是我要的64位 ubuntu14.04 系统。到终端里执行

    mkdir vagrant-ubuntu
    
    cd vagrant-ubuntu
    
    vagrant init ubuntu/trusty64

接下来执行

    vagrant up

安装过程就开始了，一般首次运行需要十几分钟时间

#vagrant常用命令

1.重启

vagrant reload

2.关机

vagrant halt

3.销毁虚拟机

vagrant destroy

4.ssh登录虚拟机

vagrant ssh

5.休眠与唤醒

vagrant suspend

vagrant status

vagrant resume


## 安装docker ##
依赖关系：

Ubuntu 14.04版本无需安装额外的依赖包，可以直接安装。
安装步骤：

使用管理员帐号登录ubuntu 14.04系统，保证该管理有root权限，或者可以执行sudo命令。
检查curl包有没有安装。

$ which curl

如果curl没有安装的话，更新apt源之后，安装curl包。

$ sudo apt-get update 
$ sudo apt-get install curl

获得最新的docker安装包。

$ curl -sSL https://get.docker.com/ | sh 

shell会提示你输入sudo的密码，然后开始执行安装过程。
确认Docker是否安装成功。

If you would like to use Docker as a non-root user, you should now consider
adding your user to the "docker" group with something like:

  sudo usermod -aG docker vagrant

Remember that you will have to log out and back in for this to take effect!

$ sudo docker run hello-world

这个命令会下载一个测试用的镜像并启动一个容器运行它。

#docker入门
1.查看版本

docker version

2.搜索镜像

[Docker官方网站专门有一个页面来存储所有可用的镜像](https://hub.docker.com/)

docker search tutorial

3.下载镜像

docker pull learn/tutorial

4.在docker容器中运行hello world!

docker run learn/tutorial echo "hello word"

## 参考文档 ##
[使用 vagrant 安装 ubuntu 系统](http://c.haoduoshipin.com/rails10/)

[vagrant学习笔记 - 基本命令的使用](http://blog.csdn.net/54powerman/article/details/50669807)

[Ubuntu Trusty 14.04 (LTS) 下面安装docker](http://www.docker.org.cn/book/install/install-docker-trusty-14.04-26.html)

[docker入门教程](http://www.docker.org.cn/book/docker/what-is-docker-16.html)

[学习docker](http://blog.csdn.net/liangyihuai/article/details/54743937)

[VirtualBox的网络设置（6种方式）](http://www.cnblogs.com/findumars/p/4982566.html)




