# TeamSpeak3 server over Debian image
FROM debian

ENV TS3_VERSION="3.0.13" TS3SERVER_LICENSE="accept" LANG="C.UTF-8"

COPY config.sh /config.sh
RUN chmod +x /config.sh \
	&& DEBIAN_FRONTEND=noniteractive apt-get -qqy update \
	&& apt-get -qqy install bzip2 curl --no-install-recommends

# Expose TeamSpeak3 used ports
EXPOSE 9987/udp 10011 30033
ENTRYPOINT ["/config.sh"]
