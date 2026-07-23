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

## Hướng dẫn sử dụng chi tiết

### Cách 1: Sử dụng trực tiếp trong cuộc trò chuyện Chat AI (ChatGPT, Claude, Gemini)

1. **Bước 1:** Mở tệp [`templates/input_template.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/templates/input_template.md) và sao chép mẫu định dạng đầu vào.
2. **Bước 2:** Điền thông tin CV của bạn (hỗ trợ văn bản thuần hoặc mã nguồn LaTeX) và Mô tả công việc (JD) vào khung mẫu:

```text
--- CV CỦA TÔI ---
[Dán nội dung CV của bạn vào đây]

--- JOB DESCRIPTION (JD) ---
[Dán nội dung Mô tả công việc vào đây]
```

3. **Bước 3:** Gửi tin nhắn cho AI Agent. Hệ thống sẽ tự động thực hiện quy trình review 3 Phase:
   - **Phase 1:** Đánh giá nhanh 10 giây dưới góc nhìn nhà tuyển dụng (Yes/No phỏng vấn, điểm mạnh, điểm yếu, nghi ngờ).
   - **Phase 2:** Lập ma trận đối chiếu CV vs JD 4 cột và trích xuất từ khóa ưu tiên.
   - **Phase 3:** Đặt câu hỏi làm rõ số liệu và đưa ra bản viết lại Bullet Points `[Trước khi sửa]` -> `[Sau khi sửa]`.

4. **Bước 4 (Tùy chọn):** Trả lời tối đa 3 câu hỏi làm rõ từ AI để nhận bản cập nhật mã LaTeX hoặc văn bản hoàn chỉnh nhất.

---

### Cách 2: Tích hợp làm Trợ lý AI riêng (Custom GPT / Claude Project / Gemini Gem)

1. Mở file [`SYSTEM_PROMPT.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/SYSTEM_PROMPT.md).
2. Sao chép toàn bộ đoạn mã trong phần Master System Prompt.
3. Dán vào phần **Instructions** / **System Prompt** của Custom GPT, Claude Project, Gemini Gem hoặc Cursor/VS Code AI Agent.
4. Lưu cấu hình. Trợ lý AI của bạn giờ đây đã sẵn sàng đánh giá mọi bộ CV & JD được gửi tới.

---

### Cách 3: Tích hợp làm Subagent / Skill cho Antigravity AI Agent

1. Giữ nguyên cấu trúc tệp [`.agents/skills/cv-reviewer-agent/SKILL.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/.agents/skills/cv-reviewer-agent/SKILL.md) trong thư mục dự án.
2. Gọi skill `cv-jd-reviewer` trong các phiên làm việc của Antigravity Agent để tự động kích hoạt quy trình đánh giá CV khắt khe chuẩn ATS.

---

### Cách 4: Chạy thử nghiệm nhanh với dữ liệu mẫu

1. Tham khảo dữ liệu đầu vào mẫu tại [`examples/sample_cv_jd.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/examples/sample_cv_jd.md).
2. Xem mẫu kết quả báo cáo phân tích chuẩn tại [`templates/output_sample.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/templates/output_sample.md).
