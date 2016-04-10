FROM doooonoooob/centos
MAINTAINER doooonooob “doooonoooob@gmai.com"

#安装依赖包
RUN yum -y install pcre-devel zlib-devel unzip gcc make

#下载openssl
RUN cd ~ \
&& curl -O -L https://github.com/openssl/openssl/archive/OpenSSL_1_0_2g.zip \
&& unzip OpenSSL_1_0_2g.zip 

#nginx-ct
RUN curl -L -o nginx-ct.zip https://github.com/grahamedgecombe/nginx-ct/archive/v1.2.0.zip \
&& unzip nginx-ct.zip 

#下载nginx
RUN curl -O http://nginx.org/download/nginx-1.9.14.tar.gz \
&& tar zxf nginx-1.9.14.tar.gz 

RUN cd nginx-1.9.14 \
&& ./configure --add-module=../nginx-ct-1.2.0 --with-openssl=../openssl-OpenSSL_1_0_2g --with-http_v2_module --with-http_ssl_module

EXPOSE 80 443
CMD ["/usr/local/nginx/sbin/nginx"]