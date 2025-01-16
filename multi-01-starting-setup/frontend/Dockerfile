FROM node

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

EXPOSE 3000

CMD [ "npm", "start" ]

## docker run --name goals-frontend --rm -d -p 3000:3000 -v \\wsl.localhost\Ubuntu\home\diego\Documents\Courses\docker-kubernetes\multi-01-starting-setup\frontend\src:/app/src goals-react