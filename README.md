# Tổng quan
- Clone project về: http://192.168.105.11:7990/projects/P2P/repos/platform/browse
- Clone các services con về trong cùng thư mục:Lưu ý không thay đổi tên folder chứa service
    - http://192.168.105.11:7990/projects/P2P/repos/im-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/account-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/loan-service/browse
    - http://192.168.105.11:7990/projects/P2P/repos/loan-application-service/browse

# Phát triển | Chỉnh sửa 1 service: Phát triển service `loan-application-service`
- Sửa file `docker-compose.yml`
- Thay đổi các service khác: `dockerfile: Dockerfile` thành `dockerfile: Dockerfile-prod`
- Thay đổi `dockerfile: Dockerfile-prod` thành `dockerfile: Dockerfile`
- Chạy lệnh: `gradle build -t -x test`

# Khởi chạy platform
- Chạy lệnh `docker-compose up -d --build`