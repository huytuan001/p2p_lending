# Intro
1. Quy chuẩn viết commit message: https://viblo.asia/p/lam-the-nao-de-viet-mot-git-commit-message-tot-DZrGNNnpGVB
2. API phát triển theo quy chuẩn RESTful: https://tools.ietf.org/html/rfc6690
3. Gitflow: https://github.com/nvie/gitflow
4. Code quality control sử dụng SonarQube
5. Đặc tả thiết kế API: https://documenter.getpostman.com/view/11739/RW1gFHck

# Tổng quan
- Clone project về: http://192.168.105.11:7990/projects/P2P/repos/platform/browse
- Clone các services con về trong thư mục platform(Lưu ý không thay đổi tên folder chứa service)
    - http://192.168.105.11:7990/projects/P2P/repos/api-gateway/browse
    - http://192.168.105.11:7990/projects/P2P/repos/im-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/account-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/loan-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/loan-application-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/admin-cp/browse


# Khởi chạy platform(môi trường developement, auto reload on source code change)
1. Cài đặt system enviroment variable: `set COMPOSE_CONVERT_WINDOWS_PATHS=1`

2. Cài đặt Docker cho phép truy xuất vào ổ D (hoặc ổ C)

3. Khởi chạy databases của các service: `docker-compose up -d`

4. Chạy lệnh: `gradle build -t -x test` để tự động reload lại ứng dụng khi thay đổi mã nguồn


# Build bản production: `docker-compose build`

# Danh sách micro-services::

## API Gateway(Port 8079 - Remote debug port 5004)


## Notification service(Port 8080 - Remote debug port 5005)


## Account service(Port 8081 - Remote debug port 5006)


## Loan service(Port 8082 - Remote debug port 5007)


## Loan application service(Port 8083 - Remote debug port 5008)

## Admin CP(Port 80)

# Link các API

http://localhost:8079 - API Gateway

http://localhost:8080 - Notification service

http://localhost:8081 - Account service

http://localhost:8082 - Loan service

http://localhost:8083 - Loan application service
