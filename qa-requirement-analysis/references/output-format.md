# Định dạng phân tích requirement

## 1. Tóm tắt phạm vi

- Mục tiêu:
- In scope:
- Out of scope:
- Nguồn đã dùng:

## 2. Điểm cần xác nhận

| ID | Phân loại | Nội dung/nguồn | Vấn đề | Câu hỏi xác nhận | Ảnh hưởng | Mức độ |
|---|---|---|---|---|---|---|

Mức độ: `Blocker`, `High`, `Medium`, `Low`.

## 3. Atomic requirements

| REQ ID | Actor/Trigger | Hành vi | Kết quả có thể verify | Điều kiện/dữ liệu | Nguồn | Trạng thái |
|---|---|---|---|---|---|---|

Trạng thái: `Confirmed`, `Partial`, `Need confirmation`, `Conflict`.

## 4. Acceptance Criteria đề xuất

Chỉ tạo khi được yêu cầu:

```gherkin
Given [điều kiện]
When [hành động]
Then [kết quả có thể quan sát]
```

## 5. Traceability

| Nguồn/Section | REQ ID | Trạng thái coverage | Ghi chú |
|---|---|---|---|
