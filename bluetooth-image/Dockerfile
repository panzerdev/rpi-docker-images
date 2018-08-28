FROM arm32v7/debian:stretch-slim

RUN apt-get update && apt-get install -y gpg \ 
	&& echo "deb http://mirrordirector.raspbian.org/raspbian/ stretch main contrib non-free rpi" >>  /etc/apt/sources.list \
	&& echo "deb http://archive.raspberrypi.org/debian/ stretch main ui" >> /etc/apt/sources.list.d/raspi.list \
	&& apt-key adv --keyserver pgp.mit.edu  --recv-key 0x9165938D90FDDD2E \
	&& apt-key adv --keyserver pgp.mit.edu  --recv-key 0x82B129927FA3303E \
	&& apt-get update \
	&& apt-get upgrade -y \
	&& apt-get install -y pi-bluetooth \
	&& apt-get remove -y gnupg \
	&& apt-get autoremove -y  

# docker build -t arm32v7/debian-rpi-bt .
