---
name: qa-testcase-review
description: Review bộ test case hiện có để tìm coverage gap, case trùng lặp, bước không thực thi được và expected result mơ hồ. Sử dụng khi người dùng cung cấp test case cần đánh giá; không dùng để tạo bộ test case mới từ đầu trừ khi được yêu cầu bổ sung gap.
---

# Review Test Case Dành Cho QA

## Mục tiêu

Đánh giá chất lượng bộ test case theo requirement và rủi ro, đưa ra phát hiện có bằng chứng và đề xuất sửa cụ thể.

## Nguyên tắc

- Review theo requirement/acceptance criteria nếu có; nếu không có, ghi rõ review chỉ dựa trên tính rõ ràng và heuristic QA.
- Phân biệt `Missing coverage` với `Requirement unclear`.
- Không đánh giá pass/fail của sản phẩm; chỉ đánh giá chất lượng test artifact.
- Không viết lại toàn bộ test case nếu người dùng chỉ yêu cầu review.
- Không coi khác wording là duplicate; duplicate phải cùng mục tiêu, điều kiện và rủi ro.

## Quy trình

1. Lập inventory requirement, test case và mapping hiện có.
2. Kiểm tra từng case về objective, precondition, data, steps, expected result và traceability.
3. Tìm coverage gap theo positive, negative, boundary, state, error, integration và non-functional liên quan.
4. Tìm overlap và phân loại: duplicate hoàn toàn, có thể parameterize, hoặc cần giữ riêng vì rủi ro khác.
5. Đánh giá khả năng thực thi và khả năng lặp lại.
6. Xếp phát hiện theo `Critical`, `Major`, `Minor` và đưa đề xuất sửa.
7. Chỉ tạo test case bổ sung cho gap khi người dùng yêu cầu.

## Đầu ra

Đọc [references/review-template.md](references/review-template.md).

## Quality gate

- Mỗi finding phải chỉ rõ TC ID hoặc requirement liên quan.
- Mỗi gap phải giải thích rủi ro nếu không test.
- Không gom nhiều vấn đề không liên quan trong một finding.
- Đề xuất phải hành động được, không dùng mô tả chung chung.
