## `prepare`

```powershall
# 윈도우 환경
> git clone https://github.com/jjangssem/yes-j.git C:\jjangssem\yes-j
```

<br />

## `build`

```bash
# docker build -t [생성할 이미지 이름] [도커파일 경로]
$ docker build -t docker_ubuntu_apm ./docker_ubuntu_apm
```

<br />

## `run`

```bash
# --name 컨테이너 작명
# -p 포트설정
# -v [로컬 디렉토리 절대경로]:[컨테이너 디렉토리 절대경로]

# 윈도우 환경
$ docker run --name docker_apm -it -p 80:80 -v c:\jjangssem\:/var/www/ docker_ubuntu_apm
```

<br />

## `command`

```bash
# init 쉘 스크립트 실행
$ init
```
