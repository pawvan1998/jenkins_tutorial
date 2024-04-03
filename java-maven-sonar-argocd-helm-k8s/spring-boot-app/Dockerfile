# Use an official Maven runtime as a parent image
FROM maven:3.8.4-openjdk-17-slim

# Set the working directory in the container
WORKDIR /app

# Copy the project files into the container
COPY . .

# Build your application using Maven
RUN mvn clean package

# Specify the command to run your application
CMD ["java", "-jar", "target/your-application.jar"]
