# Intro
1. Quy chuẩn viết commit message: https://viblo.asia/p/lam-the-nao-de-viet-mot-git-commit-message-tot-DZrGNNnpGVB
2. API phát triển theo quy chuẩn RESTful: https://tools.ietf.org/html/rfc6690
3. Gitflow: https://github.com/nvie/gitflow
4. Code quality control sử dụng SonarQube

# Tổng quan
- Clone project về: http://192.168.105.11:7990/projects/P2P/repos/platform/browse
- Clone các services con về trong cùng thư mục(Lưu ý không thay đổi tên folder chứa service)
    - http://192.168.105.11:7990/projects/P2P/repos/im-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/account-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/loan-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/loan-application-service/browse

- Thiết kế API: https://documenter.getpostman.com/view/11739/RW1gFHck

# Khởi chạy platform(môi trường developement)
1. Chạy lệnh `docker-compose up -d --build`
2. Chạy lệnh: `gradle build -t -x test`

# Build bản production

# Các microservices trong hệ thống:

## IM service:

## Account service:

## Loan service:

## Loan application service:

# Link các API
http://localhost:8080 - IM service
http://localhost:8081 - Account service
http://localhost:8082 - Loan service
http://localhost:8083 - Loan application service
