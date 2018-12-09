# Express安装及生成应用架构
 [https://expressjs.com/zh-cn/](https://expressjs.com/zh-cn/) 

1.基于原有node程序安装 
### $ npm install express —save
### $ npm install express

2.基于express应用生成器 
### 可使用应用程序生成器工具 (### express### ) 快速创建应用程序框架。
### $ npm install express-generator -g
### 例如，以下语句在当前工作目录中创建名为### myapp### 的 Express 应用程序：
$ express —view=pug myapp

   create : myapp
   create : myapp/package.json
   create : myapp/app.js
   create : myapp/public
   create : myapp/public/javascripts
   create : myapp/public/images
   create : myapp/routes
   create : myapp/routes/index.js
   create : myapp/routes/users.js
   create : myapp/public/stylesheets
   create : myapp/public/stylesheets/style.css
   create : myapp/views
   create : myapp/views/index.pug
   create : myapp/views/layout.pug
   create : myapp/views/error.pug
   create : myapp/bin
   create : myapp/bin/www
### 然后安装依赖项：
$ cd myapp
$ npm install
### 然后在浏览器中输入### http://localhost:3000/
[http://localhost:3000/](http://localhost:3000/)
### 以访问此应用程序。
更改端口号在/bin/www文件中. 更新后重启服务 
