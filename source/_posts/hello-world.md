---
title: 记录产生伟大
---
## hexo 搭建
  Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## 第一章 天才的陨落

### 关于我第一次用hexo搭建博客，并部署在github pages的一些体会

首先，本人是通过B站up*CodeSheep*于2019年发布的视频[[https://b23.tv/qsXGm8E]]开始入手搭建的，虽然时间久远，但操作大致没有变化，如果你是零基础且想要学习搭建个人博客，我觉得他的视频是值得一看的。话不多说，让我们先看一下他的操作步骤，之后再与我的进行对比，从而看出一些新手易犯的错误：  
 #安装Nodejs
node -v	#查看node版本
npm -v	#查看npm版本
npm install -g cnpm --registry=http://registry.npm.taobao.org	#安装淘宝的cnpm 管理器
cnpm -v	#查看cnpm版本
cnpm install -g hexo-cli    #安装hexo框架
hexo -v	#查看hexo版本
mkdir blog	#创建blog目录
cd blog	 #进入blog目录
sudo hexo init 	#生成博客 初始化博客
hexo s	#启动本地博客服务
http://localhost:4000/	#本地访问地址
hexo n "我的第一篇文章" #创建新的文章 
#返回blog目录
hexo clean #清理
hexo g #生成
#Github创建一个新的仓库 [[YourGithubName.github.io]]  
 cnpm install --save hexo-deployer-git #在blog目录下安装git部署插件   
 配置_config.yml  
-----
	# Deployment
	## Docs: https://hexo.io/docs/deployment.html
	deploy:
  		type: git
 		repo: https://github.com/YourGithubName/YourGithubName.github.io.git
  		branch: master
-----
hexo d	#部署到Github仓库里
https://YourGithubName.github.io/  #访问这个地址可以查看博客

 git clone https://github.com/litten/hexo-theme-yilia.git themes/yilia  #下载yilia主题到本地

#修改hexo根目录下的 _config.yml 文件 ： theme: yilia

hexo c	#清理一下
hexo g	#生成
hexo d	#部署到远程Github仓库
https://YourGithubName.github.io/  #查看博客


More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)
