FROM openjdk:8u151-jre-stretch
MAINTAINER jin820100449@qq.com

RUN mkdir /datacenter && \
    mkdir /datacenter/out && \
    mkdir /datacenter/out/logs && \
    mkdir /datacenter/out/properties
VOLUME /datacenter/out/logs
WORKDIR /datacenter
ENTRYPOINT [ "sh", "-c", "java $JAVA_OPTS -jar /datacenter/datacenter-web.jar -Dfile.encoding=utf-8 " ]
CMD ["--spring.config.location=/datacenter/application.properties"]
COPY datacenter-web.jar .
COPY application.properties .
EXPOSE 20802
EXPOSE 8088
