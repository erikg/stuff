from alpine:latest
run apk update
run apk fetch
run apk add libjpeg-turbo libbsd
copy mjpeg-streamer.tar.gz /
run mkdir -p /usr/local
run tar -C /usr/local -vzxf /mjpeg-streamer.tar.gz
#copy ustreamer.bin /usr/bin/ustreamer
#cmd ["/usr/bin/ustreamer", "--host", "0.0.0.0", "--port", "8080"]
cmd ["/usr/local/bin/mjpg_streamer", "-o", "output_http.so", "-i", "input_uvc.so"]
