# Introduction
1. Quy chuẩn viết commit message: https://viblo.asia/p/lam-the-nao-de-viet-mot-git-commit-message-tot-DZrGNNnpGVB
2. API phát triển theo quy chuẩn RESTful: https://restfulapi.net | https://tools.ietf.org/html/rfc6690
3. Gitflow: https://github.com/nvie/gitflow
4. Code quality control sử dụng SonarQube
5. Đặc tả thiết kế API: https://documenter.getpostman.com/view/11739/RW1gFHck

# Tech
1. Database engine: MariaDB version 10.
2. Caching: Redis version 5
3. Queue: RabbitMQ version 3 with management UI
4. Mongo version 4
5. Naming của database sử dụng "_" thay vì "-"


# Tổng quan
- Clone project về: http://192.168.105.11:7990/projects/P2P/repos/platform/browse
- Clone các services con về trong thư mục platform(Lưu ý không thay đổi tên folder chứa service)
    - http://192.168.105.11:7990/projects/P2P/repos/api-gateway/browse
    - http://192.168.105.11:7990/projects/P2P/repos/im-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/account-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/loan-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/loan-application-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/logging-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/scoring-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/identity-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/private_configuration/browse
    - http://192.168.105.11:7990/projects/P2P/repos/admin-cp/browse


# Khởi chạy platform(môi trường developement, auto reload on source code change)
1. Cài đặt system enviroment variable: `set COMPOSE_CONVERT_WINDOWS_PATHS=1`

2. Cài đặt Docker cho phép truy xuất vào ổ D (hoặc ổ C)

3. Khởi chạy databases của các service: `docker-compose up -d`
- MariaDB server: 127.0.0.1:3005 root/root
- Mongo server: 127.0.0.1:27017 root/root
- RabbitMQ: 127.0.0.1:15672 guest/guest

4. Khởi tạo các databases sau
- identity_service
- account_service
- loan_service
- loan_application_service
- scoring_service

5. Chạy các service trên IDE với cấu hình định nghĩa sẵn