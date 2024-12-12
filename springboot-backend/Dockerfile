FROM openjdk:17-jdk-slim

WORKDIR /app

COPY target/my-app-0.0.1-SNAPSHOT.jar /app/my-app.jar

ENTRYPOINT ["java", "-jar", "my-app.jar"]
