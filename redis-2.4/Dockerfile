#
# Create a Redis 2.4 Image
# 
# VERSION   0.1
#

from  ubuntu:precise
maintainer  Georg Kunz <kwd@gmx.ch>
run echo 'deb http://archive.ubuntu.com/ubuntu precise main universe' > /etc/apt/sources.list
run apt-get -y update
run apt-get -y install redis-server
expose  6379
cmd ["/usr/bin/redis-server"]
