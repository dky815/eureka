FROM alpine:latest

RUN  apk --no-cache add openjdk8 git

RUN \ 
    git clone https://github.com/dky815/eureka.git && \
    cd eureka/spring-eureka-server && \
    chmod +x ./mvnw && \
    ./mvnw clean package

WORKDIR /eureka/spring-eureka-server

CMD ["./mvnw","spring-boot:run"]

EXPOSE 8761