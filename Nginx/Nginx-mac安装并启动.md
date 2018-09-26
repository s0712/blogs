# Nginx-mac安装并启动  
Mac安装nginx, 先安装homebrew包管理器
在终端运行
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

```

然后brew install nginx

Mac自带apache服务器  默认占80端口
开启指令 sudo apachectl start
关闭指令 sudo apachectl stop


根据安装nginx成功可以看到
![](Nginx-mac%E5%AE%89%E8%A3%85%E5%B9%B6%E5%90%AF%E5%8A%A8/BA9012EE-D6B0-4754-BCC8-B9449CDC8C8F.png)

docroot  根目录在 /usr/local/var/www    
启动nginx 命令  brew services start nginx
重新启动命令  brew services restart nginx


Nginx常用的命令有

#查看版本，以及配置文件地址
nginx -V
#查看版本 
nginx -v
#指定配置文件
nginx -c filename
#帮助
nginx -h
#重新加载配置|重启|停止|退出 nginx
nginx -s reload|reopen|stop|quit
#打开 nginx
sudo nginx
#测试配置是否有语法错误
sudo nginx -t