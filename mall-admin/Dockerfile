# Sử dụng base image
FROM openjdk:8

RUN apt-get update && apt-get install -y \
    bash \
    iputils-ping

EXPOSE 8080

WORKDIR /app

# Copy file jar từ target vào thư mục làm việc trong container
COPY ./target/mall-admin-1.0-SNAPSHOT.jar /app/mall-admin.jar

# Cài đặt các biến môi trường cần thiết
ENV SPRING_PROFILES_ACTIVE=prod

# Cấu hình lệnh để chạy khi container khởi động
ENTRYPOINT ["java", "-jar", "mall-admin.jar"]
