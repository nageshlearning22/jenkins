FROM nginx:latest
RUN rm /usr/share/nginx/html/index.html
COPY index.html /usr/share/nginx/html/
EXPOSE 8080
CMD ["catalina.sh","run"]

FROM maven:3-jdk-11
RUN mkdir -p /build
COPY . /build
WORKDIR /build
RUN mvn clean compile package


