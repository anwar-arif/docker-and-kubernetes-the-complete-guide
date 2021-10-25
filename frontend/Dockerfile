FROM node:alpine as builder
ENV SRC_DIR=/app
WORKDIR ${SRC_DIR}
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx
COPY --from=builder /app/build /usr/share/nginx/html
