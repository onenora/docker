
## 添加了Stream模块实现SNI分流
>如无必要，勿增实体                      --奥卡姆剃刀原则

docker-compose 文件映射目录
http.conf.d 和stream.conf.d文件夹下放对应的conf即可

```
version: '3'
services:
  nginx:
   container_name: nginx
   image: altriabot/nginx
   restart: always
   network_mode: "host"
   volumes:
     - ./nginx/http.conf.d:/etc/nginx/http.conf.d
     - ./nginx/stream.conf.d:/etc/nginx/stream.conf.d
     - ./nginx/web:/etc/nginx/html
     - ./nginx/logs:/var/log/nginx
     - ./nginx/cert:/etc/nginx/cert
```
- 启动
`docker compose up -d`

## 注意事项

- 基于Docker
- 仅用于学习用途

