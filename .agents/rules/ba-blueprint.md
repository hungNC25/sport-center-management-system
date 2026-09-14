# Rule: BA Blueprint & GitHub Delivery Model

## Communication & Language
- Sử dụng tiếng Việt chuẩn trừ khi người dùng yêu cầu ngôn ngữ khác.
- Không biến giả định thành sự thật. Mọi thông tin chưa kiểm chứng phải được dán nhãn `[Assumption]` hoặc `[Open Question]`.

## Traceability Hierarchy
Mọi thành phần trong blueprint và hệ thống phải tuân thủ cây truy vết:
`Business Goal (BR) -> Functional Requirement (FR) -> Use Case (UC) -> User Story (US) -> GitHub Issue -> Branch -> PR -> Test Evidence -> Done`

## Naming Conventions
- Requirement ID: `BR-###`, `FR-###`, `NFR-###`
- Use Case ID: `UC-###`
- User Story ID: `US-###`
- Issue Title: `[FR-###] Tên chức năng ngắn gọn`
- Branch: `<type>/<issue-number>-<short-slug>` (Ví dụ: `feat/12-member-checkin`)

## GitHub Project Sync Rules
- Đọc cấu hình từ `.env` (`GITHUB_PROJECT_URL`, `GITHUB_OWNER`, `GITHUB_REPO` hoặc `GITHUB_REPOSITORY`, `GITHUB_PROJECT_NUMBER`, `GITHUB_TOKEN`).
- Không bao giờ hiển thị token hoặc secret trong chat, commit, issue body hoặc PR description.
- Nếu `GITHUB_PROJECT_DRY_RUN=true`, in ra bảng mô phỏng (dry-run summary) các item và field sẽ cập nhật, không gọi API ghi.
