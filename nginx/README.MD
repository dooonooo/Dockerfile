# nginx-mainline on centos

基于 CentOS系统, 编译安装nginx最新版(1.9.14)


### 设置使用
nginx配置文件路径为 `/usr/local/nginx/conf/nginx.conf`
网站目录为 `/usr/local/nginx/html`

请运行容器时，通过VOLUME 映射 **nginx配置文件** 和 **网站的根目录**

示例：
nginx配置文件为 宿主机上的`~/nginx_conf/nginx.conf`
网站的根目录为 宿主机上的`~/www/html`
`docker run -v ~/nginx_conf/nginx.conf:/usr/local/nginx/conf/nginx.conf -v ~/www/html/:/usr/local/nginx/html/  -p 80:80 -d doooonoooob/nginx`

### 更多
在docker中部署nginx(centos系统)
 <https://blog.doooonoooob.com/post/docker-centos-nginx.html>

🙏感谢 屈屈的文章
 <https://imququ.com/post/my-nginx-conf.html>


