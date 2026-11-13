---
name: qa-requirement-analysis
description: Phân tích requirement hoặc user story dưới góc nhìn QA, tìm điểm mơ hồ, mâu thuẫn, thiếu acceptance criteria và lập traceability. Sử dụng trước khi thiết kế test khi yêu cầu chưa rõ; không dùng để tự ý thay BA chốt business rule.
---

# Phân Tích Requirement Dành Cho QA

## Mục tiêu

Chuyển requirement thành các hành vi có thể kiểm chứng, đồng thời tách rõ nội dung đã xác nhận, điểm chưa rõ và giả định.

## Nguyên tắc nguồn

1. Ưu tiên requirement và acceptance criteria đã được xác nhận.
2. Ghi lại nguồn cho từng kết luận quan trọng khi có nhiều tài liệu.
3. Nếu các nguồn mâu thuẫn, không tự chọn một bên; đánh dấu `Conflict` và nêu câu hỏi cần xác nhận.
4. Không biến giả định thành business rule.
5. Không suy diễn hành vi từ mockup nếu tài liệu không quy định.

## Quy trình

1. Xác định actor, trigger, precondition, luồng chính, kết quả và dữ liệu bị tác động.
2. Tách requirement thành các atomic requirement, mỗi mục chỉ mô tả một hành vi có thể verify.
3. Kiểm tra các nhóm: input, validation, state transition, error handling, integration, persistence và non-functional constraint.
4. Phân loại phát hiện thành `Missing`, `Ambiguous`, `Conflict`, `Inconsistent` hoặc `Unverifiable`.
5. Viết câu hỏi xác nhận cụ thể, có lựa chọn khi có thể và nêu ảnh hưởng nếu chưa được trả lời.
6. Đề xuất acceptance criteria theo Given/When/Then chỉ khi người dùng yêu cầu; ghi rõ là đề xuất, không phải requirement đã chốt.
7. Lập traceability từ requirement gốc sang atomic requirement và trạng thái phân tích.

## Đầu ra

Đọc [references/output-format.md](references/output-format.md) và dùng đúng các bảng cần thiết. Bỏ qua bảng không có nội dung.

## Quality gate

- Mỗi kết luận phải có nguồn hoặc được đánh dấu là giả định.
- Câu hỏi phải cụ thể và có thể trả lời.
- Requirement phải có kết quả quan sát được.
- Không tự thêm scope, role/permission hoặc business rule ngoài nguồn.
- Các mâu thuẫn và blocker phải được đặt trước phần tóm tắt.
