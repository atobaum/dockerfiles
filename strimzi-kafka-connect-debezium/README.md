## Prepare Docker Buildx
```
docker buildx create --use --name multiplatform-builder
docker buildx inspect --bootstrap
```

## Build Docker Image
```
docker buildx build --platform linux/amd64,linux/arm64 --tag atobaum/strimzi-kafka:0.48.0-kafka-4.1.0-debezium-3.2.1 --push .
```

## Run Docker Container
```
docker run -d --name strimzi-kafka -p 8083:8083 atobaum/strimzi-kafka:0.48.0-kafka-4.1.0-debezium-3.2.1
```
