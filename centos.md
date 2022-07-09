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