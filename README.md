# AcneCare - AI-Powered Acne Diagnosis & Treatment Platform

AcneCare là một nền tảng hỗ trợ chăm sóc da thông minh, kết hợp giữa sức mạnh của **Trí tuệ nhân tạo (AI)** để cung cấp giải pháp điều trị mụn cá nhân hóa. Hệ thống giúp người dùng tự chẩn đoán qua hình ảnh và nhận lộ trình điều trị khoa học.

---

## Công Nghệ Sử Dụng

### Backend
* **Java Spring Boot**: Framework chính xây dựng hệ thống RESTful API mạnh mẽ.
* **Spring Security & JWT**: Cơ chế xác thực và phân quyền người dùng (Stateless).
* **MySQL**: Hệ quản trị cơ sở dữ liệu lưu trữ thông tin người dùng, bệnh án và sản phẩm.
* **WebSocket (Spring Message)**: Xử lý tương tác thời gian thực (Chat, Notification).

### AI & Computer Vision
* **YOLOv8/v11**: Model được huấn luyện để nhận diện chính xác các loại mụn (Mụn viêm, mụn đầu đen, mụn ẩn...).
* **Roboflow**: Quản lý tập dữ liệu và tiền xử lý hình ảnh.
* **Recommendation Engine**: Thuật toán gợi ý sản phẩm dựa trên kết quả phân tích AI và loại da.

### Frontend & Tools
* **HTML5, CSS3, JavaScript**: Giao diện người dùng sinh động.
* **Postman**: Tài liệu hóa và kiểm thử API.
* **Git/GitHub**: Quản lý mã nguồn.

---

## Phân Quyền Người Dùng (Role-Based Access Control)

Hệ thống được thiết kế chặt chẽ với 4 phân quyền chính:

| Vai trò | Mô tả chức năng |
| :--- | :--- |
| **Patient** | Chụp ảnh chẩn đoán, xem gợi ý sản phẩm, đặt lịch tư vấn và chat với bác sĩ. |
| **Doctor** | Quản lý ca bệnh (Treatment Cases), tư vấn chuyên môn và thiết lập lộ trình điều trị. |
| **Brand** | Quản lý danh mục sản phẩm chăm sóc da và cập nhật thông tin thành phần. |
| **Admin** | Quản lý người dùng, phân quyền (Roles/Permissions) và kiểm duyệt nội dung. |

---

## Các Tính Năng Chính

### RESTful API Modules
* **Auth Service**: Đăng ký, đăng nhập, cấp phát JWT và quản lý Profile.
* **Social Hub**: Đăng bài viết chia sẻ kinh nghiệm, hệ thống Like và Comment bài viết.
* **Acne Detection**: API tiếp nhận hình ảnh, gọi model AI để phân tích và trả về kết quả chẩn đoán.
* **Product Recommendation**: Tự động gợi ý các sản phẩm phù hợp với từng loại mụn được phát hiện.

###  Real-time Features (WebSocket)
* **Instant Chat**: Nhắn tin trực tiếp giữa Bệnh nhân và Bác sĩ trong phòng chat riêng.
* **Live Notifications**: Nhận thông báo tức thì khi có phản hồi mới hoặc nhắc lịch hẹn.

---

##  Cơ Sở Dữ Liệu

Dự án sử dụng mô hình dữ liệu quan hệ (ERD) với các bảng thực thể quan trọng:
* `users`, `roles`, `permissions`: Quản lý bảo mật hệ thống.
* `acne_prediction`, `acne_prediction_details`: Lưu trữ dữ liệu phân tích từ AI.
* `skincare_products`, `treatment_plans`: Các sản phẩm chăm sóc da.
* `messages`, `chat_rooms`: Lưu trữ đoạn chat thời gian thực.

---
## Thành Viên Thực Hiện (Team Members)

Dự án được phát triển bởi các thành viên:

* Trần Bá Tòng
* Nguyễn Văn Tú Anh
* Nguyễn Tấn Phát
* Bùi Xuân Hào
* Trần Hải Đăng
