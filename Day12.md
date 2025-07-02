












📅






 Day 1–2: Odoo Basics & Setup









🎯






 Mục tiêu học tập:




Kết thúc 2 ngày học này, bạn sẽ có thể:










Hiểu rõ cấu trúc giao diện người dùng của Odoo 18, bao gồm các thành phần chính như Top Bar, App Switcher, Kanban View, List View, Form View, Search + Filters.










Nắm vững cách cấu hình thông tin công ty cơ bản như tên, logo, địa chỉ, ngôn ngữ, múi giờ và cấu hình tài chính.










Thành thạo việc tạo mới và quản lý người dùng, phân quyền truy cập dựa trên các nhóm quyền (Roles/Groups) trong từng module.










Hiểu và thiết lập tính năng đa công ty (Multi-company), biết cách chuyển đổi giữa các công ty và nhận diện các thành phần dữ liệu bị tách biệt.










Cài đặt và khởi tạo một instance Odoo 18 (bằng Docker hoặc mã nguồn) để thực hành.










Biết cách bật và sử dụng chế độ nhà phát triển (Developer Mode) để xem các thông tin kỹ thuật hữu ích.









📌






 Modules cần active và vai trò trong hệ thống:




Trong giai đoạn này, các module sau đóng vai trò nền tảng quan trọng:














Base (mặc định, luôn có sẵn):


 Đây là module cốt lõi của Odoo, cung cấp cấu trúc cơ bản cho hệ thống, quản lý dữ liệu chung và là nền tảng để các module khác hoạt động. Bạn không cần "active" nó vì nó luôn có sẵn.














Contacts (contacts):


 














Vai trò:


 Cung cấp cơ sở dữ liệu để quản lý tất cả các liên hệ trong hệ thống, bao gồm khách hàng, nhà cung cấp và cả nhân viên của bạn. Module này là nền tảng cho Sales, Purchase, và các module khác cần thông tin đối tác.














Sales (sale\_management) hoặc CRM (crm - nếu cần tạo khách hàng mẫu):


 














Vai trò:


 Sales quản lý toàn bộ quy trình bán hàng từ báo giá đến đơn hàng và hóa đơn. CRM quản lý mối quan hệ khách hàng và các cơ hội bán hàng. Mặc dù chưa đi sâu vào nghiệp vụ, việc cài đặt giúp bạn có dữ liệu mẫu khách hàng để thực hành phân quyền công ty.














Settings (quyền truy cập thông qua user admin):















Vai trò:


 Không phải là một "module" theo nghĩa truyền thống mà là một khu vực cấu hình hệ thống. Tại đây, bạn có thể truy cập và điều chỉnh các thiết lập toàn cục, bao gồm cấu hình công ty, quản lý người dùng, quyền truy cập và đặc biệt là bật tính năng đa công ty.














Multi-company Support (được bật trong Settings → Users & Companies → Companies):


 














Vai trò:


 Cho phép một instance Odoo quản lý nhiều công ty riêng biệt, mỗi công ty có dữ liệu tài chính, kho, đơn hàng... riêng, nhưng có thể chia sẻ một số thông tin nhất định như liên hệ nếu cấu hình. Đây là một tính năng cực kỳ quan trọng đối với các tập đoàn hoặc doanh nghiệp có nhiều chi nhánh.









🔧






 Mục tiêu chính trong thực hành:










Thiết lập một instance Odoo 18 (sử dụng Docker là phương pháp được khuyến nghị để dễ dàng và nhanh chóng).










Cấu hình thông tin cơ bản cho công ty mặc định và tạo thêm một công ty mới.










Tạo người dùng với các vai trò và quyền hạn khác nhau, đồng thời gán họ vào các công ty cụ thể.










Thực hành chuyển đổi giữa các công ty để kiểm tra việc tách biệt và chia sẻ dữ liệu (đặc biệt là liên hệ và sản phẩm).










Khám phá các giao diện chính của Odoo và bật/tắt chế độ nhà phát triển.






















📖






 Tài liệu học tập và tham khảo:














Tài liệu Odoo Documentation (Official):


 










Odoo User Interface Docs: 




https://www.odoo.com/documentation/18.0/user 










Odoo Setup for Dev: 




https://www.odoo.com/documentation/18.0/administration/install 










Multi-Company Guide: 




https://www.odoo.com/documentation/18.0/applications/general/multi\_company 














Tài liệu ôn tập Day12.docx (đã cung cấp):










Mục 1: Giao Diện Người Dùng (UI Overview).











Mục 2: Cài Đặt Công Ty (Company Configuration).










Mục 3: Người Dùng & Quyền Truy Cập (Users & Access Rights).










Mục 4: Thiết Lập Đa Công Ty (Multi-company).










Mục 5: Cài Đặt & Khởi Tạo Instance Odoo.






















🧪






 Bài tập thực hành – Odoo Basics & Setup (Day 1–2)








Mục tiêu chung:


 Thực hành để làm quen với giao diện, cấu hình ban đầu và hiểu rõ cách hoạt động của hệ thống phân quyền cũng như tính năng đa công ty.














