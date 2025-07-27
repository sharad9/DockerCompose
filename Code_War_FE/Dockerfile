FROM openjdk:17-jdk-slim
WORKDIR /app

# Copy the JAR file
COPY target/Code_War_FE-1.0-SNAPSHOT.jar /app/Code_War_FE-1.0-SNAPSHOT.jar

# Copy the entire frontend folder
COPY frontend/ /app/frontend/

EXPOSE 8081

ENTRYPOINT ["java", "-jar", "Code_War_FE-1.0-SNAPSHOT.jar"]
