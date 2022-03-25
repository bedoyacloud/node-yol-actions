FROM node:12-alpine
RUN mkdir  -p /home/node/app/node_modules && chown -R node /home/node/app
WORKDIR /home/node/app
COPY app/package.json ./
USER node
RUN npm install
COPY --chown=node:node app/ .
EXPOSE port 8080
CMD ["node", "app.js"]