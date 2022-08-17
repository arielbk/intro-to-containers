FROM node:12-stretch

# node user is shipped with the node container for security
USER node

# if the directory doesn't exist it will create it for you
WORKDIR /home/node/code

COPY --chown=node:node index.js index.js

CMD ["node", "index.js"]
