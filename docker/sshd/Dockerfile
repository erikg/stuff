from debian:bullseye-slim
run apt-get update
run apt-get upgrade -y
run apt-get install -y ssh libpam-google-authenticator
run mkdir -m 700 /run/sshd
run apt-get install -y vim
cmd ["/usr/sbin/sshd", "-D"]
