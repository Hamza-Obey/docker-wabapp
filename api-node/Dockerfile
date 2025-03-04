FROM node:18.20.7-alpine 

WORKDIR /usr/src/app

ENV NODE_ENV production

COPY package*.json ./

RUN npm ci --only=production

RUN chown -R node:node /usr/src/app

USER node

COPY ./src .

EXPOSE 3000

CMD ["node","index.js"]
