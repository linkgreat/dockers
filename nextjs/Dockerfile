FROM node:20-alpine AS base
#RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories
RUN apk update
RUN apk add --no-cache libc6-compat proxychains-ng
RUN echo "Asia/Shanghai" > /etc/timezone
RUN sed -i  '$d;N;$d;N;$d' /etc/proxychains.conf  && echo socks5 172.16.1.10 1080 >> /etc/proxychains.conf
RUN proxychains npm i sharp -g
