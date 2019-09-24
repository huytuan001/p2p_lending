# Introduction
1. Quy chuẩn viết commit message: https://viblo.asia/p/lam-the-nao-de-viet-mot-git-commit-message-tot-DZrGNNnpGVB
2. API phát triển theo quy chuẩn RESTful: https://restfulapi.net | https://tools.ietf.org/html/rfc6690
3. Gitflow: https://github.com/nvie/gitflow
4. Code quality control sử dụng SonarQube
5. Đặc tả thiết kế API.
6. Checklist for creating new services

# Checklist
- [ ] Spring boot: 2.0.x 
- [ ] Spring Cloud: Finchley Release
- [ ] build.gradle bao gồm: Eureka Client Discovery, Sleuth, Zipkin Client, Spring Boot Admin, Spring boot actuators, Swaggers
- [ ] Tạo run configuration chia sẻ cho môi trường local. 

# Tech
1. Database engine: MariaDB version 10.4
2. Caching: Redis version 5
3. Queue: RabbitMQ version 3 with management UI
4. Mongo version 4.2
5. Naming của database sử dụng "_" thay vì "-"


# Tổng quan
- Clone project về: https://git.five9.vn/mony/platform
- Clone các services con về trong thư mục platform(Lưu ý không thay đổi tên folder chứa service)
    - https://git.five9.vn/mony/config-service
    - https://git.five9.vn/mony/api-gateway
    - https://git.five9.vn/mony/identity-service
    - https://git.five9.vn/mony/account-service
    - https://git.five9.vn/mony/loan-service
    - https://git.five9.vn/mony/loan-application-service
    - https://git.five9.vn/mony/logging-service
    - https://git.five9.vn/mony/payment-service
    - https://git.five9.vn/mony/report-service
    - https://git.five9.vn/mony/scoring-service
    - https://git.five9.vn/mony/im-service
    
    
# Khởi chạy platform(môi trường developement, auto reload on source code change)
1. Cài đặt system enviroment variable: `set COMPOSE_CONVERT_WINDOWS_PATHS=1`
2. Cài đặt Docker cho phép truy xuất vào ổ D (hoặc ổ C)
3. Khởi chạy databases của các service: `docker-compose up -d`
- MariaDB server: 127.0.0.1:3005 root/root
- Mongo server: 127.0.0.1:27017 root/root
- RabbitMQ: 127.0.0.1:15672 guest/guest
3.1: Một số phương thức chay khác: `docker-compose -f docker-compose.yml -f docker-compose.[dev|staging|prod].yml up -d`
4. Khởi tạo các databases sau
- identity_service
- account_service
- loan_service
- loan_application_service
- scoring_service
- report_service
- payment_service
5. Chạy các service trên IDE với cấu hình định nghĩa sẵn (Phục vụ mục đích debug service)