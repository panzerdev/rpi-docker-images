FROM arm32v7/busybox

ENV VERSION=2.1.0

RUN wget "https://github.com/prometheus/prometheus/releases/download/v2.1.0/prometheus-${VERSION}.linux-armv7.tar.gz" -O /tmp/prom.tar.gz \
	&& cd /tmp \
	&& tar -xvzf prom.tar.gz  \
	&& rm prom.tar.gz  \
	&& mkdir -p /usr/local/prometheus \
	&& mv prometheus-${VERSION}.linux-armv7/* /usr/local/prometheus/

WORKDIR /usr/local/prometheus

ENTRYPOINT ["./prometheus"]
