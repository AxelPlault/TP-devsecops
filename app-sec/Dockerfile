FROM node:20-alpine
WORKDIR /app
COPY package.json ./
RUN npm install && apk upgrade --no-cache
COPY app.js ./
CMD ["node", "app.js"]
