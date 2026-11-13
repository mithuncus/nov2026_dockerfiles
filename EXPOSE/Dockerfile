FROM almalinux:8
RUN dnf -y install nginx \
 && dnf clean all \
 && rm -rf /var/cache/dnf
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
 && ln -sf /dev/stderr /var/log/nginx/error.log
EXPOSE 80/tcp   
CMD ["nginx", "-g", "daemon off;"]