---
name: qa-regression-planning
description: Phân tích change impact và lập phạm vi regression theo rủi ro sau khi code, config, schema, API hoặc business rule thay đổi. Sử dụng khi cần chọn smoke, targeted hoặc full regression; không dùng để tự động khẳng định test đã pass.
---

# Lập Kế Hoạch Regression Dành Cho QA

## Mục tiêu

Chọn regression scope đủ bao phủ rủi ro mà không lặp lại toàn bộ test suite một cách máy móc.

## Đầu vào ưu tiên

- Change request, diff, PR hoặc danh sách file/module thay đổi.
- Requirement và acceptance criteria liên quan.
- Dependency, API contract, DB migration, feature flag và config.
- Lịch sử defect và khu vực có tần suất sử dụng cao.

Nếu không có code/diff, ghi rõ phân tích dựa trên functional impact và mức độ tin cậy thấp hơn.

## Quy trình

1. Xác định thay đổi trực tiếp: component, API, DB, config, role, batch/job và third party.
2. Lần theo dependency để tìm impact gián tiếp: caller, consumer, shared component, cache, report, notification và data migration.
3. Đánh giá rủi ro theo impact, likelihood, detectability và change complexity.
4. Chia suite thành:
   - `Smoke`: hệ thống có thể test tiếp.
   - `Targeted regression`: luồng thay đổi và dependency gần.
   - `Broad regression`: shared contract hoặc impact cross-module.
   - `Full regression`: chỉ khi blast radius lớn, migration lớn hoặc release risk cao.
5. Ưu tiên P0-P3, gán owner/data/environment và ước lượng nếu có cơ sở.
6. Nêu rõ scope không test và residual risk.
7. Định nghĩa entry/exit criteria và evidence cần lưu.

## Đầu ra

Đọc [references/regression-template.md](references/regression-template.md).

## Quality gate

- Mỗi scope item liên kết được tới change hoặc dependency.
- Phân biệt direct impact và inferred impact.
- Không gọi full regression nếu không có lý do rõ ràng.
- Có các luồng revenue/data/security/core flow nếu bị ảnh hưởng.
- Có out-of-scope và residual risk để người phụ trách chấp nhận.
