# AI Job Search & CV Reviewer Agent System

Hệ thống Trợ lý AI Toàn diện Quản lý Tìm kiếm Việc làm, Đánh giá & Tối ưu CV theo Job Description (JD), Soạn thảo Thư xin việc (Cover Letter) và Luyện tập Phỏng vấn Chuyên nghiệp.

---

## Các tính năng chính của Hệ thống

1. **Recruiter 10-Second Skim (Đánh giá lướt 10 giây):**
   - Đóng vai Nhà tuyển dụng thực tế, khắt kê để đưa ra nhận xét nhanh trong 10s: Ấn tượng đầu tiên, điểm mạnh nổi bật, nghi ngờ lớn nhất, điểm trừ mất điểm nhanh nhất và quyết định Yes/No có mời phỏng vấn hay không.

2. **CV vs JD Matrix Analysis (Phân tích Ma trận đối chiếu):**
   - Trích xuất từ khóa JD (Kỹ năng chuyên môn, Công cụ, Kinh nghiệm, Kỳ vọng, Phẩm chất) và phân loại cấp độ ưu tiên (Rất quan trọng / Quan trọng / Có lợi thế).
   - Lập bảng đối chiếu 4 cột chỉ ra điểm mạnh, điểm thiếu, điểm yếu chung chung và 5 hành động khắc phục cụ thể cho ứng viên.

3. **CV Bullet Rewrite Engine (Tối ưu Bullet Points):**
   - Đặt tối đa 3 câu hỏi làm rõ nếu thiếu số liệu hoặc bối cảnh.
   - Viết lại các bullet points theo dạng `[Trước khi sửa]` -> `[Sau khi sửa]` tuân thủ 10 nguyên tắc vàng (Chuẩn ATS, Động từ hành động mạnh, Cấu trúc Action + Tool + Result, Max 20 từ, Impact-driven, Trung thực 100%).

4. **Recruiter Mock Interview & Q&A Engine (Chuẩn bị & Luyện tập Phỏng vấn):**
   - Tạo bộ câu hỏi phỏng vấn thực tế chia thành 4 nhóm: Kỹ thuật chuyên sâu (Technical Deep Dive), Tình huống thực tế (Case Studies), Hành vi (Behavioral STAR) và Thách thức điểm yếu CV (Red Flag Questions).
   - Hướng dẫn trả lời theo mô hình STAR (Situation - Task - Action - Result) và gợi ý các câu hỏi ngược ấn tượng dành cho Nhà tuyển dụng.

5. **Professional Summary Generator (Tạo phần Giới thiệu bản thân):**
   - Tự động tạo 3 phiên bản phần Giới thiệu bản thân / About Me (Doanh nghiệp chuyên nghiệp, Hiện đại tự tin, Tối ưu từ khóa ATS) dựa trên thông tin kinh nghiệm, ngành nghề, vị trí mục tiêu và kỹ năng. Mỗi phiên bản đảm bảo dưới 90 từ.

6. **Multi-Portal Job Search & Scraper (Tìm kiếm & Thu thập Việc làm):**
   - Tích hợp công cụ tìm kiếm tự động trên nhiều trang tuyển dụng (LinkedIn, Freehire me, Jobindex, Jobnet, Akademikernes Jobbank, Jobdanmark).
   - Tự động phân tích, lọc trùng lặp và xếp hạng mức độ phù hợp của công việc với hồ sơ ứng viên.

7. **Tailored CV & Cover Letter Generator (Tạo CV & Cover Letter LaTeX):**
   - Tự động biên dịch và tạo tệp CV PDF (tối đa 2 trang) và Cover Letter PDF (tối đa 1 trang) chuẩn định dạng LaTeX, tối ưu khả năng đọc của hệ thống ATS (pdftotext verification).

---

## Khả năng ứng dụng đa ngành nghề

Hệ thống AI Agent này hoàn toàn **phù hợp và hoạt động hiệu quả cho mọi ngành nghề**, bởi vì nguyên lý cốt lõi của tuyển dụng (sự tương thích giữa CV và JD) là không thay đổi giữa các lĩnh vực:

