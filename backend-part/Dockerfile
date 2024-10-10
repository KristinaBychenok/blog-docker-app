FROM node:22-alpine

RUN mkdir -p /home/app/backend

WORKDIR /home/app/backend

COPY ./package.json /home/app/backend/

RUN npm install

COPY . /home/app/backend/

CMD ["node", "app.js"]