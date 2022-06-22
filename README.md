# Docker

Learn Docker!

```bash
# clone repository
$ docker run --name repo alpine/git clone https://github.com/docker/getting-started.git
$ docker cp repo:/git/getting-started/ .

# build image
$ cd getting-started
# docker build -t [생성할 이미지 이름]
$ docker build -t docker101tutorial .

# run container
# docker run -d -p [OS-PORT]:[DOCKER-PORT] --name [생성할 컨테이너 이름] [사용할 이미지 이름]
$ docker run -d -p 80:80 --name docker-tutorial docker101tutorial

# share image
# docker tag [업로드할 이미지] [생성할 태그 이름]
$ docker tag docker101tutorial nosf6842/docker101tutorial
# docker push [업로드할 태그 이름]
$ docker push nosf6842/docker101tutorial
```