- **Công nghệ / IT / Data:** Tối ưu các chỉ số Uptime, xử lý dữ liệu, tối ưu hóa code, các công cụ Python, SQL, Cloud, Docker, Spark, Kafka,...
- **Marketing & Communication:** Tối ưu chỉ số ROAS, CTR, Conversion Rate, Lead, các công cụ Facebook Ads, Google Ads, SEO, Canva,...
- **Sales & Business Development:** Tối ưu chỉ số doanh số, tỷ lệ chốt deal, số lượng khách hàng mới, quy mô hợp đồng, CRM (Salesforce, HubSpot),...
- **Tài chính - Kế toán:** Tối ưu quy mô ngân sách quản lý, tỷ lệ giảm chi phí vận hành, báo cáo kiểm toán, các phần mềm SAP, Fast, Excel,...
- **Nhân sự & Vận hành (HR & Operations):** Tối ưu chỉ số tuyển dụng (Time-to-hire), tỷ lệ giữ chân nhân sự, tối ưu quy trình chuỗi cung ứng, hệ thống ERP, WMS,...

---

## Cấu trúc thư mục toàn diện của Dự án

```text
AI Reviewer Jobs / AI Job Search
├── .agents/
│   └── skills/
│       ├── cv-reviewer-agent/
│       │   └── SKILL.md         # Skill Review CV & Ma trận đối chiếu CV-JD
│       ├── interview-prep-agent/
│       │   └── SKILL.md         # Skill Tạo bộ câu hỏi phỏng vấn & Luyện tập phỏng vấn
│       ├── summary-generator-agent/
│       │   └── SKILL.md         # Skill Viết phần Giới thiệu bản thân (3 phong cách < 90 từ)
│       ├── linkedin-search/     # Skill Tìm kiếm công việc toàn cầu trên LinkedIn
│       ├── freehire-search/     # Skill Tìm kiếm việc làm Tech / Data trên Freehire API
│       ├── jobindex-search/     # Skill Tìm kiếm việc làm Đan Mạch trên Jobindex
│       ├── jobnet-search/       # Skill Tìm kiếm việc làm cổng chính phủ Jobnet
│       ├── jobbank-search/      # Skill Tìm kiếm việc làm Akademikernes Jobbank
│       └── jobdanmark-search/   # Skill Tìm kiếm việc làm Jobdanmark
├── .claude/
│   ├── commands/                # Lệnh workflow (/setup, /scrape, /apply, /rank, /interview, /outcome, /upskill, /expand, /html-report)
│   └── skills/
│       ├── job-application-assistant/ # Thư mục quản lý hồ sơ candidate và quy tắc ứng tuyển
│       └── job-scraper/               # Điều phối tìm kiếm công việc tự động
├── templates/
│   ├── input_template.md        # Mẫu định dạng đầu vào gửi cho AI Agent
│   └── output_sample.md         # Mẫu kết quả phân tích & review chuẩn 3 Phase
├── examples/
│   └── sample_cv_jd.md          # Bộ dữ liệu CV và JD mẫu để chạy thử nghiệm
├── cv/
│   └── main_example.tex         # Mẫu mã nguồn CV chuẩn moderncv LaTeX
├── cover_letters/
│   ├── cover.cls                # Class định dạng Cover Letter LaTeX
│   └── cover_example.tex        # Mẫu thư xin việc Cover Letter
├── documents/                   # Thư mục lưu trữ bằng cấp, chứng chỉ, lịch sử ứng tuyển
├── SYSTEM_PROMPT.md             # Master System Prompt dành cho Custom GPT / Claude / Gemini
├── AGENTS.md                    # Nguyên tắc Thin-Pointer (Single Source of Truth) cho AI Agents
└── README.md                    # Hướng dẫn sử dụng và giới thiệu tổng quan dự án
```

---

## Hướng dẫn Tải xuống & Clone Dự án

### Cách 1: Sử dụng lệnh Git Clone (Khuyên dùng)
Mở Terminal / Command Prompt / Git Bash trên máy tính và chạy lệnh:

```bash
git clone https://github.com/ToMoiChoi/AI-Reviews-Jobs.git
cd AI-Reviews-Jobs
```

