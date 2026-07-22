# AI CV & JD Reviewer Agent

Hệ thống **AI Agent Review & Optimize CV theo Job Description (JD)** chuyên nghiệp dành cho ứng viên.

## Các tính năng chính (Skills)

1. **Recruiter 10-Second Skim (Đánh giá lướt 10s):**
   - Đóng vai Nhà tuyển dụng thực tế, khắt khe, đánh giá ấn tượng đầu tiên, điểm mạnh, nghi ngờ lớn nhất, điểm trừ nhanh nhất và đưa ra quyết định mời phỏng vấn hay không.

2. **CV vs JD Matrix Analysis (Ma trận đối chiếu):**
   - Trích xuất từ khóa JD (Kỹ năng, Công cụ, Kinh nghiệm, Kỳ vọng, Phẩm chất) & Phân loại cấp độ ưu tiên (**Rất quan trọng** / **Quan trọng** / **Có lợi thế**).
   - Bảng đối chiếu 4 cột chỉ ra điểm mạnh, điểm thiếu, điểm yếu chung chung và 5 hành động khắc phục cụ thể.

3. **CV Bullet Rewrite Engine (Tối ưu Bullet Points):**
   - Đặt tối đa 3 câu hỏi làm rõ nếu thiếu số liệu/bối cảnh.
   - Viết lại bullet theo dạng `[Trước khi sửa]` -> `[Sau khi sửa]` tuân thủ **10 nguyên tắc vàng** (Chuẩn ATS, Động từ mạnh, Cấu trúc Action+Tool+Result, Max 20 từ, Impact-driven, Trung thực 100%).

---

## Khả năng ứng dụng đa ngành nghề

Hệ thống AI Agent này hoàn toàn **phù hợp và hoạt động hiệu quả cho mọi ngành nghề**, bởi vì nguyên lý cốt lõi của tuyển dụng (sự tương thích giữa CV và JD) là không thay đổi giữa các lĩnh vực.

Hệ thống tự động điều chỉnh thuật ngữ, công cụ và chỉ số đo lường theo từng ngành:

- **Công nghệ / IT / Data:** Tối ưu các chỉ số Uptime, xử lý dữ liệu, tối ưu hóa code, các công cụ Python, SQL, Cloud, Docker,...
- **Marketing & Communication:** Tối ưu chỉ số ROAS, CTR, Conversion Rate, Lead, các công cụ Facebook Ads, Google Ads, SEO, Canva,...
- **Sales & Business Development:** Tối ưu chỉ số doanh số, tỷ lệ chốt deal, số lượng khách hàng mới, quy mô hợp đồng, CRM (Salesforce, HubSpot),...
- **Tài chính - Kế toán:** Tối ưu quy mô ngân sách quản lý, tỷ lệ giảm chi phí vận hành, báo cáo kiểm toán, các phần mềm SAP, Fast, Excel,...
- **Nhân sự & Vận hành (HR & Operations):** Tối ưu chỉ số tuyển dụng (Time-to-hire), tỷ lệ giữ chân nhân sự, tối ưu quy trình chuỗi cung ứng, hệ thống ERP, WMS,...

---

## Cấu trúc thư mục

```text
├── .agents/
│   └── skills/
│       └── cv-reviewer-agent/
│           └── SKILL.md         # Skill definition dành cho AI Assistant / Subagent
├── templates/
│   ├── input_template.md        # Mẫu định dạng đầu vào gửi cho AI Agent
│   └── output_sample.md         # Mẫu kết quả phân tích & review chuẩn
├── examples/
│   └── sample_cv_jd.md          # Ví dụ bộ dữ liệu CV và JD mẫu để chạy thử
├── SYSTEM_PROMPT.md             # Master System Prompt dành cho Custom GPT / Claude / Gemini
└── README.md                    # Hướng dẫn sử dụng và giới thiệu dự án
```

---

## Hướng dẫn sử dụng

### Cách 1: Sử dụng trực tiếp trong cuộc trò chuyện này
Gửi cho AI thông tin theo mẫu:

```text
--- CV CỦA TÔI ---
[Dán nội dung CV của bạn vào đây]

--- JOB DESCRIPTION (JD) ---
[Dán nội dung Mô tả công việc vào đây]
```

### Cách 2: Tự tạo Custom GPT / Trợ lý AI riêng
1. Mở file [`SYSTEM_PROMPT.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/SYSTEM_PROMPT.md).
2. Sao chép đoạn System Prompt trong block code.
3. Dán vào phần **Instructions** / **System Prompt** của Custom GPT, Claude Project, hoặc Gemini Gem.
