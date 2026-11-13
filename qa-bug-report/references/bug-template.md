# Bug report template

**Title:**  
`[Environment/Area] [Action or condition] causes [observable problem]`

**Environment:**

- Environment:
- Build/Commit:
- Browser/OS/Device:
- Account/Test data:

**Preconditions:**

**Steps to reproduce:**

1.
2.
3.

**Actual Result:**

**Expected Result:**

**Reproducibility:**  
`x/y attempts` hoặc `Always/Intermittent`.

**Impact/Scope observed:**

**Severity:**  
`Blocker`, `Critical`, `Major`, `Minor`, `Trivial`.

**Priority:**  
Chỉ ghi khi đủ cơ sở: `P0`, `P1`, `P2`, `P3`.

**Evidence:**

- Screenshot/video:
- Console/network/backend log:
- Request/response đã mask secret:
- Requirement/design reference:

**Notes/Questions:**

## Severity guide

- `Blocker`: Không thể tiếp tục luồng test/release quan trọng và không có workaround.
- `Critical`: Mất dữ liệu, security nghiêm trọng, crash diện rộng hoặc core flow hỏng.
- `Major`: Chức năng chính sai, impact lớn, workaround khó.
- `Minor`: Impact giới hạn, có workaround rõ ràng.
- `Trivial`: Cosmetic hoặc wording, không ảnh hưởng flow.
