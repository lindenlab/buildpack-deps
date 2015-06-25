FROM registry.docker/buildpack-deps:jessie-curl

RUN apt-get update && apt-get install -y --no-install-recommends \
		bzr \
		git \
		mercurial \
		openssh-client \
		subversion \
		adduser \
		iptables \
		init-system-helpers \
		perl \
		libapparmor1 \
		libc6 \
		libdevmapper1.02.1 \
		libsqlite3-0 \
	&& rm -rf /var/lib/apt/lists/*
ADD docker.io_*.deb .
RUN dpkg -i docker.io_*.deb && rm docker.io_*.deb
