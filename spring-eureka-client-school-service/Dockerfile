FROM alpine:latest

RUN  apk --no-cache add openjdk8 git

RUN \ 
    git clone https://github.com/dky815/eureka.git && \
    cd eureka/spring-eureka-client-school-service && \
    chmod +x ./mvnw && \
    ./mvnw clean package

WORKDIR /eureka/spring-eureka-client-school-service

CMD ["./mvnw","spring-boot:run"]

EXPOSE 9098