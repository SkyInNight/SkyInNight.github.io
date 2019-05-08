---
layout: my
title: Hexo安装教程（一）
date: 2019-04-23 15:49:22
tags: 
	- Hexo
---

> 小编最近一直都在忙于各种杂七杂八的事情，一直都没办法静下心来好好学习，而且每次忙完事情后总是没能来的及将自己的经验进行总结归纳，主要是因为东西过于杂乱，并且每次任务间隔的时间都很短，逐渐消磨了我写博客的意志（看来我和咸鱼已经没有什么区别了）。不过小编近期发现了hexo：一个十分简单就能搭建个人博客的博客框架，在美化自己的博客之余，逐渐也找到了写博客的动力。



# Hexo安装教程（一） -> 小白上手Hexo

## 1. Hexo安装

### 1.1 Node.js安装

**因为Hexo是基于Node.js的静态博客框架，所以如果电脑没有Node.js的话请务必安装一下**

+ 检查自己电脑是否已经安装好Node.js

  + 打开执行终端，输入命令

    ```shell
    # 查看Node包管理器版本 npm -> node.js package management
    npm -version
    
    # 查看Node.js版本
    node --version
    ```

    如果能正常显示版本号则说明安装成功

    ![EsIQgS.jpg](https://s2.ax1x.com/2019/05/07/EsIQgS.jpg)

    

    

+ [Node.js官网](https://nodejs.org/zh-cn/download/)

+ Node.js快速安装方法（目前只适用于Windows和macOS，Linux需要通过源码编译）

  + 从官网下载自己系统的node.js

    ![EsIljg.png](https://s2.ax1x.com/2019/05/07/EsIljg.png)

  + 下载后打开安装包.pkg或.exe一路继续就行（windows保险起见还需要查看一下环境变量）

    Node.js在Windows中默认安装在`C:\Program Files\nodejs\` 中，配置环境变量的话可以加以参考

    ![EsIM38.png](https://s2.ax1x.com/2019/05/07/EsIM38.png)

  + 如果上述方式不行的话可以尝试以下方法(`linux`或者想通过源码直接编译的伙计们也可以参考这篇文章`)

    + [菜鸟教程|Node.js 安装配置](https://www.runoob.com/nodejs/nodejs-install-setup.html)

### 1.2 Hexo项目安装和启动

**Node.js安装好后就可以安装Hexo了，这时候你需要选择一个空文件夹（可以自己创建一个）来保存将来属于你自己的博客**

+ [Hexo官网](https://hexo.io/)

+ 这里我创建了一个文件夹叫myblog

+ 在终端中cd到你创建的文件夹前一个文件夹中

+ `首次安装`的时候还需要在终端中输入指令，安装一下Hexo

  ```shell
  #安装Hexo -g代表全局可以访问Hexo
  npm install -g hexo-cli
  
  #如果安装完毕检查一下Hexo是否安装成功
  Hexo -v
  ```

+ 在确保Hexo已经安装后，就可以开始安装自己的博客了

  + 先初始化一下自己的Hexo

    ```shell
    # 这里myblog为我创建的文件夹名称
    hexo init [你的博客文件夹名称]
    ```

    

### 1.3 git的安装和简单使用

`因为`



### GitHub账号注册

##  2. 将Hexo的博客发布到Github

##  3. 

