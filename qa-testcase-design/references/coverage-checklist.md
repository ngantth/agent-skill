# Coverage checklist

Chỉ áp dụng các mục liên quan; không ép mọi feature phải có tất cả.

## Functional

- Happy path và alternative flow.
- Empty, null, invalid format, duplicate.
- Min, max, just below, just above.
- State transition và hành động không hợp lệ theo state.
- Cancel, back, refresh, reload, retry, double submit.
- Partial success, timeout, dependency failure.
- Persistence sau refresh, relogin hoặc job async.

## UI/UX

- Loading, empty, error, disabled và success state.
- Text, translation, overflow và responsive.
- Keyboard navigation và focus cơ bản.

## Integration/data

- UI/API/DB mapping và data type.
- Idempotency, duplicate request và stale data.
- Third-party unavailable hoặc trả về dữ liệu thiếu.

## Non-functional cơ bản

- Dữ liệu lớn và response time hợp lý.
- Sensitive data không lộ trên UI, URL, log hoặc payload không cần thiết.
- Browser/device được hỗ trợ.
