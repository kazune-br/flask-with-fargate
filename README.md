### Docker Command
```
$ docker build -t flask-with-fargate:latest .
$ docker run -d -p 80:5000 falsk-with-fargate -n flask-app
$ docker rm -f flask-app
$ docker-compose up --build -d
$ docker-compose down
$ docker-compose run web test.py
```

### Codebuild Local
```
$ docker pull amazon/aws-codebuild-local:latest --disable-content-trust=false
$ git clone https://github.com/aws/aws-codebuild-docker-images.git 
$ cd aws-codebuild-docker-images/ubuntu/python/3.7.1
$ docker build -t aws/codebuild/python:3.7.1 .
$ docker run -it -v /var/run/docker.sock:/var/run/docker.sock \
-e "IMAGE_NAME=aws/codebuild/python:3.7.1" \
-e "ARTIFACTS=/Users/kazune.miyagi/python/flask-with-fargate/artifacts" \
-e "SOURCE=/Users/kazune.miyagi/python/flask-with-fargate" \
amazon/aws-codebuild-local
```
    
    
### REF
- [AWS CodeBuildをローカル環境で動かす](https://techte.co/2018/09/19/aws-codebuild-local/)
- [How to apply CI/CD by using GitHub, CodeBuild, CodePipeline and ECS](https://medium.com/@vankhoa011/how-to-apply-ci-cd-by-using-github-codebuild-codepipeline-and-ecs-58192b8322a9)
- [AWS CodeBuild がローカル環境での実行をサポートしているとのことなので, ざっくりと試してみた](https://inokara.hateblo.jp/entry/2018/05/05/085201)
- 