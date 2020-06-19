FROM azul/zulu-openjdk:13

RUN groupadd -g 322 lavalink && \
  useradd -r -u 322 -g lavalink lavalink

USER lavalink

ADD Lavalink.jar application.yml ./

ENTRYPOINT ["java", "-Djdk.tls.client.protocols=TLSv1.2", "-Xmx4G", "-jar", "Lavalink.jar"]