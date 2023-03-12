#FROM --platform=$TARGETPLATFORM python:alpine
FROM python:alpine
ENV TZ=Asia/Shanghai
WORKDIR /TMBot

RUN  \
    build_pkgs="gcc libc-dev linux-headers" \
    && run_pkgs="git" \
    && apk --no-cache add ${run_pkgs} ${build_pkgs} \
    && git clone https://github.com/noreph/TMBot /TMBot \
    && pip install --upgrade pip \
    && pip install --root-user-action=ignore -r requirements.txt \
    && apk del --no-network ${build_pkgs} \
    && rm -rf /var/cache/apk/*

CMD [ "sh", "-c", "/TMBot/__main__.py" ]