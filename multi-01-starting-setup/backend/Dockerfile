FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 80

ENV MONGODB_USERNAME=root
ENV MONGODB_PASSWORD=secret

CMD [ "npm", "start" ]

## docker run --name mongodb --network goals-net --rm -d -v data:/data/db -e MONGO_INITDB_ROOT_USERNAME=diego-admin -e MONGO_INITDB_ROOT_PASSWORD=secret mongo                             
## docker run --name goals-backend --rm -d --network goals-net -p 80:80 -v logs:/app/logs -v \\wsl.localhost\Ubuntu\home\diego\Documents\Courses\docker-kubernetes\multi-01-starting-setup\backend:/app -v /app/node_modules -e MONGODB_USERNAME=diego-admin goals-node
