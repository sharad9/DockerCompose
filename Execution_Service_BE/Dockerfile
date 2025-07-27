# Use slim OpenJDK 17 image
FROM openjdk:17-slim

# Install required tools: Python3, pip, gcc, g++
RUN apt-get update && \
    apt-get install -y python3 python3-pip gcc g++ && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Set working directory inside container
WORKDIR /app

# Ensure the directory for user-submitted code exists
RUN mkdir -p UserSubmittedCodes

# Copy your Spring Boot JAR into the container
COPY Execution_Service_BE-0.0.1-SNAPSHOT.jar /app/Execution_Service_BE-0.0.1-SNAPSHOT.jar

# Expose the port your Spring Boot app runs on (Tomcat embedded)
EXPOSE 6001

# Set entrypoint to create code directory before starting app
ENTRYPOINT ["sh", "-c", "mkdir -p /app/UserSubmittedCodes && java -jar /app/Execution_Service_BE-0.0.1-SNAPSHOT.jar"]