Bài tập 1: Thiết lập hệ thống Odoo


 










Cài đặt Odoo 18 bằng Docker hoặc mã nguồn theo hướng dẫn trong tài liệu. (Khuyến nghị dùng Docker để nhanh chóng và đơn giản).










Sau khi cài đặt, truy cập vào Odoo và bật chế độ Developer bằng cách thêm 




/debug vào URL.










Đi tới 




Settings và cập nhật các thông tin cơ bản của công ty mặc định (ví dụ: Your Company): logo, địa chỉ, múi giờ, ngôn ngữ.










Trong 




Settings > General Settings > Multi Companies, bật tính năng Multi-company.










Đi tới 




Settings > Users & Companies > Companies và thêm một công ty mới với tên: "Công ty TNHH ABC".














Bài tập 2: Quản lý người dùng & phân quyền


 










Đi tới Settings > Users & Companies > Users.










Tạo 3 người dùng mới với các thiết lập sau: 














User 1: admin










Email: (tùy chọn)










Gán quyền: Super Admin (hoặc Admin trên tất cả các module để có toàn quyền).










Công ty mặc định: "Công ty TNHH ABC".











Công ty truy cập: "Công ty TNHH ABC", "Your Company" (tức là có thể truy cập cả hai công ty).














User 2: ketoan1@abc.com










Email: ketoan1@abc.com










Gán quyền: "Accountant" trong module Accounting.










Công ty mặc định: "Công ty TNHH ABC".










Công ty truy cập: Chỉ "Công ty TNHH ABC".














User 3: nhansu1@abc.com










Email: nhansu1@abc.com










Gán quyền: "Employee" hoặc "HR Officer" trong module Human Resources (nếu đã cài đặt HR).










Công ty mặc định: "Công ty TNHH ABC".










Công ty truy cập: Chỉ "Công ty TNHH ABC".










Đăng nhập bằng từng tài khoản vừa tạo để xác minh rằng họ chỉ có thể truy cập các module và dữ liệu theo đúng quyền đã phân và trong công ty được gán.














Bài tập 3: Kiểm tra dữ liệu liên công ty


 










Đăng nhập với tài khoản 




admin và đảm bảo bạn đang ở "Công ty TNHH ABC" (kiểm tra góc trên bên trái).










Đi tới module 




Contacts và tạo một liên hệ mới (ví dụ: "Nguyễn Văn A - Khách hàng ABC").










Đăng xuất khỏi tài khoản admin.










Đăng nhập bằng tài khoản 




ketoan1@abc.com (hoặc bất kỳ user nào chỉ được gán cho "Công ty TNHh ABC") và kiểm tra trong module Contacts xem có thấy liên hệ "Nguyễn Văn A" không.










Đăng nhập lại bằng 




admin, đi tới Settings > General Settings > Multi Companies, bật tùy chọn "Share Contacts" (hoặc tên tương tự).










Đăng xuất và đăng nhập lại bằng 




ketoan1@abc.com để kiểm tra xem liên hệ "Nguyễn Văn A" đã hiển thị chưa.















Bài tập 4: Thử tạo record trong nhiều công ty


 










Với tài khoản 




admin, chuyển sang "Công ty TNHH ABC".










Cài đặt module 




Inventory (nếu chưa cài).










Đi tới 




Inventory > Products và tạo một sản phẩm mới: "Bút Bi Thiên Long".










Chuyển đổi công ty sang "Your Company" (công ty ban đầu).










Đi tới 




Inventory > Products và tạo một sản phẩm mới: "Tập Học Sinh".










Chuyển đổi qua lại giữa "Công ty TNHH ABC" và "Your Company" để kiểm tra tính tách biệt của các sản phẩm bạn vừa tạo.














Bài tập 5: Bật và kiểm tra các module cơ bản


 










Với tài khoản admin, đi tới Apps.










Cài đặt các module sau (nếu chưa cài): Contacts, Sales, Inventory.










Sau khi cài đặt, mở từng module và liệt kê các view chính mà bạn thấy (ví dụ: Kanban, List/Tree, Form, Graph, Calendar...). Ghi chú lại những view mặc định của mỗi module.






















❓






 Quiz ôn tập – Odoo Basics & Setup (Odoo 18)








(Dạng trắc nghiệm – mỗi câu chỉ có 1 đáp án 






đúng







)


 














Câu 1:


 Chế độ Developer Mode trong Odoo có tác dụng gì? 




A. Cho phép người dùng truy cập tất cả dữ liệu trong hệ thống 




B. Bật các tính năng kỹ thuật như xem ID trường, cấu trúc view 




C. Thay đổi giao diện thành chế độ tối 




D. Tự động cấp quyền Super Admin 








Đáp án:


 B 














Câu 2:


 Khi tạo một bản ghi mới (ví dụ: khách hàng), hệ thống sẽ: 




A. Gán bản ghi này cho tất cả các công ty 





B. Không cho phép tạo bản ghi nếu không chọn công ty 




C. Gán bản ghi cho công ty đang hoạt động hiện tại 




D. Tự động chia sẻ cho tất cả người dùng 








Đáp án:


 C 














