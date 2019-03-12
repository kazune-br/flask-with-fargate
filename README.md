### Command
```
$ docker build -t flask-with-fargate:latest .
$ docker run -d -p 80:5000 falsk-with-fargate -n flask-app

Codebuild Local
$ git clone https://github.com/aws/aws-codebuild-docker-images.git 
$ cd aws-codebuild-docker-images/ubuntu/python/3.7.1
$ docker build -t aws/codebuild/python:3.7.1 .
```