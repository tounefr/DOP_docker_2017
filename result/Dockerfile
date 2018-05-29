FROM node:9.11.1

RUN mkdir /app
COPY . /app
WORKDIR /app
RUN npm install --save /app
EXPOSE 80
CMD node server.js
