# this file describes how to build tsuru lisp image
# to run it:
# 1 - tsuru-admin platform-add lisp -d https://raw.github.com/tsuru/basebuilder/master/lisp/Dockerfile

from	ubuntu:14.04
RUN     locale-gen en_US.UTF-8
ENV     LANG en_US.UTF-8
ENV     LANGUAGE en_US:UTF-8
ENV     LC_ALL en_US.UTF-8
run	apt-get update
run	apt-get install wget -y --force-yes
run	wget http://github.com/nightshade427/basebuilder/tarball/lisp-update -O basebuilder.tar.gz --no-check-certificate
run	mkdir /var/lib/tsuru
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	cp /var/lib/tsuru/lisp/deploy /var/lib/tsuru
run	cp /var/lib/tsuru/base/start /var/lib/tsuru
run	/var/lib/tsuru/lisp/install
