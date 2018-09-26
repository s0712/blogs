Nginx 配置http反向代理 (Mac)

反向代理（reverse proxy）方式是指用代理服务器来接受Internet上的连接请求，然后将请求转发给内部网络中的上游服务器，并将从上游服务器上得到的结果返回给Internet上请求连接的客户端，此时代理服务器对外的表现就是一个Web服务器。
这里，我是在本机搭建，通过修改host来模拟多个域名访问本机的nginx


修改/etc/hosts文件,添加域名和域名别名 ,添加如下
> 127.0.0.1 sxy_baidu.com www.sxy_baidu.com  
127.0.0.1 sxy_renren.com www.sxy_renren.com
127.0.0.1 sxy_zhihu.com www.sxy_zhihu.com

然后在/usr/local/etc/nginx/nginx.conf文件http模块中添加如下server监听,注意属性和值用空格或tab间隔 结尾使用分号结束
> server {  
    listen  80;
    server_name  *.sxy_baidu.com sxy_baidu.com;
    location / {
        proxy_pass http://www.baidu.com;
    }
}
server {
    listen 80;
    server_name *.sxy_renren.com sxy_renren.com;
    location / {
        proxy_pass http://www.renren.com;
    }
}
server {
    listen 8088;
    server_name sxy_zhihu.com;
    location / {
        proxy_pass http://www.zhihu.com;
    }
}
Ok 配置好了之后重启  sudo nginx -s reload
接下来在网址中输入  
sxy_baidu.com  
sxy_renren.com 
 www.sxy_zhihu.com:8088
测试,就可以看到跳转到百度 人人和知乎的首页了