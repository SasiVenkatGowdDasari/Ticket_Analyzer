# Stage 1: Build the application using Maven (Updated to Java 21)
FROM maven:3.9.6-eclipse-temurin-21 AS build
WORKDIR /app

# Copy the pom.xml and source code
COPY pom.xml .
COPY src ./src

# Package the application (skip tests to speed up deployment)
RUN mvn clean package -DskipTests

# Stage 2: Run the application (Updated to Java 21)
FROM eclipse-temurin:21-jre
WORKDIR /app

# Copy the generated JAR file from the build stage
COPY --from=build /app/target/*.jar app.jar

# Expose port 8080
EXPOSE 8080

# Run the application
ENTRYPOINT ["java", "-jar", "app.jar"]