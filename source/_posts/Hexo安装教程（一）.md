---
layout: my
title: Hexo安装教程（一）
date: 2019-04-23 15:49:22
tags: 
	- Hexo
---

> 小编最近一直都在忙于各种杂七杂八的事情，一直都没办法静下心来好好学习，而且每次忙完事情后总是没能来的及将自己的经验进行总结归纳，主要是因为东西过于杂乱，并且每次任务间隔的时间都很短，逐渐消磨了我写博客的意志（看来我和咸鱼已经没有什么区别了）。不过小编近期发现了hexo：一个十分简单就能搭建个人博客的博客框架，在美化自己的博客之余，逐渐也找到了写博客的动力。


# Hexo安装教程（一） -> 小白上手Hexo

> **因为是新手教程，所以这里不对除Hexo以外的内容做过多的说明**

## 1. Hexo安装

### 1.1 Node.js安装

**因为Hexo是基于Node.js的静态博客框架，所以如果电脑没有Node.js的话请务必安装一下**

+ 1.1.1 检查自己电脑是否已经安装好Node.js

  + 打开执行终端，输入命令

    ```shell
    # 查看Node包管理器版本 npm -> node.js package management
    npm -version
    
    # 查看Node.js版本
    node --version
    ```

    如果能正常显示版本号则说明安装成功

    ![EsIQgS.jpg](https://s2.ax1x.com/2019/05/07/EsIQgS.jpg)

    

    

+ 1.1.2 [Node.js官网](https://nodejs.org/zh-cn/download/)

+ 1.1.3 Node.js快速安装方法（目前只适用于Windows和macOS，Linux需要通过源码编译）

  + 从官网下载自己系统的node.js

    ![EsIljg.png](https://s2.ax1x.com/2019/05/07/EsIljg.png)

  + 下载后打开安装包.pkg或.exe一路继续就行（windows保险起见还需要查看一下环境变量）

    Node.js在Windows中默认安装在`C:\Program Files\nodejs\` 中，配置环境变量的话可以加以参考

    ![EsIM38.png](https://s2.ax1x.com/2019/05/07/EsIM38.png)

  + 如果上述方式不行的话可以尝试以下方法(`linux`或者想通过源码直接编译的伙计们也可以参考这篇文章`)

    + [菜鸟教程|Node.js 安装配置](https://www.runoob.com/nodejs/nodejs-install-setup.html)

### 1.2 Hexo项目安装和启动

**Node.js安装好后就可以安装Hexo了，这时候你需要选择一个空文件夹（可以自己创建一个）来保存将来属于你自己的博客**

+ 1.2.1 [Hexo官网](https://hexo.io/)

+ 1.2.2 这里我创建了一个文件夹叫myblog

  ![EgakRI.png](https://s2.ax1x.com/2019/05/09/EgakRI.png)

+ 1.2.3 在终端中cd到你创建的文件夹前一个文件夹中

  ![Egaiid.png](https://s2.ax1x.com/2019/05/09/Egaiid.png)

+ 1.2.4 `首次安装`的时候还需要在终端中输入指令，安装一下Hexo

  ```shell
  #安装Hexo -g代表全局可以访问Hexo
  npm install -g hexo-cli
  
  #如果安装完毕检查一下Hexo是否安装成功
  Hexo -v
  ```

  ![EgaCIH.png](https://s2.ax1x.com/2019/05/09/EgaCIH.png)

+ 1.2.5 在确保Hexo已经安装后，就可以开始安装自己的博客了

  + 先初始化一下自己的Hexo

    ```shell
    #hexo init myblog
    hexo init [你的博客文件夹名称]
    ```

    ![EgUxsK.png](https://s2.ax1x.com/2019/05/09/EgUxsK.png)
    
  + 初始化完后打开博客文件夹，并安装node.js依赖
  
    ![Ega9de.png](https://s2.ax1x.com/2019/05/09/Ega9de.png)
  
    ```shell
    #cd myblog
    cd [你的博客文件夹爱名称]
    
    #安装node依赖
    npm install
    
    #如果觉得安装慢点话可以尝试使用淘宝镜像源 效果和 npm install 一样，会更快
    npm install --registry https://registry.npm.taobao.org
    ```
  
  + 安装好以后打开myblog文件夹可以看见自动生成的文件目录结构  
    
| 文件名称     | 实际作用            |
| ------------ | ------------------- |
| _config.yml  | 博客主题配置文件    |
| node_modules | node.js依赖包文件夹 |
| scaffolds    | 文章模板            |
| source       | 存放你的博客文章    |
| themes       | 博客主题文件夹      |

![EgaAzt.png](https://s2.ax1x.com/2019/05/09/EgaAzt.png)
    
**你新建的博客文章全部放在`source/_posts`文件夹中，格式为Markdown格式**
    

  + 这个时候已经可以在本地运行你的博客了只要输入指令
  
    ```shell
    #生成hexo博客
    hexo g
    #运行hexo博客
    hexo s
    
    #创建新的博客文章名称
    hexo new [你新的博客文章名称]
    ```
  
    
  
    
  ![EgaFJA.png](https://s2.ax1x.com/2019/05/09/EgaFJA.png)
    
  + **启动hexo后打开浏览器，输入`localhost:4000`即可查看你的博客 **
    
  ![EgaVQP.png](https://s2.ax1x.com/2019/05/09/EgaVQP.png)
    
    **如果需要停止输入`ctrl+c`即可**
    
    

### 1.3 git的安装和简单使用

因为hexo要和GitHub结合在一起使用，所以git安装和简单指令的使用是必不可少的

+ 1.3.1 git的安装

  + [git官网](https://git-scm.com/)	
  + [git全平台安装|菜鸟教程](https://www.runoob.com/git/git-install-setup.html)

  + windows安装git：
    + 官网下载完.exe安装包后直接安装即可
  + macos安装git：
    + 打开终端输入git如果没有安装会自行提示你安装git
  + Linux如果不是安装的极简版的话基本上都配有git

+ 1.3.2 git的基本指令

  + [git基本操作|菜鸟教程](https://www.runoob.com/git/git-basic-operations.html)

### 1.4 GitHub账号

+ 1.4.1 [github官网]([https://github.com](https://github.com/))

+ 1.4.2 点开官网选择Sign up注册属于你自己的账号即可

  ![Egg1MQ.png](https://s2.ax1x.com/2019/05/09/Egg1MQ.png)

+ 1.4.3 为了方便以后使用git这里我们把本机的ssh key提交到GitHub仓库上

  + 1.4.3.1 先检查本机是否存在ssh key

    ```shell
    ls -al ~/.ssh
    ```

    如果能显示`id_rsa.pub`则说明ssh key已经存在，如果没有则需要自行创建

    ![Egg8qs.png](https://s2.ax1x.com/2019/05/09/Egg8qs.png)

  + 1.4.3.2 生成ssh key

    + 在终端中输入

      ```shell
      #这里youremail@example.com替换成你的邮箱
      ssh-keygen -t rsa -C  youremail@example.com
      ```

      **输入完后可以一路回车**

    + 获取你本机当前的ssh key

      + 在终端中输入

        ```shell
        cat ~/.ssh/id_rsa.pub
        ```

        **显示的内容为你ssh的公匙**

        ![Egg3rj.png](https://s2.ax1x.com/2019/05/09/Egg3rj.png)

  + 1.4.3.3 将你的ssh key导入到GitHub中

    + 登陆GitHub账号，点击右上角头像->setting

      ![EggMRS.png](https://s2.ax1x.com/2019/05/09/EggMRS.png)

    + 在setting页面中选择SSH and GPG keys->New SSH key

      ![EggJZn.png](https://s2.ax1x.com/2019/05/09/EggJZn.png)

    + 填入对应到title和ssh key内容，点击添加即可

      ![EggKG8.png](https://s2.ax1x.com/2019/05/09/EggKG8.png)
      ![EggQxg.png](https://s2.ax1x.com/2019/05/09/EggQxg.png)

### 1.5 创建Github仓库，存储Hexo博客信息

+ 1.5.1 创建一个新的博客仓库

  + 登陆GitHub账号选择右上角+号->New repository

    ![EgRYCV.png](https://s2.ax1x.com/2019/05/09/EgRYCV.png)

  + 填写好你仓库名称后选择添加仓库即可

    ![EgRt3T.png](https://s2.ax1x.com/2019/05/09/EgRt3T.png)

+ 1.5.2打开刚创建好的仓库，拷贝仓库http链接，下面会用到


  ![EgRNgU.png](https://s2.ax1x.com/2019/05/09/EgRNgU.png)


##  2. 将Hexo的博客发布到Github

### 2.1 配置Hexo配置文件`_config.yml`

+ 2.1.1 打开`_config.yml`

  在配置文件中找到(ctrl+f)：`deploy`将对应段落修改成以下内容

  ```yaml
  # Deployment
  ## Docs: https://hexo.io/docs/deployment.html
  deploy:
    type: git
    repo: 你的github仓库链接
    branch: master
  ```

### 2.2 安装deploy-git

+ 2.2.1 终端中输入

  ```shell
  npm install hexo-deployer-git --save
  ```

  **等待安装完毕后即可将项目部署到GitHub上，只需在终端中输入**

  ```shell
  #hexo g是 hexo generate的缩写，用于生成你写的博客文章
  #hexo d是 hexo deploy的缩写，用于将你的文章部署到GitHub上
  #连起来就是生成你的博客并部署到GitHub上
  hexo d -g
  ```

  **执行完以上指令后打开浏览器访问`你的GitHub账号名+github.io`即可查看你的博客**

  ![EgW3se.png](https://s2.ax1x.com/2019/05/09/EgW3se.png)

  **如果你线下又写了新的博客，只需要执行`hexo d -g  `即可部署到github上**

## 3. 参考文章

+ [文档|Hexo](https://hexo.io/zh-cn/docs/index.html)
+ [廖雪峰git详细教程](https://www.liaoxuefeng.com/wiki/896043488029600)
+ [hexo史上最全搭建教程](https://blog.csdn.net/sinat_37781304/article/details/82729029)

