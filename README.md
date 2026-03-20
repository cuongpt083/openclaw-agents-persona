# OpenClaw AI Agent Personas

Dự án này là một bộ sưu tập các **Persona (Nhân cách)** và **Workflows (Quy trình làm việc)** chuyên biệt được thiết kế cho **OpenClaw Agent**. Mục tiêu của repository là cung cấp các trợ lý AI có "linh hồn" (Soul) và bộ kỹ năng sắc bén để giải quyết các bài toán nghiên cứu, vận hành và săn tìm cơ hội công nghệ.

## 🚀 Persona nổi bật: The Research Assistant

Nằm tại: `research-assistant/`

Trợ lý này không chỉ tổng hợp thông tin; nó là một **Radar Cơ hội** chuyên săn tìm các tín hiệu công nghệ mới (AI, ML, Fintech) từ các thị trường dẫn đầu và đối chiếu khả năng áp dụng tại Việt Nam.

### Các thành phần chính của Persona:
*   **IDENTITY.md & SOUL.md**: Định nghĩa phong cách làm việc sắc bén, điềm tĩnh và các nguyên tắc cốt lõi về kỷ luật nguồn tin.
*   **AGENTS.md & TOOLS.md**: Quy trình vận hành chuẩn (Workflows) để săn tín hiệu trong cửa sổ 90 ngày và cách sử dụng các công cụ như `web_search`, `web_fetch`, `browser`.
*   **Hệ thống Registry Nguồn tin (`references/`)**: 
    *   **China Tech Hub**: Danh mục các chuyên gia và technical blogs hàng đầu Trung Quốc.
    *   **Western Global Insight**: Các nguồn uy tín từ Âu Mỹ (Substack, Medium) như Latent Space, Ahead of AI, Fintech Brainfood.
    *   **Source Snapshots**: Các bản ghi nhanh về tín hiệu mới nhất để agent truy xuất nhanh.

## 📁 Cấu trúc Repository

*   `research-assistant/`: Persona Trợ lý Nghiên cứu Radar Cơ hội.
    *   `sources/`: Hồ sơ chi tiết các nguồn tin (Profiles).
    *   `source-snapshots/`: Dữ liệu tín hiệu gần nhất (Q1 2026).
    *   `tech-blog-sources-index.md`: Chỉ mục trung tâm để quản lý nguồn tin theo chủ đề.

## 🛠 Cách sử dụng

1.  **Cài đặt**: Sao chép thư mục persona vào không gian làm việc OpenClaw của bạn.
2.  **Cấu hình**: Bổ sung hoặc cập nhật các nguồn tin tại `references/sources/` để phù hợp với lĩnh vực bạn quan tâm.
3.  **Vận hành**: Sử dụng OpenClaw Agent với các skill như `opportunity-radar` để bắt đầu quét thị trường.

---
*Dự án được xây dựng nhằm giúp cộng đồng công nghệ Việt Nam tiếp cận nhanh hơn với các tri thức và tín hiệu công nghệ tiên tiến nhất từ cả Đông và Tây.*
