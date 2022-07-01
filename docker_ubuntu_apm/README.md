## Settings

```bash
# $APACHE_HOME/apache2.conf
# 디렉토리 설정
<Directory />
        Options FollowSymLinks
        AllowOverride None
        Require all denied
        LimitRequestBody 2147483647 # 파일 업로드 용량 설정
</Directory>
<Directory /var/www/>
        Options Indexes FollowSymLinks
        AllowOverride None
        Require all granted
</Directory>
# HTML 문서에 PHP 문서를 불러올 수 있도록 설정
AddType application/x-httpd-php .php4 .php .phtml .ph .inc .html .htm

# $APACHE_HOME/sites-available/000-default.conf
DocumentRoot /var/www/html

# $PHP_HOME/apache2/php.ini
## 타임존
date.timezone=Asia/Seoul
## 파일 업로드 사용여부
file_uploads = On
## 업로드 용량 제한 설정
upload_max_filesize = 2048M
post_max_size = 2048M
## php 메모리 사용량
memory_limit = 2048M
## 숏코드 사용
short_open_tag = On
```