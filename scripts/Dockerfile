FROM node:16-bullseye-slim
WORKDIR /workspace
COPY ./package.json ./yarn.lock ./
COPY ./srs ./
RUN yarn
COPY ./*.ts ./tsconfig.json ./
RUN yarn build
ENTRYPOINT ["node", "index.js"]
