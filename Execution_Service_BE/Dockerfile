FROM openjdk

RUN apt-get update && \
    apt-get install -y python3 gcc g++ && \
    apt-get clean && rm -rf /var/lib/apt/lists/*


WORKDIR /app

COPY /Execution_Service_BE-0.0.1-SNAPSHOT.jar /app/Execution_Service_BE-0.0.1-SNAPSHOT.jar

EXPOSE 6000

ENTRYPOINT ["java", "-jar", "Execution_Service_BE-0.0.1-SNAPSHOT.jar"]



