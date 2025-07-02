# 📅 Day 1–2: Odoo Basics & Setup

## 🎯 Mục tiêu học tập:

Kết thúc 2 ngày học này, bạn sẽ có thể:

- Hiểu rõ cấu trúc giao diện người dùng của Odoo 18, bao gồm các thành phần chính như Top Bar, App Switcher, Kanban View, List View, Form View, Search + Filters.
- Nắm vững cách cấu hình thông tin công ty cơ bản như tên, logo, địa chỉ, ngôn ngữ, múi giờ và cấu hình tài chính.
- Thành thạo việc tạo mới và quản lý người dùng, phân quyền truy cập dựa trên các nhóm quyền (Roles/Groups) trong từng module.
- Hiểu và thiết lập tính năng đa công ty (Multi-company), biết cách chuyển đổi giữa các công ty và nhận diện các thành phần dữ liệu bị tách biệt.
- Cài đặt và khởi tạo một instance Odoo 18 (bằng Docker hoặc mã nguồn) để thực hành.
- Biết cách bật và sử dụng chế độ nhà phát triển (Developer Mode) để xem các thông tin kỹ thuật hữu ích.

---

## 📌 Modules cần active và vai trò trong hệ thống:

- **Base (mặc định, luôn có sẵn)**: module cốt lõi, không cần active.
- **Contacts (contacts)**: Quản lý liên hệ – khách hàng, nhà cung cấp, nhân viên.
- **Sales (sale_management) / CRM (crm)**: Quản lý bán hàng / mối quan hệ khách hàng.
- **Settings**: khu vực cấu hình hệ thống.
- **Multi-company Support**: Cho phép Odoo quản lý nhiều công ty riêng biệt.

---

## 🔧 Mục tiêu chính trong thực hành:

- Thiết lập Odoo 18 bằng Docker.
- Cấu hình công ty mặc định và thêm công ty mới.
- Tạo người dùng với quyền và công ty khác nhau.
- Chuyển đổi giữa công ty, kiểm tra chia sẻ dữ liệu.
- Khám phá giao diện chính, bật Developer Mode.

---

## 📖 Tài liệu học tập và tham khảo:

- [Odoo User Interface Docs](https://www.odoo.com/documentation/18.0/user)
- [Odoo Setup for Dev](https://www.odoo.com/documentation/18.0/administration/install)
- [Multi-Company Guide](https://www.odoo.com/documentation/18.0/applications/general/multi_company)

---

## 🧪 Bài tập thực hành – Odoo Basics & Setup (Day 1–2)

### Bài tập 1: Thiết lập hệ thống Odoo

1. Cài đặt Odoo 18 bằng Docker.
2. Truy cập Odoo, bật Developer Mode bằng `/debug`.
3. Vào `Settings` và cập nhật thông tin công ty mặc định.
4. Bật Multi-company tại `Settings > General Settings > Multi Companies`.
5. Thêm công ty mới: "Công ty TNHH ABC".

### Bài tập 2: Quản lý người dùng & phân quyền

Tạo 3 user:

| User       | Email              | Quyền           | Công ty mặc định | Công ty truy cập         |
|------------|--------------------|------------------|------------------|---------------------------|
| admin      | (tùy chọn)         | Super Admin      | Công ty TNHH ABC | ABC & Your Company        |
| ketoan1    | ketoan1@abc.com    | Accountant       | Công ty TNHH ABC | ABC only                  |
| nhansu1    | nhansu1@abc.com    | HR Officer       | Công ty TNHH ABC | ABC only                  |

Đăng nhập từng user để kiểm tra quyền.

### Bài tập 3: Kiểm tra dữ liệu liên công ty

- Tạo liên hệ với `admin` ở "Công ty TNHH ABC".
- Kiểm tra liên hệ bằng `ketoan1`.
- Bật tùy chọn "Share Contacts" để kiểm tra chia sẻ dữ liệu.

### Bài tập 4: Thử tạo record trong nhiều công ty

- Tạo sản phẩm ở từng công ty.
- Kiểm tra sự tách biệt khi chuyển công ty.

### Bài tập 5: Bật và kiểm tra các module cơ bản

- Cài: Contacts, Sales, Inventory.
- Liệt kê các view chính của từng module: Kanban, List, Form, Graph, Calendar...

---

## ❓ Quiz ôn tập – Odoo Basics & Setup (Odoo 18)

**Câu 1:** Developer Mode dùng để làm gì?  
**Đáp án:** B. Bật các tính năng kỹ thuật như xem ID trường, cấu trúc view

**Câu 2:** Khi tạo bản ghi mới?  
**Đáp án:** C. Gán bản ghi cho công ty đang hoạt động hiện tại

**Câu 3:** Để user thao tác trong nhiều công ty?  
**Đáp án:** B. Gán nhiều công ty cho user

**Câu 4:** Module nào để quản lý khách hàng?  
**Đáp án:** D. Contacts

**Câu 5:** Quyền truy cập được kiểm soát bởi?  
**Đáp án:** B. Nhóm quyền (Groups)

**Câu 6:** Nếu user đang ở công ty B và tạo dữ liệu?  
**Đáp án:** B. Dữ liệu được lưu trong công ty đang hoạt động (B)

---

## 📌 Gợi ý ôn thi thêm:

- Thực hành cấu hình người dùng, gán quyền, chuyển đổi công ty.
- Luôn bật Developer Mode để kiểm tra kỹ thuật.
- Tạo checklist cá nhân:

```text
[ ] Tạo người dùng  
[ ] Gán quyền  
[ ] Thêm công ty  
[ ] Kiểm tra quyền  
[ ] Cài app  
[ ] Quan sát UI
