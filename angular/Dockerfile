FROM node:22-alpine

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci

RUN npm install -g @angular/cli

COPY . .

EXPOSE 4200

CMD ["ng", "serve", "--host", "0.0.0.0"]




# FROM node:22-alpine AS build
# WORKDIR /app

# COPY package.json package-lock.json ./
# RUN npm ci

# RUN npm install -g @angular/cli

# COPY . .
# RUN npm run build -- --configuration=production

# FROM nginx:alpine

# COPY --from=build /app/dist/angular /usr/share/nginx/html

# COPY nginx.conf /etc/nginx/conf.d/default.conf

# EXPOSE 80
