FROM node:20-alpine AS builder

WORKDIR /app

COPY package.json .

COPY *.js .

RUN npm install --omit=dev


FROM node:20-alpine

WORKDIR /app

COPY --from=builder /app /app

ENV MONGO=true \
    MONGO_URL="mongodb://mongodb:27017/catalogue"

CMD ["node", "server.js"]
