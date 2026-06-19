# Lab 03: AI Vision Service API

Bài Lab thực hiện thiết lập Mock Server bằng Prism và kiểm thử tự động với Newman.

## Cấu trúc thư mục
- `contracts/`: Chứa file định nghĩa API `ai-vision.openapi.yaml`.
- `postman/collections/`: Chứa các kịch bản kiểm thử.
- `postman/environments/`: Chứa cấu hình môi trường.
- `reports/`: Chứa báo cáo kết quả kiểm thử (`newman-report.html`).

## Cách chạy dự án

### 1. Khởi động Mock Server
Mở terminal và chạy lệnh:
```bash
npx prism mock contracts/ai-vision.openapi.yaml -p 4010