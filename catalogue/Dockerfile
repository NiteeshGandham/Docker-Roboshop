FROM node:20 as builder
#This will create and move there
WORKDIR /app
COPY package.json .
COPY *.js .


FROM node:20
WORKDIR /app
COPY --from=builder /app /app
RUN npm install
ENV MONGO=true
ENV MONGO_URL="mongodb://mongodb:27017/catalogue"

CMD ["node", "server.js"]
