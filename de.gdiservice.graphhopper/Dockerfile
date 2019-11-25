FROM openjdk:11-jre-slim

LABEL maintainer="Ralf Trier GDI-Service"

RUN java -version 
ADD target/de.gdiservice.graphhopper-0.12.0.jar /graphhopper-lib/service.jar

WORKDIR /graphhopper-lib

EXPOSE 8989

ENTRYPOINT [ "java", "-jar", "/graphhopper-lib/service.jar", "server", "/graphhopper/conf/config.yml" ]
