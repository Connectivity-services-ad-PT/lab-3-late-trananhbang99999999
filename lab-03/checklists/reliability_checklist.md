# Reliability Checklist - Team A4 AI Vision

## 1. OpenAPI Contract & Linting
- [x] Mỗi operation có ít nhất một response thành công 2xx.
- [x] Mỗi operation có ít nhất một response lỗi 4xx.
- [x] Cấu trúc lỗi tuân thủ chuẩn `ProblemDetails` (có status từ 400 đến 599).
- [x] Đã cấu hình và chạy Spectral lint không còn lỗi nghiêm trọng.

## 2. Environment & Postman Collection Isolation
- [x] Hoàn toàn KHÔNG hardcode `baseUrl` và `authToken` trong bộ kịch bản kiểm thử.
- [x] Đã phân tách rõ ràng cấu hình giữa môi trường `mock` và môi trường `local`.
- [x] Bộ collection đã được tổ chức phân chia cấu trúc thành 5 thư mục chức năng bắt buộc theo đúng quy định.

## 3. Test Coverage & Boundaries
- [x] Khởi tạo thành công các ca kiểm thử luồng hợp lệ (Happy Path).
- [x] Viết kịch bản kiểm tra an toàn bảo mật khi thiếu token xác thực (Auth Test).
- [x] Thiết lập các ca kiểm thử biên dữ liệu đầu vào vượt ngưỡng hợp lệ (`confidenceThreshold = 1.5`).
- [x] Mọi ca kiểm thử độ tin cậy đều thực hiện kiểm tra dữ liệu phản hồi (`response`) thực tế trả về từ phía server, thay vì chỉ kiểm tra lại gói tin gửi đi (`request`).