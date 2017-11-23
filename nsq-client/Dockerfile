FROM node:8.6.0-alpine

# RUN apk --update add tzdata \
#     && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
#     && echo "Asia/Shanghai" > /etc/timezone \
#     && apk del tzdata

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# add npm package
COPY package.json /usr/src/app/package.json
RUN npm i --registry=https://registry.npm.taobao.org

# copy code
COPY . /usr/src/app

CMD npm start