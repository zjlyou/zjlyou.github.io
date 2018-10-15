---
title: 在github上建立个人博客
tags: 
- github pages
category:
- 其他
---
基本步骤：
1. 安装[Node.js](https://nodejs.org/en/)
安装完后，通过` node -v `查看版本号
2. 安装[Git](https://git-scm.com/downloads)
安装完后，通过` git version `查看版本号
3. 配置[GitHub](https://github.com/)
4. 安装hexo
新建一个文件夹，用作博客目录，在该目录下打开` git bash `，输入如下命令：
安装hexo：` npm install -g hexo `
初始化：` hexo init `
安装依赖包node_modules：` npm install `
安装完后，hexo文件夹如下：
   * node_modules：依赖包
   * public：存放的是生成的页面
   * scaffolds：命令生成文章等的模板
   * source：用命令创建的各种文章
   * themes：主题
   * _config.yml：整个博客的配置
   * package.json：项目所需模块项目的配置信息
5. 站点配置
修改博客配置文件_config.yml及主题配置文件_config.yml
创建分类页：`hexo new page "categories"`
创建标签页：`hexo new page "tags"`
6. 本地查看默认站点
发布文章：`hexo new "博客文章名"` 或 新建md文件到/source/_posts文件夹或其子文件夹下
生成文件：` hexo generate ` 或 ` hexo g `
启动服务：` hexo server ` 或 ` hexo s `
在浏览器输入` localhost:4000 `即可查看
7. 发布，部署到github
` hexo clean && hexo generate && hexo deploy `
8. 在多台电脑上提交和更新github pages博客
在yourname.github.io仓库上新建一个hexo分支，该分支用于保存hexo的源文件（部署环境文件）
clone仓库到本地：` git clone https://github.com/yourname/yourname.github.io `
切换到hexo分支：` git checkout hexo `
将本地博客的部署文件（hexo目录下的全部文件）拷贝到hexo分支目录下
提交hexo分支：` git add . && git commit -m 'hexo' && git push `
需要在另一台电脑操作时，clone yourname.github.io仓库的hexo分支到本地，执行` npm install`重新生成依赖包
至此，本地博客环境就绪
9. git基本操作命令
创建git仓库：` git init `
配置git仓库,创建文件过滤规则文件，并进行规则配置： ` touch .gitignore `
根据过滤规则添加文件到本地仓库：` git add . `
提交：` git commit -m 'Initial commit' `
关联到远端仓库：` git remote add <name> url `
将本地仓库推送到远端仓库：` git push -u <name> master `
10. markdown基本语法
参考链接：[https://www.jianshu.com/p/191d1e21f7ed](https://www.jianshu.com/p/191d1e21f7ed)


参考链接：
[https://www.cnblogs.com/visugar/p/6821777.html](https://www.cnblogs.com/visugar/p/6821777.html)
[https://blog.csdn.net/tianbo_zhang/article/details/79137103](https://blog.csdn.net/tianbo_zhang/article/details/79137103)
[https://www.jianshu.com/p/0b1fccce74e0](https://www.jianshu.com/p/0b1fccce74e0)

