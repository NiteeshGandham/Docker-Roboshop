FROM node:20 as builder
#This will create and move there
WORKDIR /app
COPY package.json .
COPY *.js .
RUN npm install


FROM node:20
WORKDIR /app
COPY --from=builder /app /app
ENV MONGO=true
ENV MONGO_URL="mongodb://mongodb:27017/catalogue"
ENTRYPOINT ["server.js"]
CMD ["node"] 
