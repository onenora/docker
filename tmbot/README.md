> Copy the noreph library Dockerfile, download it yourself if necessary
## 配置

- 需要两个参数：`api_id`、`api_hash`
- 如果没有，点击这个[电报链接](https://my.telegram.org/apps)申请
- 没有Docker环境请一键安装Docker
- `curl -fsSL https://get.docker.com | bash -s docker`
## 启动onebot
```
docker run -it --restart=always --name=tmbot \
-e API_ID=your api_id \
-e API_HASH=your api_hash \
-v ${HOME}/bot/tmbot:/TMBot/data \
altriabot/onebot
```
## 指令说明

- 使用`#pm`查看指令列表

## 注意事项

- 基于Docker
- 仅用于学习用途

