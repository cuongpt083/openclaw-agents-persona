# TOOLS.md - Hướng dẫn dùng công cụ OpenClaw cho Research Assistant

## Mục đích của file này

File này chỉ mô tả:
- Agent nên dùng **tool nào của OpenClaw** cho từng loại tác vụ nghiên cứu.
- Khi nào nên đổi từ tool này sang tool khác.
- Những giới hạn cần lưu ý khi dùng tool.

Các quy tắc về:
- chọn thị trường ưu tiên,
- xếp hạng nguồn,
- chấm điểm cơ hội,
- format `Opportunity Radar`,

không phải là định nghĩa của tool. Chúng nên nằm ở:
- [AGENTS.md](/home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/AGENTS.md)
- [SOUL.md](/home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/SOUL.md)
- [EXAMPLES.md](/home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/EXAMPLES.md)
- hoặc skill [opportunity-radar](/home/cuongpt/Workspaces/openclaw-agents-persona/skills/opportunity-radar/SKILL.md) khi cần workflow tái sử dụng.

Theo docs chính thức của OpenClaw, tools là các năng lực first-class như `web_search`, `web_fetch`, `browser`; còn skills là các thư mục riêng có `SKILL.md` để dạy agent workflow hoặc capability mới.

## Tool ưu tiên cho research

### `web_search`

Dùng để:
- săn tín hiệu mới trong 90 ngày gần nhất,
- tìm paper, technical blog, GitHub repo, conference talk,
- quét nhanh nhiều nguồn trước khi chọn URL để đọc sâu.

Lưu ý:
- Đây là tool phù hợp nhất cho bước discovery.
- Cần API key của web provider theo cấu hình OpenClaw.

### `web_fetch`

Dùng để:
- tải và trích xuất nội dung đọc được từ một URL cụ thể,
- đọc bài blog, press release, paper page, agenda conference,
- lấy nội dung sạch hơn để tóm tắt hoặc đối chiếu.

Lưu ý:
- Phù hợp khi đã có URL cụ thể.
- Với site nhiều JavaScript hoặc chặn fetch thường, có thể cần chuyển sang `browser`.

### `browser`

Dùng để:
- mở các site JavaScript-heavy,
- đọc agenda conference, docs, dashboard, hoặc trang động,
- chụp ảnh màn hình hoặc tương tác với UI nếu `web_fetch` không đủ.

Lưu ý:
- Ưu tiên dùng khi `web_fetch` không trích xuất tốt nội dung.
- Không nên dùng browser cho mọi tác vụ tìm kiếm cơ bản nếu `web_search` và `web_fetch` đã đủ.

### `pdf`

Dùng để:
- đọc paper hoặc report ở định dạng PDF,
- trích nội dung từ báo cáo nghiên cứu, whitepaper, tài liệu regulator.

### `image`

Dùng để:
- đọc sơ đồ, chart, infographic, hoặc screenshot từ report hay conference deck nếu cần thêm ngữ cảnh.

## Tool flow khuyến nghị

Khi nghiên cứu trend hoặc competitor:
1. Dùng `web_search` để quét tín hiệu và tìm candidate sources.
2. Dùng `web_fetch` để đọc các URL quan trọng.
3. Nếu trang khó đọc hoặc phụ thuộc JavaScript, chuyển sang `browser`.
4. Nếu nguồn là PDF, dùng `pdf`.
5. Nếu có chart hoặc hình ảnh quan trọng, dùng `image`.

## Khi nào cần skill thay vì tool

Nếu muốn thêm một workflow có thể tái sử dụng, ví dụ:
- `opportunity-radar`
- `competitor-watch`
- `fintech-trend-scout`

thì nên tạo một **skill** riêng trong thư mục `skills/<skill-name>/SKILL.md`, vì theo docs OpenClaw:
- skill là nơi chứa hướng dẫn và workflow cho agent,
- tool là bề mặt năng lực được OpenClaw cấp sẵn hoặc plugin đăng ký.

Nói ngắn gọn:
- `TOOLS.md` nên trả lời câu hỏi: "dùng công cụ nào?"
- `SKILL.md` nên trả lời câu hỏi: "thực hiện workflow nào?"

## Skill đang dùng cho persona này

- Với yêu cầu săn trend, theo dõi đối thủ, hoặc tìm cơ hội áp dụng tại Việt Nam trong AI, ML, banking, finance, fintech, hãy ưu tiên dùng skill [opportunity-radar](/home/cuongpt/Workspaces/openclaw-agents-persona/skills/opportunity-radar/SKILL.md).
- Skill đó đã đóng gói sẵn source policy, ranking logic, và output contract cho `Opportunity Radar`.

## Example References

- Tham khảo [EXAMPLES.md](/home/cuongpt/Workspaces/openclaw-agents-persona/research-assistant/EXAMPLES.md) để xem seed sources và mẫu `Opportunity Radar`.
