白卷是一个前后端分离的图书管理系统，项目采用 SpringBoot+Vue 开发。  

项目地址：[https://github.com/Antabot/White-Jotter](https://github.com/Antabot/White-Jotter)       

# 前言 

这是一个简单的小项目，旨在熟悉 Java Web 项目开发流程，我会把开发的经验分享给大家，并尽量采用目前较为流行的技术。

由于我经验尚欠，项目中难免有许多不足之处，希望路过的大神们能够帮忙指出。

# 一、整体效果

## 1.首页

作为展示页面，包括开发这个项目的主要参考资料、近期更新和 Slogan

![首页](https://img-blog.csdnimg.cn/20190403215932913.png)

## 2.图书馆

作为核心功能页面之一，提供图书信息展示、图书信息管理两大功能

![图书馆](https://img-blog.csdnimg.cn/20190408220816445.png)

功能实现情况

### 1.图书展示

功能描述 | 实现情况
---|---
基本信息 | 完成
扩充信息 | 未完成

### 2.图书管理

功能描述 | 实现情况
---|---
图书分类 | 未完成
图书上传 | 基本完成
图书维护 | 基本完成

### 3.信息查询

功能描述 | 实现情况
---|---
图书检索 | 基本完成
图书排序 | 未完成

### 4.其它功能

功能描述 | 实现情况
---|---
阅读标注 | 未完成

## 3.笔记本

该页面尚未成型

# 二、技术栈

## 1.前端技术栈

1.Vue  
2.ElementUI  
3.axios   

## 2.后端技术栈

1.SpringBoot  
2.Java Persistence API  
3.MySQL  
  
在开发过程中还会不断用到一些细碎的技术，有必要的我会增添上去

# 三、部署方法

1.clone项目到本地`git clone https://github.com/Antabot/White-Jotter`

2.数据库脚本放在 `wj` 项目的根目录下，在MySQL中执行数据库脚本  

3.数据库配置在 `wj` 项目的 `src\main\resources` 目录下的`application.properties` 文件中，mysql 版本为 5.7.21   

4.在IntelliJ IDEA中运行 `wj` 项目，为了保证项目成功运行，可以右键点击 `pom.xml` 选择 maven -> reimport

至此，服务端就启动成功了，此时在地址栏输入 `http://localhost:8443` 即可访问项目登录页面，默认账号为 `admin`，密码为 `123`

如果要做二次开发，请继续看第五、六步。

5.进入到 `wj-vue` 目录中，在命令行依次输入如下命令：  

```
# 安装依赖
npm install

# 在 localhost:8080 启动项目
npm run dev
```  

由于在 `wj-vue` 项目中已经配置了端口转发，将数据转发到SpringBoot上，因此项目启动之后，在浏览器中输入 `http://localhost:8080` 就可以访问我们的前端项目了，所有的请求通过端口转发将数据传到 SpringBoot 中（注意此时不要关闭 SpringBoot 项目）。

6.最后可以用 `WebStorm` 等工具打开 `wj-vue`项目，继续开发，开发完成后，当项目要上线时，依然进入到 `wj-vue` 目录，然后执行如下命令：  

```
npm run build
```  

该命令执行成功之后， `wj-vue` 目录下生成一个 `dist` 文件夹，将该文件夹中的两个文件 `static` 和 `index.html` 拷贝到 SpringBoot 项目中 `resources/static/` 目录下，然后就可以像第 4 步那样直接访问了。  

# 教程

我在 CSDN 上分享了开发这个项目的教程，有兴趣的小伙伴可以点击下面的链接查看。  

1.[项目简介](https://blog.csdn.net/Neuf_Soleil/article/details/88925013)

2.[使用 CLI 搭建 Vue.js 项目](https://blog.csdn.net/Neuf_Soleil/article/details/88926242)

3.[前后端结合测试（登录页面开发](https://blog.csdn.net/Neuf_Soleil/article/details/88955387)

(持续更新中)

# 近期更新

04-08 完成图书分页功能  
04-06 完成图书查询功能  
04-05 完成图书修改功能  
04-04 完成图书删除功能  
04-03 完成图书新增功能

# 其他资料
