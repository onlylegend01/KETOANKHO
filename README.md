# KETOANKHO
Hệ thống tự động hóa xử lý, làm sạch và kiểm soát dữ liệu kế toán kho; hỗ trợ đồng bộ vào phần mềm ERP MISA với cơ chế bảo mật 2 lớp (2FA).
# KETOANKHO - Hệ Thống Tự Động Hóa Kế Toán & Quản Trị Tồn Kho

Hệ thống tự động hóa xử lý, làm sạch và kiểm soát dữ liệu kế toán kho; hỗ trợ đồng bộ vào phần mềm ERP MISA với cơ chế bảo mật 2 lớp (2FA). Dự án ra đời nhằm giải quyết triệt để "nỗi đau" nhập liệu thủ công của kế toán viên, biến hàng giờ làm việc mệt mỏi thành một nút bấm.

## 🎥 Video Demo & Báo Cáo
> **👉 Xem Video Demo Hoạt Động Của Hệ Thống Tại Đây:** 
> [(https://drive.google.com/file/d/1c8ajd6PyrLty1DrfVnt4JhqCIUaN-QOe/view?usp=drive_link)]

---

## 🚀 Tính Năng Nổi Bật (Core Features)

* **Upload Hàng Loạt (Batch Upload):** Hỗ trợ tải lên cùng lúc hàng trăm hóa đơn (PDF, XML) và nuốt trọn cả các tệp nén (ZIP) mà không cần giải nén thủ công.
* **Bóc Tách Thông Minh Đa Định Dạng:** Tự động lùng sục, đọc hiểu cấu trúc XML/HTML ẩn trong file ZIP để lấy số liệu chuẩn xác 100%.
* **Phân Luồng Tự Động (Auto-Routing):** Nhận diện hóa đơn Mua vào (Nhập kho) hoặc Bán ra (Xuất kho) tự động thông qua đối chiếu Mã số thuế.
* **Từ Điển Học Máy (Smart Mapping):** Tự động "dịch" tên hàng hóa của nhà cung cấp sang mã hàng nội bộ. Kế toán chỉ cần chỉnh sửa 1 lần trên bảng, AI sẽ tự động đồng bộ ngược lại toàn bộ hệ thống.
* **Báo Cáo Thời Gian Thực (Real-time Reporting):** Tích hợp luồng tính toán liên tục, cung cấp ngay lập tức các bảng: Tổng Quan, Nhập Kho, Xuất Kho, Thẻ Kho và Tồn Kho.
* **Giao Diện Chuẩn ERP (AG Grid):** 
    * Hiển thị Master-Detail: Click vào dòng tổng tiền để xổ ra danh sách mặt hàng chi tiết.
    * Tải dữ liệu siêu tốc hàng chục ngàn dòng không độ trễ.
    * Giữ nguyên vị trí cuộn (Scroll Retention) khi cập nhật dữ liệu.
* **Xuất Excel 1-Click:** Đóng gói toàn bộ báo cáo ra file Excel chuẩn định dạng phần mềm MISA.

---

## 💻 Công Nghệ Sử Dụng (Tech Stack)

### Frontend
* **Core:** ReactJS (Vite)
* **Data Grid:** AG Grid Community (Siêu hiệu năng, xử lý dữ liệu lớn)
* **Auth:** Firebase Authentication (Xác thực đa tầng)

### Backend & AI Extraction
* **Core:** Python, FastAPI (Xử lý đa luồng, chịu tải cao)
* **Data Processing:** Pandas (Xử lý bảng dữ liệu, gộp nhóm, tính toán mảng)
* **Extraction Engine:** `pdfplumber`, `BeautifulSoup`, `xml.etree`

### Cloud & Database
* **Storage:** Supabase Storage (Lưu trữ chứng từ gốc dạng đám mây bảo mật)
* **Database:** SQL/PostgreSQL

---

## 🧠 Các Thuật Toán Chạy Ngầm Đáng Chú Ý

1. **Thuật toán Khử nhiễu & Lọc trùng (Data Deduplication):** Rà soát chéo chứng từ, tự động chặn đứng hóa đơn tải lên nhiều lần.
2. **Thuật toán Quét Regex (Regex Engine):** Bóc tách chính xác Thuế suất, Ngày tháng, Tổng tiền giữa văn bản phi cấu trúc.
3. **Phân rã dữ liệu đa tầng (Master-Detail Parser):** Biến mớ dữ liệu phẳng phẳng thành mạng lưới quan hệ cây (Hóa đơn cha -> Mặt hàng con).
4. **Kế toán Tồn kho Liên tục (Perpetual Inventory):** Tự động chốt Thẻ kho theo thời gian thực (Real-time) ngay sau mỗi giao dịch.
