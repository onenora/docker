#FROM --platform=$TARGETPLATFORM alpine
FROM python:alpine
ENV TZ=Asia/Shanghai
WORKDIR /pagermaid_pyro
RUN apk add --no-cache gcc libc-dev linux-headers git curl neofetch && \
    git clone -b master https://github.com/TeamPGM/PagerMaid-Pyro.git /pagermaid_pyro && \
    cd /pagermaid_pyro && \
    pip3 install --root-user-action=ignore -r requirements.txt && \
    rm -rf /var/cache/apk/* && \
    apk del --no-network gcc libc-dev linux-headers
CMD ["python3","-m","pagermaid"]