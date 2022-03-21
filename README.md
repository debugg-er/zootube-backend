
# HƯỚNG DẪN CÀI ĐẶT
## Cài đặt Back-end
Bước 1: Cài đặt các công cụ git, docker, docker-compose từ trang chủ trên môi trường linux.

Bước 2: Tải về các file cấu hình và kịch bản của đề tài và điều hướng vào dự
án:
```
git clone https://github.com/backy4rd/zootube-backend
cd zootube-backend
```
Bước 3: Build và chạy toàn bộ dự án:

    docker-compose --env-file .env.example up --build -d

## Cài đặt Front-end
Bước 1: Tải về source code của dự án ReactJS và điều hướng vào dự án:

    git clone https://github.com/backy4rd/zootube
    cd zootube

Bước 2: Tải về các thư viện mà dự án sử dụng:

    npm install

Bước 3: Tạo file .env tại đường dẫn gốc của dự án. Cập nhật nội dung của file
này để Front-end có thể gọi tới Back-end như sau:

    REACT_APP_API_URL=http://localhost:8080/api
    REACT_APP_LIVE_URL=http://localhost:8080/live
    REACT_APP_RTMP_URL=rtmp://localhost:8080/live
    REACT_APP_STATIC_URL=http://localhost:8080/static
    REACT_APP_CHAT_HOST=http://localhost:8080
    REACT_APP_CHAT_PATH=/chat

Bước 4: Chạy dự án. Sau khi chạy, trình duyệt sẽ tự động được mở ở địa chỉ
http://localhost:3000

    npm start
## Tham chiếu
- API Service: https://github.com/backy4rd/zootube-api
- Live chat Service: https://github.com/backy4rd/zootube-media
- Livestream Service: https://github.com/backy4rd/zootube-live
- Media Service: https://github.com/backy4rd/zootube-chat
