FROM python:3.13-trixie

VOLUME /config

ENV LANG C.UTF-8

COPY .. /opt/insteon-mqtt

RUN apt-get update && apt-get install -y git python3-dev && \ 
    pip3 install --break-system-packages /opt/insteon-mqtt && \
    chmod +x /opt/insteon-mqtt/standalone/entrypoint.sh && \
    rm -rf /var/lib/apt/lists/*

CMD ["/opt/insteon-mqtt/standalone/entrypoint.sh" ]
