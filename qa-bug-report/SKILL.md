---
name: qa-bug-report
description: Chuẩn hóa bug report từ mô tả, ảnh, video, log hoặc kết quả test thành báo cáo có thể reproduce. Sử dụng khi cần viết mới hoặc cải thiện bug report; không dùng để kết luận root cause khi chưa có bằng chứng kỹ thuật.
---

# Bug Report Dành Cho QA

## Mục tiêu

Tạo bug report ngắn gọn, có đủ bằng chứng để Dev tái hiện, điều tra và verify fix.

## Nguyên tắc bằng chứng

1. Chỉ ghi sự kiện quan sát được vào Actual Result.
2. Expected Result phải đến từ requirement, acceptance criteria, design đã chốt hoặc hành vi hệ thống được xác nhận.
3. Nếu không có nguồn expected, ghi rõ `Expected behavior needs confirmation`.
4. Không khẳng định root cause, hệ thống gây lỗi hoặc bên thứ ba gây lỗi nếu chưa có log/bằng chứng.
5. Loại bỏ password, token, card data, personal data và secret khỏi screenshot, log, URL và payload.

## Quy trình

1. Xác định build, environment, account/data và precondition.
2. Rút gọn reproduction về các bước tối thiểu vẫn gây lỗi.
3. Tách một bug report nếu có nhiều lỗi độc lập hoặc khác root symptom.
4. Viết title theo mẫu `[Area] Action/condition causes observable problem`.
5. Mô tả Actual và Expected tách biệt, có giá trị cụ thể.
6. Đánh giá Severity theo impact; Priority chỉ đề xuất khi có thông tin business urgency.
7. Ghi reproducibility và phạm vi ảnh hưởng đã quan sát.
8. Thêm evidence và điểm cần thu thập thêm.

## Đầu ra

Đọc [references/bug-template.md](references/bug-template.md).

## Quality gate

- Title không chứa suy đoán root cause.
- Steps bắt đầu từ trạng thái xác định và có thể lặp lại.
- Actual/Expected không bị đảo ngược.
- Severity phù hợp với impact, không dựa trên mức độ khó fix.
- Không lộ dữ liệu nhạy cảm.
