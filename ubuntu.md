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