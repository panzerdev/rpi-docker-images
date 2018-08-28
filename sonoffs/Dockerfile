FROM arm32v7/debian:stretch-slim

RUN apt-get update \
	&& apt-get install -y ca-certificates

WORKDIR app

COPY sonoffs sonoffs

ENTRYPOINT ["./sonoffs"]
