FROM openjdk:17-slim

RUN apt-get update && \
    apt-get install -y python3 python3-pip gcc g++ && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Create directory for code
RUN mkdir -p /app/UserSubmittedCodes

# Optional: Copy any initial test file
# COPY UserSubmittedCodes/test.py /app/UserSubmittedCodes/test.py

ENV EXECUTION_DIRECTORY=/app/UserSubmittedCodes

WORKDIR /app

COPY Execution_Service_BE-0.0.1-SNAPSHOT.jar /app/Execution_Service_BE-0.0.1-SNAPSHOT.jar

EXPOSE 6000

ENTRYPOINT ["java", "-jar", "Execution_Service_BE-0.0.1-SNAPSHOT.jar"]
