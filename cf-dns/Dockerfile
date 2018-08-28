FROM arm32v7/debian:stretch-slim

RUN apt-get update \
	&& apt-get install -y ca-certificates

WORKDIR app

COPY cf-dns cf-dns

ENTRYPOINT ["./cf-dns"]
