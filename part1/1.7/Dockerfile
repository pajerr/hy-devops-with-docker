FROM ubuntu:16.04 
RUN apt-get update && apt-get install -y curl
WORKDIR /tmp 
COPY script.sh . 
CMD ["/tmp/script.sh"]

