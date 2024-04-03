# Use a base image with required dependencies
FROM alpine:latest

# Set environment variables for locale
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8

# Install required packages using apk
RUN apk update && apk add --no-cache openjdk11-jdk docker

# Set Java environment variables
ENV JAVA_HOME=/usr/lib/jvm/java-11-openjdk
ENV PATH=$PATH:$JAVA_HOME/bin

# Set working directory
WORKDIR /opt/app

# Copy the application JAR file into the container
COPY target/spring-boot-web.jar app.jar

# Specify the default command to run the Java application
ENTRYPOINT ["java", "-jar", "app.jar"]
