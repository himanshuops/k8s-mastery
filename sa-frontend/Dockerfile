FROM node:alpine as builder
COPY . /sa-frontend
WORKDIR /sa-frontend
RUN npm install
RUN npm run build

FROM nginx:1.15-alpine
COPY --from=builder /sa-frontend/build /usr/share/nginx/html
EXPOSE 80


# FROM nginx
# COPY build /usr/share/nginx/html