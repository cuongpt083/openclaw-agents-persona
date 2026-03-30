---
name: knowledge-ingestor
description: Skill dùng để tự động hóa việc nạp và chuẩn hóa tri thức mới cho Secretary Kim. Sử dụng khi có tài liệu thô (Raw documents), ghi chú hoặc thông tin mới cần đưa vào kho references/ của Kim.
---

# Knowledge Ingestor - The "Kim-Standard" Digestion Skill

Skill này giúp chuẩn hóa mọi tài liệu đầu vào thành định dạng chuyên gia cho Secretary Kim, đảm bảo tính khoa học, chuyên nghiệp và an toàn (Compliance).

## 🏗️ Workflow (Quy trình tiêu hóa tri thức)

### Bước 1: Context Awareness (Nhận diện bối cảnh)
Đọc nội dung từ thư mục nguồn hoặc nội dung Sếp cung cấp. Xác định đây là:
- **Sản phẩm (Product)**: Trà, dinh dưỡng, thực phẩm chức năng.
- **Quy trình (SOP)**: Cách tư vấn, cách vận hành Spa/Fitness.
- **Dinh dưỡng (Nutrition)**: Kiến thức Calo, Macro, TDEE.
- **Kinh doanh (Business)**: Marketing, Sale, Quản lý đội nhóm.

### Bước 2: Kim-Style Transformation (Chuyển đổi chuẩn Kim)
Sử dụng tài liệu `references/kim_markdown_standard.md` để cấu trúc lại nội dung. 
**Yêu cầu tối thượng**: 
- Phải biến các thông tin thô thành các **Hook khoa học** lôi cuốn.
- Luôn phải trích xuất các mục **Thận trọng/Cảnh báo** (Caution).
- Sử dụng giọng văn: Thanh lịch, sắc bén, đáng tin cậy.
- **Metadata SP Injection**: Mỗi file phải chứa metadata ẩn hoặc frontmatter định nghĩa các Atoms: **Aim (Mục tiêu), People (Đối tượng), Locale (Bối cảnh), Example (Ví dụ kịch bản)** để các agent khác dễ dàng kế thừa.

### Bước 3: Categorized Injection (Phân loại & Lưu trữ)
Ghi file đã chuẩn hóa vào thư mục tương ứng trong `/references`:
- `references/products/`
- `references/sop/`
- `references/nutrition/`
- `references/business/`

**Quy tắc đặt tên file**: `tên-sản-phẩm-slug.md` hoặc `ten-quy-trinh-slug.md`.

### Bước 4: Knowledge Pulse (Đồng bộ tri thức)
Sau khi lưu file, THỰC THI lệnh `/refresh-kim` để cập nhật `manifest.md` và thông báo cho Sếp về các điểm mới quan trọng.

## 📋 Kiểm soát chất lượng (QC)
Mọi tài liệu nạp vào phải vượt qua bài kiểm tra "SMART POLE Ready":
1.  Có tiêu đề rõ ràng chưa?
2.  Có mục "Thận trọng" cho sức khỏe chưa? (Nếu là sp/dinh dưỡng).
3.  Có kịch bản mẫu (**Example**) cho Sếp dùng ngay chưa?
4.  Đã xác định rõ **People** (Đối tượng khách hàng mục tiêu) chưa?
5.  Ngôn ngữ có chuyên nghiệp (**Style**) không hay bị lủng củng?

---
*Lưu ý: Mọi tài liệu nạp vào phải luôn tham chiếu đến triết lý "Trust-first" của Anna Nguyễn.*
