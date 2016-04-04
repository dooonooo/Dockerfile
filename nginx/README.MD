install nginx-mainline on CentOS
基于 CentOS系统, 编译安装nginx最新版

运行容器时，通过VOLUME 映射 nginx的配置文件，网站的根目录
容器中
nginx配置文件路径为 ｀/usr/local/nginx/conf/nginx.conf｀
网站目录为 ｀/usr/local/nginx/html｀
如
｀docker run -v /Users/dong/tmp/nginx.conf:/usr/local/nginx/conf/nginx.conf -v /Users/dong/tmp2:/usr/local/nginx/html  -p 80:80 -d dooonooo/nginx｀