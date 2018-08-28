FROM arm32v7/debian:stretch-slim 

ENV VERSION=v0.10.11
ENV HOST=/app/certs
ENV CADDYPATH=/app/caddypath

WORKDIR app

RUN 	apt-get update \
	&& apt-get install wget -y \
	&& mkdir tmp \
	&& wget "https://github.com/mholt/caddy/releases/download/${VERSION}/caddy_${VERSION}_linux_arm7.tar.gz" -O tmp/caddy.tar.gz \
	&& tar -xzf tmp/caddy.tar.gz -C tmp \
	&& mv tmp/caddy . \
	&& rm -rf tmp \
	&& apt-get remove -y wget \
	&& apt-get autoremove -y \
	&& apt-get clean

ENTRYPOINT ["./caddy"]
