from alpine:latest
run apk update
run apk fetch
run apk add g++ python3 make npm linux-headers
run npm install -g npm@latest
run npm install -g cncjs
run adduser --disabled-password --gecos "" cncjs
user cncjs
cmd /usr/local/bin/cncjs
