FROM nginx

MAINTAINER zero <zhangszi0291@gmail.com>

#替换配置文件
ADD default.conf /etc/nginx/conf.d/default.conf
#添加前端页面到容器内
ADD dist /usr/share/nginx/html/rework
#停用nginx后台运行
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
#暴露80端口
EXPOSE 80

CMD ["/usr/sbin/nginx"]
