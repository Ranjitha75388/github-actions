# Step 1: Use Maven to build the project.
FROM maven:3.8.5-openjdk-17 AS build

WORKDIR /app

# Copy the project files to the container.
COPY . .

# Build the application (without running tests)
RUN mvn clean package -DskipTests

# Step 2: Use a minimal Java runtime for the final image
FROM openjdk:17-jdk-slim

WORKDIR /app

# Copy the built JAR file from the Maven stage
COPY --from=build /app/target/springboot-backend-0.0.1-SNAPSHOT.jar /app/springboot-backend.jar

# Expose the application port
EXPOSE 8080

# Run the application
ENTRYPOINT ["java", "-jar", "/app/springboot-backend.jar"]

