FROM dockerfile/java:oracle-java8

VOLUME /tmp
ADD hello.jar /opt/hello/
EXPOSE 8080
WORKDIR /opt/hello/
CMD ["java", "-Djava.security.egd=file:/dev/./urandom", "-Xms512m", "-Xmx1g", "-jar", "hello.jar"]
