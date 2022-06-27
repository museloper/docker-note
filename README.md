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

## centos

```bash
# Setting APM
$ docker pull centos:centos7
$ docker run -it -p 80:80 --name docker_apm centos:centos7
$ yum install httpd

# 아파치 실행
$ sudo systemctl start httpd
bash: sudo: command not found

# sudo 패키지 설치
$ yum install sudo

# 다시 아파치 실행
$ sudo systemctl start httpd
Failed to get D-Bus connection: Operation not permitted # ...ㅂㄷㅂㄷ
```

## ubuntu

```bash
$ docker pull ubuntu:18.04
$ docker run -it -p 80:80 --name docker_apm ubuntu:18.04
$ apt update -y

# 아파치 설치
$ apt install apache2 -y

# 서비스 실행 / 재시작 / 종료
$ service apache2 start # /etc/init.d
$ service apache2 restart
$ service apache2 stop

$ apt install vim -y # 기본적인 편집기도 존재하지 않는다...

# mysql 설치
$ apt install mysql-server -y

# mysql 실행
$ service mysql start

# mysql 보안 스크립트 실행
$ mysql_secure_installation
# 비밀번호 복잡도 체크 여부
# root 비밀번호 설정
# 익명 사용자 삭제 여부
# root 원격 접속 차단 여부
# test db 접속 정보 삭제 여부
# root 비밀번호 및 권한 적용

# php 설치
$ apt install php libapache2-mod-php php-mysql -y
```

## build

```bash
# docker build -t [생성할 이미지 이름] [도커파일 경로]
$ docker build -t docker_ubuntu_apm .
```

## run

```bash
$ docker run --name docker_apm -it -p 80:80 -p 3306:3306 docker_ubuntu_apm
```
