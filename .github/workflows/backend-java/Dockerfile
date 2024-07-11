# Use an official OpenJDK runtime as a parent image
FROM openjdk:17-jdk-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . .

# Install Gradle
RUN apt-get update && \
    apt-get install -y wget unzip && \
    wget https://services.gradle.org/distributions/gradle-7.3.3-bin.zip && \
    unzip gradle-7.3.3-bin.zip -d /opt && \
    ln -s /opt/gradle-7.3.3/bin/gradle /usr/bin/gradle && \
    gradle -v

# Build the application
RUN gradle build

# Run the application
CMD ["java", "-jar", "build/libs/your-app.jar"]
