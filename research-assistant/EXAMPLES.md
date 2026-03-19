# EXAMPLES.md - Persona-Level Example Guidance

## Mục đích

File này không còn là nơi giữ workflow chính hay bộ examples chi tiết cho `Opportunity Radar`.

Nguồn chuẩn cho phần đó là:
- skill [opportunity-radar](/home/cuongpt/Workspaces/openclaw-agents-persona/skills/opportunity-radar/SKILL.md)
- [source-policy.md](/home/cuongpt/Workspaces/openclaw-agents-persona/skills/opportunity-radar/references/source-policy.md)
- [output-examples.md](/home/cuongpt/Workspaces/openclaw-agents-persona/skills/opportunity-radar/references/output-examples.md)

## Cách dùng trong persona

- Khi yêu cầu thuộc nhóm trend scouting, competitor tracking, hoặc opportunity spotting, persona nên ưu tiên gọi skill `opportunity-radar`.
- Các ví dụ và source patterns cụ thể cho `Opportunity Radar` nên đọc từ thư mục `skills/opportunity-radar/references/`.
- File này chỉ giữ vai trò nhắc rằng persona và skill có liên kết với nhau; không nên lặp lại chi tiết đã có trong skill.

## Khi nào mở rộng file này

Chỉ mở rộng file này nếu cần các ví dụ ở tầng persona mà không thuộc riêng skill `opportunity-radar`, ví dụ:
- phong cách trả lời mặc định của persona trong các yêu cầu nghiên cứu không phải radar,
- ví dụ chuyển đổi giữa `general research mode` và `opportunity radar mode`,
- các anti-pattern ở cấp persona.
