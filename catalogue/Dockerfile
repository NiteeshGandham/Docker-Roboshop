FROM node:20
#This will create and move there
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install
ENV MONGO=true\
    MONGO_URL="mongodb://localhost:27017/catalogue"

