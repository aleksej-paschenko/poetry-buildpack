
# About

This repository shows a way to use a custom buildpack and Shipa Cloud to deploy a poetry application.

# How to deploy 

* clone this repo
```shell
git clone https://github.com/aleksej-paschenko/poetry-buildpack.git
```

* create an application
```shell
shipa app create -a my-app --framework shipa-framework --team shipa-team
```

* deploy the application, you need to use your own docker image instead of `image-name`
```shell
cd poetry-buildpack
shipa app deploy -a my-app --build-packs ./poetry-pack,heroku/python poetry-demo/ --image=<image-name> 
```
