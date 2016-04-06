# nginx-mainline on centos


基于 CentOS系统, 编译安装nginx最新版(1.9.13)

### 设置使用
nginx配置文件路径为 `/usr/local/nginx/conf/nginx.conf`
网站目录为 `/usr/local/nginx/html`

请运行容器时，通过VOLUME 映射 nginx的 **配置文件** 和 **网站的根目录**

示例：
`docker run -v /conf/nginx.conf:/usr/local/nginx/conf/nginx.conf -v /www/:/usr/local/nginx/html  -p 80:80 -d dooonooo/nginx`

