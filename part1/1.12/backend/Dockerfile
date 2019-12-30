FROM ubuntu:16.04

EXPOSE 8000
ENV FRONT_URL=http://127.0.0.1:5000
WORKDIR /nodejs

RUN apt update && apt install -f -y curl
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
RUN node -v && npm -v

COPY backend-example-docker .
RUN npm install
ENTRYPOINT npm start
