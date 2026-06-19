# Consumer-Provider Handshake Memo - Team A4 AI Vision

## 1. Thông tin kết nối phụ thuộc (Dependencies)
- **Service của chúng tôi (Provider):** `AI Vision Service` (Phụ trách nhận diện hình ảnh từ Camera).
- **Service phụ thuộc bên ngoài (Dependency Provider):** `Core Business Service` (Hệ thống quản trị trung tâm, xử lý logic nghiệp vụ sau khi nhận diện).

## 2. Thỏa thuận tích hợp (Integration Contract)
- Để chứng minh khả năng tích hợp hệ thống thấu suốt ngay cả khi `Core Business Service` chưa hoàn thiện code thật, nhóm **AI Vision** đã thiết lập một ca kiểm thử Smoke Test đặc hiệu (`05_Consumer_side_Smoke`) nhắm thẳng vào cổng Mock Endpoint của đối tác.
- **Endpoint kiểm tra:** `POST {{coreBusinessMockUrl}}/access/check`
- **Mục tiêu kiểm chứng:** Đảm bảo gói tin thông báo trạng thái thiết bị và kết quả phân tích từ AI Vision gửi đi đúng định dạng cấu trúc mà hệ thống Core Business yêu cầu.