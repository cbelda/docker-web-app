# 1. Build
FROM maven:3.5-jdk-8-alpine AS build
WORKDIR /app
COPY mtsj/. /app
RUN ls -l
RUN mvn install

# 2. Deploy
FROM tomcat:latest
WORKDIR /app
COPY --from=build /path/to/your/server/artifact /usr/local/tomcat/webapps/
EXPOSE 8080