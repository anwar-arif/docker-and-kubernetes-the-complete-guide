FROM node:16.19.1-alpine as builder

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

RUN npm run build

FROM nginx
COPY --from=builder /app/build /usr/share/nginx/html

# we dont need to set startup command 
# as nginx has its default command to start