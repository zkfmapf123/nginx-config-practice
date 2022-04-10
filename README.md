## Nginx 

## Install

```
    brew install nginx (mac)
    brew services restart nginx
```

## 문법검사

```
    nginx -t
```

## config 

### 1. nginx.conf include 설정

```
    find / -name nginx
    sudo vi /usr/local/etc/nginx/nginx.conf

    http {
        ...

        include conf-settings/*;
    }

    pwd (usr/local/etc/nginx)
    mkdir conf-settings

    donggyu.conf 파일을 conf-settings 폴더내에 위치
```

### 2. curl test

```
    curl donggyu.com:82

    # prefix
    curl donggyu.com:82/job
    curl donggyu.com:82/job/a
    curl donggyu.com:82/job/b ...

    # exact
    curl donggyu.com:82/profile
```

### iamge, text 파일 설정

```
    /tmp/public 에 위치 (root 문법)

    curl donggyu.com:82/public/kg.jpeg
    curl donggyu.com:82/public/profile.txt
```