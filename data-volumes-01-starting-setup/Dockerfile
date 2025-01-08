FROM node

WORKDIR /node-app

COPY package.json .

RUN npm install 

COPY . .

ARG DEFAULT_PORT=80

ENV PORT $DEFAULT_PORT

EXPOSE $PORT

# VOLUME ["/node-app/node_modules"]

CMD [ "npm", "start" ]

# docker run -p 3000:8080 --env-file ./.env --name feedback-app -d -v feedback:/node-app/feedback -v "$(Convert-Path $(pwd)):/node-app:ro" -v /node-app/node_modules -v /node-app/temp  --rm feedback-node