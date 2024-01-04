FROM python:3.8.18-slim  AS prepare
LABEL authors="fjw"

WORKDIR /prepare

RUN apt update
RUN apt install telnet iputils-ping iputils-tracepath vim git tzdata ffmpeg proxychains binutils -y
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo "Asia/Shanghai" > /etc/timezone

RUN pip install numpy pyinstaller objdump
RUN pip install opencv-python opencv-python-headless

COPY requirements.txt ./

ENTRYPOINT ["top", "-b"]