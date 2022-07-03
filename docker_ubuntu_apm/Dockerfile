# docker_ubuntu_apm

FROM ubuntu:18.04

ENV TZ=Asia/Seoul

RUN apt update -y
RUN apt install git -y
RUN apt install apache2 -y
RUN apt install mysql-server -y
RUN apt install vim -y
RUN apt install net-tools -y

# 심볼릭 링크
# ln -sf [원본 파일명] [심볼릭 링크 파일명]
# -s: 심볼릭 링크파일 생성
# -f: 대상파일이 존재할 경우에 대상파일을 지우고 링크파일 생성
RUN ln -sf /usr/share/zoneinfo/$TZ /etc/localtime 

# php를 설치할 때 timezone에 대한 질문을 하기 때문에 위와 같이 timezone 설정을 선행한 후에 설치
RUN apt install php libapache2-mod-php php-mysql -y
RUN apt install expect -y
RUN mkdir /root/src

COPY index.php /var/www/html
COPY ./config/000-default.conf /etc/apache2/sites-available/
COPY ./config/apache2.conf /etc/apache2/
COPY ./config/php.ini /etc/php/7.2/apache2/
COPY ./config/mysqld.cnf /etc/mysql/mysql.conf.d/
COPY ./config/init /root/src/