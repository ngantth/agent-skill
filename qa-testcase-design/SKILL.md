---
name: qa-testcase-design
description: Thiết kế manual test case và coverage matrix từ requirement, acceptance criteria hoặc user story. Sử dụng khi cần bộ test case positive, negative, boundary và edge case có traceability; không dùng chỉ để review bộ test case đã có.
---

# Thiết Kế Test Case Dành Cho QA

## Mục tiêu

Tạo bộ test case có thể thực thi, không trùng mục tiêu, bao phủ rủi ro và truy vết được về requirement.

## Đầu vào tối thiểu

- Requirement hoặc user story.
- Acceptance criteria nếu có.
- Phạm vi và môi trường test nếu đã biết.

Nếu thiếu thông tin làm thay đổi expected result, đánh dấu `Need confirmation`; không tự chốt.

## Quy trình

1. Tách requirement thành behavior và condition có thể verify.
2. Lập coverage model theo flow, state, input partition, boundary, error và integration.
3. Ưu tiên theo rủi ro: business impact, tần suất, khả năng lỗi và khả năng phát hiện.
4. Tạo test case cho các nhóm phù hợp: happy path, alternative, negative, boundary, validation, state transition, retry, persistence, integration, compatibility, performance và security cơ bản.
5. Không tạo role/permission test nếu requirement không đề cập và người dùng không yêu cầu.
6. Mỗi test case chỉ có một mục tiêu chính. Dùng parameterization nếu chỉ khác data nhưng cùng logic và expected behavior.
7. Expected result phải chỉ rõ UI/API/DB/state nào thay đổi và cách verify.
8. Lập coverage matrix và nêu rõ requirement chưa được bao phủ.

## Đầu ra

Đọc [references/testcase-template.md](references/testcase-template.md) và [references/coverage-checklist.md](references/coverage-checklist.md).

## Quality gate

- Tất cả acceptance criteria có ít nhất một test case hoặc lý do chưa bao phủ.
- Có negative và boundary test khi feature có input hoặc giới hạn.
- Step độc lập, có thứ tự và không chứa expected result mơ hồ.
- Test data không chứa secret hoặc dữ liệu cá nhân thật.
- Không lặp test case chỉ để tăng số lượng.
