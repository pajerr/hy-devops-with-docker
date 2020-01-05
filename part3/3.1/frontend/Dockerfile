FROM ubuntu:16.04

EXPOSE 5000
ENV API_URL=http://127.0.0.1:8000

WORKDIR /nodejs

RUN apt-get update && apt-get install -f -y \
    curl nodejs && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    rm -rf /var/lib/apt/lists/* 

RUN node -v && npm -v
COPY frontend-example-docker .
RUN npm install

ENTRYPOINT npm start