Câu 3:


 Muốn một người dùng có thể thao tác trong nhiều công ty, ta cần: 




A. Tạo nhiều tài khoản cho từng công ty 




B. Gán nhiều công ty cho user trong phần cấu hình 




C. Bật module HR 




D. Không thể làm điều này 








Đáp án:


 B 














Câu 4:


 Module nào cần cài đặt để người dùng có thể xem và chỉnh sửa thông tin khách hàng? 




A. Sales 




B. Accounting 




C. Inventory 




D. Contacts 








Đáp án:


 D 














Câu 5:


 Trong Odoo, quyền truy cập được kiểm soát dựa trên: 




A. Loại dữ liệu người dùng tạo 




B. Nhóm quyền (Groups) được gán cho người dùng 




C. Loại hệ điều hành người dùng sử dụng 




D. Dung lượng bộ nhớ máy chủ 








Đáp án:


 B 














Câu 6:


 Khi người dùng tạo dữ liệu trong công ty A, nhưng đang chọn công ty B, điều gì xảy ra? 




A. Dữ liệu được lưu ở cả hai công ty 




B. Dữ liệu được lưu trong công ty đang hoạt động (B) 




C. Hệ thống báo lỗi 




D. Không thể tạo dữ liệu trong chế độ multi-company 









Đáp án:


 B 
















📌






 Gợi ý ôn thi thêm:










Thực hành đi thực hành lại các bài tập cấu hình người dùng, gán quyền và kiểm tra việc tách biệt dữ liệu giữa các công ty vì đây là phần nền tảng quan trọng cho kỳ thi chứng chỉ.










Luôn bật chế độ Developer Mode khi thực hành để dễ dàng xem ID, trường kỹ thuật, cấu trúc ORM, điều này rất hữu ích cho các câu hỏi chuyên sâu về kỹ thuật của Odoo.










Tạo một Checklist cá nhân: 




Tạo người dùng → Gán quyền → Thêm công ty → Kiểm tra quyền → Cài app → Quan sát UI để đảm bảo không bỏ sót bước nào khi ôn tập.










Ghi nhớ tên module kỹ thuật (




account, stock, contacts, sale\_management) vì có thể xuất hiện trong các câu hỏi thi.




## 🔄 Luồng Hoạt Động Gợi Ý Cho Người Học

1. **Cài đặt hệ thống Odoo 18** (Docker hoặc mã nguồn)
2. **Khởi tạo dữ liệu công ty**: tạo công ty mặc định và công ty mới
3. **Tạo người dùng và phân quyền**
4. **Bật chế độ Developer Mode** để kiểm tra dữ liệu kỹ thuật
5. **Chuyển đổi giữa các công ty** và thử tạo dữ liệu
6. **Kiểm tra tính tách biệt và chia sẻ dữ liệu liên công ty**
7. **Cài đặt module cơ bản**: Contacts, Sales, Inventory
8. **Luyện tập các thao tác CRUD (Create, Read, Update, Delete)**
9. **Thực hiện bài quiz để củng cố kiến thức**

## ❓ Quiz ôn tập – Odoo Basics & Setup (Odoo 18)

### Câu 1: Developer Mode trong Odoo có tác dụng gì?
- A. Cho phép người dùng truy cập tất cả dữ liệu trong hệ thống  
- B. Bật các tính năng kỹ thuật như xem ID trường, cấu trúc view ✅  
- C. Thay đổi giao diện thành chế độ tối  
- D. Tự động cấp quyền Super Admin  

### Câu 2: Khi tạo một bản ghi mới (ví dụ: khách hàng), hệ thống sẽ:
- A. Gán bản ghi này cho tất cả các công ty  
- B. Không cho phép tạo bản ghi nếu không chọn công ty  
- C. Gán bản ghi cho công ty đang hoạt động hiện tại ✅  
- D. Tự động chia sẻ cho tất cả người dùng  

### Câu 3: Muốn một người dùng có thể thao tác trong nhiều công ty, ta cần:
- A. Tạo nhiều tài khoản cho từng công ty  
- B. Gán nhiều công ty cho user trong phần cấu hình ✅  
- C. Bật module HR  
- D. Không thể làm điều này  

### Câu 4: Module nào cần cài đặt để người dùng có thể xem và chỉnh sửa thông tin khách hàng?
- A. Sales  
- B. Accounting  
- C. Inventory  
- D. Contacts ✅  

### Câu 5: Trong Odoo, quyền truy cập được kiểm soát dựa trên:
- A. Loại dữ liệu người dùng tạo  
- B. Nhóm quyền (Groups) được gán cho người dùng ✅  
- C. Loại hệ điều hành người dùng sử dụng  
- D. Dung lượng bộ nhớ máy chủ  

### Câu 6: Khi người dùng tạo dữ liệu trong công ty A, nhưng đang chọn công ty B, điều gì xảy ra?
- A. Dữ liệu được lưu ở cả hai công ty  
- B. Dữ liệu được lưu trong công ty đang hoạt động (B) ✅  
- C. Hệ thống báo lỗi  
- D. Không thể tạo dữ liệu trong chế độ multi-company  
