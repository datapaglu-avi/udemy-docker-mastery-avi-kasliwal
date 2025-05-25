# use this empty Dockerfile to build your assignment
FROM node:24-alpine3.20

EXPOSE 3000

RUN apk add --no-cache tini

WORKDIR /usr/src/app

COPY package.json package.json

RUN npm install \
    && npm cache clean --force

COPY . .

CMD ["/sbin/tini", "--", "node", "./bin/www"]


# docker image build -t datapaglu-avi/node:assignment_solve .
# docker container run -d -p 80:3000 --name node_assignment_1 datapaglu-avi/node:assignment_solve
# docker image tag datapaglu-avi/node:assignment_solve datapagluavi/node:assignment_solve
# docker container run -d -p 80:3000 --rm --name node_assignment datapagluavi/node:assignment_solve