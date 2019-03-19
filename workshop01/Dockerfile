# get node env
FROM node:latest

ENV DB_HOST=mydb DB_PORT=3306
ENV DB_USER=root DB_PASSWORD=changeit
ENV APP_DIR=/app APP_PORT=3000

#make the dir, cd into dir
WORKDIR ${APP_DIR}

ADD config config
ADD public public
ADD views views

ADD main.js .
ADD package.json .
ADD package-lock.json .

RUN npm install

EXPOSE ${APP_PORT}

#VOLUME ${APP_DIR}/public
ENTRYPOINT ["node","main.js"]