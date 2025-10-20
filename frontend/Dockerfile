# build env
FROM node:16-alpine AS build

WORKDIR /app

COPY package.json package-lock.json ./
COPY package-lock.json package-lock.json

RUN npm install --legacy-peer-deps

COPY . .
RUN npm run build

# CMD sh -c "mkdir -p /out && rm -rf /out/* && cp -r /app/build/* /out/"
