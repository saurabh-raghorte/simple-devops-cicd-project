FROM nginx:1.21.6
# RUN rm /etc/nginx/conf.d/default.conf
COPY kubernetes/nginx-nodejs-redis/nginx/nginx.conf /etc/nginx/conf.d/default.conf
# ENTRYPOINT [ "nginx","-g","daemon off" ]
