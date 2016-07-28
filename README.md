# node-demo





## official node:4 version

```
$ docker build -t node-demo  .
Sending build context to Docker daemon 2.967 MB
Step 1 : FROM node:4-onbuild
# Executing 3 build triggers...
Step 1 : COPY package.json /usr/src/app/
 ---> Using cache
Step 1 : RUN npm install
 ---> Using cache
Step 1 : COPY . /usr/src/app
 ---> a2dea800a7a9
Removing intermediate container 52da3191f1e0
Step 2 : ENV foo bar
 ---> Running in 23fd97847874
 ---> 85911e6b0f59
Removing intermediate container 23fd97847874
Successfully built 85911e6b0f59
$ docker run -ti --rm node-demo
npm info it worked if it ends with ok
npm info using npm@2.15.8
npm info using node@v4.4.7
npm info prestart node-demo@1.0.0
npm info start node-demo@1.0.0

> node-demo@1.0.0 start /usr/src/app
> node index.js;

bar
npm info poststart node-demo@1.0.0
npm info ok 
```





## alpine version

```
$ docker build -t node-demo -f Dockerfile.alpine .
$ $ docker run -ti --rm node-demo
bar
```

