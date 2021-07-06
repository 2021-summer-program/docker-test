# base image 
FROM node 
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY frontend/package.json /usr/src/app

RUN npm install
COPY frontend/ /usr/src/app

EXPOSE 3000
CMD ["npm", "start"]