### Cách 2: Tải tệp ZIP trực tiếp từ GitHub
1. Truy cập repository: `https://github.com/ToMoiChoi/AI-Reviews-Jobs`
2. Nhấp vào nút **Code** ở góc phải phía trên danh sách tệp.
3. Chọn **Download ZIP**.
4. Giải nén tệp `.zip` trên máy tính để bắt đầu sử dụng.

### Cách 3: Clone qua VS Code / Antigravity IDE
1. Mở phần mềm VS Code hoặc Antigravity IDE.
2. Nhấn tổ hợp phím `Ctrl + Shift + P` (hoặc `Cmd + Shift + P` trên macOS), gõ `Git: Clone` và chọn.
3. Dán đường link: `https://github.com/ToMoiChoi/AI-Reviews-Jobs.git`.
4. Chọn thư mục lưu trữ trên máy tính.

---

## Hướng dẫn Sử dụng Chi tiết

### Cách 1: Sử dụng trực tiếp trong cuộc trò chuyện Chat AI (ChatGPT, Claude, Gemini)

1. **Bước 1:** Mở tệp [`templates/input_template.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/templates/input_template.md) và sao chép mẫu định dạng đầu vào.
2. **Bước 2:** Điền thông tin CV của bạn (hỗ trợ văn bản thuần hoặc mã nguồn LaTeX) và Mô tả công việc (JD) vào khung mẫu:

```text
--- CV CỦA TÔI ---
[Dán nội dung CV của bạn vào đây]

--- JOB DESCRIPTION (JD) ---
[Dán nội dung Mô tả công việc vào đây]
```

3. **Bước 3:** Gửi tin nhắn cho AI Agent. Hệ thống sẽ tự động thực hiện quy trình phân tích và tối ưu theo từng Phase.
4. **Bước 4 (Tùy chọn):** Trả lời các câu hỏi làm rõ từ AI để nhận bản cập nhật mã LaTeX hoặc nội dung hoàn chỉnh nhất.

---

### Cách 2: Tích hợp làm Trợ lý AI riêng (Custom GPT / Claude Project / Gemini Gem)

1. Mở tệp [`SYSTEM_PROMPT.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/SYSTEM_PROMPT.md).
2. Sao chép toàn bộ nội dung trong phần Master System Prompt.
3. Dán vào phần **Instructions** / **System Prompt** của Custom GPT, Claude Project, Gemini Gem hoặc Cursor/VS Code AI Agent.
4. Lưu cấu hình. Trợ lý AI của bạn sẵn sàng đánh giá mọi bộ CV & JD.

---

### Cách 3: Tích hợp làm Subagent / Skill cho Antigravity AI Agent & Claude Code CLI

1. Giữ nguyên cấu trúc các tệp skill trong thư mục `.agents/skills/`.
2. Trong các phiên làm việc của AI Agent (Antigravity hoặc Claude Code), bạn có thể gọi trực tiếp các lệnh slash commands:
   - `/setup`: Khởi tạo hồ sơ năng lực cá nhân từ CV hoặc tài liệu trong thư mục `documents/`.
   - `/scrape`: Tìm kiếm công việc tự động trên các trang tuyển dụng.
   - `/rank`: Xếp hạng danh sách công việc theo mức độ phù hợp.
   - `/apply <URL hoặc JD text>`: Tự động đánh giá fit, tạo CV & Cover Letter LaTeX, kiểm tra ATS và tạo kết quả hoàn chỉnh.
   - `/interview`: Tạo bộ câu hỏi phỏng vấn chuẩn STAR và luyện tập phỏng vấn thử.
   - `/upskill`: Phân tích khoảng trống kỹ năng so với thị trường và tạo lộ trình học tập.

---

### Cách 4: Chạy thử nghiệm nhanh với dữ liệu mẫu

1. Tham khảo dữ liệu đầu vào mẫu tại [`examples/sample_cv_jd.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/examples/sample_cv_jd.md).
2. Xem mẫu kết quả báo cáo phân tích chuẩn tại [`templates/output_sample.md`](file:///c:/Users/Admin/OneDrive%20-%20Thang%20Long%20University/Desktop/Self_Project/AI%20Reviewer%20Jobs/templates/output_sample.md).
