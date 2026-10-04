ARG BUILD_ARCH
FROM ghcr.io/home-assistant/${BUILD_ARCH}-base-python:3.13-alpine3.23


RUN python -m venv /opt/venv \
     && /opt/venv/bin/pip install -U --no-cache-dir "cremalink[server] @ https://github.com/dr-duke/cremalink/archive/05518ea2d73ecadbdd7aa5bc7fbf14f99b51fafc.zip"

WORKDIR /opt/cremalink

COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
