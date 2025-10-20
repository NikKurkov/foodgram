# build env
FROM node:13.12.0-alpine as build
WORKDIR /app
COPY package*.json ./
RUN npm install --legacy-peer-deps
COPY . ./
RUN npm run build

CMD sh -c "mkdir -p /out && rm -rf /out/* && cp -r /app/build/* /out/"
