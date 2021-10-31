FROM node:lts-alpine

USER node
ENV NODE_ENV production

WORKDIR /usr/src/app

COPY --chown=node:node package*.json ./

RUN npm ci --only=production

COPY --chown=node:node . /usr/src/app

EXPOSE 3000

CMD [ "dumb-init", "node", "main.js" ]
