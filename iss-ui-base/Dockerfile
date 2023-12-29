FROM f7star/nextjs:latest AS deps
LABEL authors="fjw"

WORKDIR /app
COPY iss-ui-base/package.json iss-ui-base/yarn.lock ./
#RUN yarn config set registry 'http://172.16.1.20:8081/repository/ydn-npm-prx/'
RUN yarn install --frozen-lockfile
#RUN proxychains yarn add sharp
RUN yarn add sharp