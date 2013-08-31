#
# Create a Redis 2.6 Image
# 
# VERSION   0.1
#

from  ubuntu:precise
maintainer  Georg Kunz <kwd@gmx.ch>
run echo 'deb http://archive.ubuntu.com/ubuntu precise main universe' > /etc/apt/sources.list
run apt-get -y update
run apt-get -y install wget build-essential
run wget -O - http://download.redis.io/releases/redis-2.6.16.tar.gz | tar -C /root -zxv
run cd /root/redis-2.6.16 && make
run /bin/bash -c "cp /root/redis-2.6.16/src/redis-{server,cli,benchmark,check-aof,check-dump} /usr/local/bin/"
expose  6379
cmd ["/usr/local/bin/redis-server"]
