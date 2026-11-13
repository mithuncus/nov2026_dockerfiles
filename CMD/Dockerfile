# FROM almalinux:8
# RUN yum install nginx -y
# CMD ["nginx", "-g", "daemon off;"]
FROM almalinux:8

RUN dnf -y install nginx \
 && dnf clean all \
 && rm -rf /var/cache/dnf

# Send nginx logs to the container's stdout/stderr so `docker logs` shows them
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
 && ln -sf /dev/stderr /var/log/nginx/error.log

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]