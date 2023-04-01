FROM alpine:latest

RUN  apk --no-cache add openjdk8 git

RUN \ 
    git clone https://github.com/dky815/eureka.git && \
    cd eureka/gateway && \
    chmod +x ./mvnw && \
    ./mvnw clean package

WORKDIR /eureka/gateway

CMD ["./mvnw","spring-boot:run"]

EXPOSE 9100