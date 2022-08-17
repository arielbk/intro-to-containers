FROM node:12-stretch

RUN npm i -g nodemon

USER node

WORKDIR /home/node/code

# First copy the package and lockfile (check if cache changed)
COPY --chown=node:node package-lock.json package.json ./
RUN npm ci

COPY --chown=node:node . .

RUN npm ci

CMD ["nodemon", "index.js"]