---
name: qa-manual-test-design
description: Design and review manual QA test cases from requirements or user stories, trace coverage, identify gaps and edge cases, and consolidate redundant cases without losing distinct risks.
---

# Thiết kế và review test case QA manual

Dùng khi người dùng muốn phân tích requirement để thiết kế một bộ manual test case, hoặc yêu cầu đồng thời tạo, review và rút gọn test case. Tập trung vào hành vi và rủi ro nghiệp vụ, không phụ thuộc vào code hay một công cụ quản lý test cụ thể.

## Quy trình

1. Đọc requirement, acceptance criteria, thiết kế và test case hiện có nếu được cung cấp. Tóm tắt phạm vi, actor/quyền, luồng, business rules và nguồn. Gán ID tham chiếu tạm nếu nguồn chưa có ID, ghi rõ đây là ID do phân tích đặt ra. Phân biệt nội dung đã xác nhận với giả định và đề xuất.
2. Nêu điểm thiếu, mơ hồ hoặc mâu thuẫn kèm câu hỏi BA/PO/Dev theo mức ảnh hưởng. Nếu thiếu dữ liệu, tiếp tục các phần có thể làm; đánh dấu chờ xác nhận, không tự biến giả định thành expected result hay khẳng định hành vi thực tế. Nếu không thể xác định outcome, dùng `Chờ xác nhận: ...` nêu đúng nội dung còn thiếu.
3. Lập coverage matrix ngắn từ từng requirement/AC tới các điều kiện và scenario cần kiểm tra. Xác định phạm vi và mức ưu tiên theo rủi ro; ghi các yêu cầu, scenario hoặc môi trường chưa đủ thông tin. Chọn kỹ thuật phù hợp: equivalence partitioning, boundary value, decision table hoặc state transition. Cân nhắc positive, negative, boundary, edge case, vai trò/quyền, dữ liệu, trạng thái, lỗi/tích hợp, tương thích, hiệu năng và bảo mật cơ bản khi liên quan. Không sinh checklist máy móc hoặc tự đặt ngưỡng, thông báo, URL hay quy tắc chưa có trong nguồn.
4. Tạo test case manual đủ rõ để thực hiện: một mục tiêu hoặc một biến thể có ý nghĩa trong mỗi case, điều kiện tiên quyết và test data cụ thể khi có cơ sở, các bước thao tác, expected result quan sát được và priority theo tác động/rủi ro. Dùng dữ liệu tham số khi nhiều đầu vào có cùng ý nghĩa kiểm thử và oracle; giữ được giá trị biên và expected result của từng biến thể. Ưu tiên các trường hợp khác biệt có giá trị, không chạy hết mọi tổ hợp không cần thiết.
5. Review toàn bộ bộ case đối chiếu độc lập với requirement, coverage matrix và rủi ro đã xác định: tìm thiếu coverage, bước/expected mơ hồ, test data không đủ, lặp và yêu cầu chưa thể kiểm thử. Đề xuất bổ sung hoặc sửa; không coi việc tự review là bằng chứng đã bao phủ mọi rủi ro.
6. Rút gọn case chỉ khi cùng mục tiêu, điều kiện có liên quan và kết quả mong đợi tương đương; ghi ID cũ → ID cuối cùng và lý do gộp hoặc loại. Không gộp chỉ vì giống các bước. Giữ các phân biệt quan trọng về role/permission, boundary, state, dữ liệu, nghiệp vụ, rủi ro hoặc expected result; nếu tham số hóa, liệt kê từng biến thể và expected result tương ứng. Với case hiện có, không sửa nguồn hoặc xóa dữ liệu gốc trừ khi người dùng yêu cầu.
7. Đối chiếu lại matrix sau khi rút gọn, gắn ID case cuối cùng cho từng requirement/AC và đánh dấu `Đã cover`, `Một phần` hoặc `Chưa cover`, nêu gap/chờ xác nhận và lý do. Không tuyên bố coverage tuyệt đối hoặc bịa phần trăm nếu không có tập yêu cầu rõ ràng và cách tính xác định.

## Đầu ra mặc định

Trả lời tiếng Việt, dùng thuật ngữ tiếng Anh khi cần; theo ngôn ngữ và mẫu riêng nếu người dùng yêu cầu. Với đầu vào đủ rõ, không trì hoãn việc tạo bản đầu vì các câu hỏi có thể được ghi riêng.

- Tóm tắt phạm vi/business rules và các giả định hoặc câu hỏi cần xác nhận theo mức ưu tiên.
- Coverage matrix: Requirement/AC | Scenario hoặc điều kiện | ID test case cuối | Trạng thái/gap.
- Bảng test case cuối: **ID | Requirement/AC | Mô tả | Preconditions | Steps | Test data | Expected result | Priority**. Đánh số bước khi hữu ích và đảm bảo kết quả tương ứng kiểm chứng được.
- Review ngắn: case đã bổ sung/sửa, danh sách ID trước → sau và lý do gộp/loại; ghi `Không có` nếu không có thay đổi. Với bộ dài, trình bày đủ thông tin thay vì rút gọn mất điều kiện.
- Rủi ro, phạm vi chưa kiểm thử và các điểm chờ BA/Dev xác nhận.

Tôn trọng yêu cầu của người dùng nếu họ chỉ cần một giai đoạn, một phạm vi hẹp, định dạng riêng hoặc review case có sẵn. Không tạo file, cập nhật công cụ quản lý test, chạy test hoặc tương tác với hệ thống bên ngoài chỉ vì skill này được kích hoạt; thực hiện khi yêu cầu và quyền truy cập phù hợp.
