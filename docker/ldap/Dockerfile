from debian:bullseye-slim
run apt-get update -y
run apt-get upgrade -y
run apt-get autoremove -u
copy selections /root/selections
copy seed.ldif /root/seed.ldif
run debconf-set-selections < /root/selections
run DEBIAN_FRONTEND=noninteractive apt-get install -y tmux vim sudo ldap-utils psmisc netbase libodbc1 libgdbm-compat4 slapd
run slapadd < /root/seed.ldif
cmd ["/usr/sbin/slapd", "-d", "0"]
