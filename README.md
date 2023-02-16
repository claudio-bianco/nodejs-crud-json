npm -y init

npm i express@4.17.1

npm install morgan

node index.js

(POST)
http://localhost:3000/user/add

{
    "username":"admin",
    "password":"mypass",
    "fullname":"Administrator",
    "age":33
}

(GET)
http://localhost:3000/user/list

(PATCH)
http://localhost:3000/user/update/:username

(DELETE)
http://localhost:3000/user/delete/:username






docker build -t claudiobianco/nodejs-crud:latest .

docker run -d -p 3000:3000 --name nodejs-crud claudiobianco/nodejs-crud:latest

docker exec -it nodejs-crud /bin/bash

docker push claudiobianco/nodejs-crud:latest

docker logs nodejs-crud




docker build -t claudiobianco/alpine-git .

docker tag claudiobianco/alpine-git claudiobianco/labs-git:v1.0

docker run -d -p 8080:8080 --name my-labs-git claudiobianco/labs-git:v1.0

docker run -itd claudiobianco/labs-git:v1.0 /bin/sh

docker attach e117c2f78177

git --version

docker push claudiobianco/labs-git:v1.0




docker build -t claudiobianco/alpine-git .

docker run -d -p 8080:8080 --name my-labs-git claudiobianco/labs-git:v1.0

docker exec -it <container id> /bin/bash