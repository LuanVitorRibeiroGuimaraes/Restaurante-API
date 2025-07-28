FROM node:22-alpine

RUN apk add --no-cache python3 g++ make libpq postgresql-client

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 3000

CMD ["sh", "-c", "npm install pg && node app.js"]