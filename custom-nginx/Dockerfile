FROM nginx

COPY index.html /usr/share/nginx/html
ADD nginx.conf /etc/nginx
EXPOSE 9080

CMD [ "nginx", "-g", "daemon off;" ]