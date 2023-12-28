FROM golang:1.21.5 AS go-dev

#RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.ustc.edu.cn/g' /etc/apk/repositories
#RUN sed -i 's/deb.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list.d/debian.sources
RUN apt update
RUN apt install telnet iputils-ping iputils-tracepath vim git tzdata ffmpeg -y
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo "Asia/Shanghai" > /etc/timezone
RUN go install github.com/swaggo/swag/cmd/swag@latest


