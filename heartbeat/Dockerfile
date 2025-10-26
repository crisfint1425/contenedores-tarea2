FROM elastic/heartbeat:8.14.3
# Copiamos la config desde el host via volumen en docker-compose
USER root
RUN mkdir -p /usr/share/heartbeat/data && chown -R heartbeat:heartbeat /usr/share/heartbeat
USER heartbeat

