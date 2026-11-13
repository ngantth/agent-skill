# Regression plan template

## 1. Change summary

- Change:
- Source/PR/REQ:
- Components affected directly:
- Assumptions/open questions:

## 2. Impact analysis

| Impact ID | Area/Flow | Direct/Indirect | Dependency/evidence | Failure impact | Risk |
|---|---|---|---|---|---|

Risk: `Critical`, `High`, `Medium`, `Low`.

## 3. Regression scope

| Scope ID | Suite level | Area/Scenario | Reason | Priority | Environment/Data | Expected evidence |
|---|---|---|---|---|---|---|

Suite level: `Smoke`, `Targeted`, `Broad`, `Full`.

## 4. Execution order

1. Environment and deployment health.
2. Smoke/core flow.
3. Changed behavior.
4. Direct dependencies.
5. Indirect/shared impact.
6. Non-functional checks khi liên quan.

## 5. Entry/Exit criteria

### Entry

- Build và environment sẵn sàng.
- Test data/dependency sẵn sàng.
- Blocker từ requirement đã được xử lý hoặc chấp nhận.

### Exit

- Tất cả P0/P1 đã execute.
- Không còn open blocker/critical không được chấp nhận.
- Evidence và defect link đã được cập nhật.

## 6. Out of scope and residual risk

| Area | Lý do không test | Residual risk | Người chấp nhận |
|---|---|---|---|
