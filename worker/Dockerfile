FROM schoolofdevops/maven

WORKDIR /app

COPY . .

RUN mvn package && \
    mvn target/worker-jar-with-dependencies.jar /run/worker.jar && \
    rm -rf /app/*

CMD java -jar /run/worker.jar
