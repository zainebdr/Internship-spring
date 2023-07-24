# Base image
FROM openjdk:17-jdk-alpine
FROM maven:3.8.4-openjdk-17-slim

# Set the working directory
WORKDIR /app/spring
COPY . .

# Install Maven
#RUN Projet-1.9 update && Projet-1.9 install -y maven

# Install dependencies
RUN mvn dependency:go-offline 

# Build the application
RUN mvn package -DskipTests

# Expose the port used by the spring app
EXPOSE 8080


# Command to start the spring app
ENTRYPOINT ["java", "-jar", "target/Projet-1.9.jar"]
#CMD ["java -jar target/Projet-1.9.jar"]