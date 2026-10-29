# HCM_KS26_CNTT2_IT108_Session14_Ex09
## Phần 1. Phân tích bài toán

### 1. Đầu vào và đầu ra

**Đầu vào:**

- Ban Kỹ thuật (3 người): Quản lý code và API.
- Ban Thiết kế (2 người): Thiết kế giao diện.
- Ban Kinh doanh (2 người): Quản lý kế hoạch kinh doanh.
- Nhà đầu tư (1 người): Xem tài liệu dự án.

**Đầu ra:**

- Thư mục Google Drive được sắp xếp rõ ràng.
- Mỗi người chỉ được truy cập tài liệu cần thiết.
- Tài liệu quan trọng được lưu phiên bản ít nhất 30 ngày.
- Nhà đầu tư hết quyền sau 14 ngày.

### 2. Cấu trúc thư mục

**CampusPay**

- **Ban_Ky_Thuat:** Code, API.
- **Ban_Thiet_Ke:** Hình ảnh, giao diện.
- **Ban_Kinh_Doanh:** Business Plan.
- **Tai_Lieu_Chung:** Slide Pitch, tài liệu chung.
- **Bao_Mat:** Dữ liệu khách hàng, thông tin nhạy cảm.

### 3. Các bước thực hiện

1. Tạo thư mục CampusPay trên Google Drive.
2. Tạo 5 thư mục con và đặt tên.
3. Cấp quyền theo từng ban.
4. Đặt tài liệu mật ở chế độ Restricted.
5. Kiểm tra quyền và lịch sử phiên bản.
6. Thu hồi quyền khi thành viên nghỉ việc.
##  Phần 2. Triển khai và chống lỗi

### 4. Bảng phân quyền

| Tài liệu | Ban KT | Ban TK | Ban KD | Nhà đầu tư | Bảo mật |
|---|---|---|---|---|---|
| Code, API | Sửa | Xem | Không | Không | Restricted |
| Thiết kế UI | Xem | Sửa | Xem | Không | Restricted |
| Business Plan | Xem | Không | Sửa | Xem | Restricted |
| Slide Pitch | Xem | Sửa | Sửa | Xem | Hạn 14 ngày |
| Dữ liệu mật | Người được chỉ định | Không | Không | Không | Restricted |

### 5. Giải quyết 3 tình huống

**Tình huống 1:** Ban Kỹ thuật muốn đọc Business Plan.

- Cấp quyền Viewer để chỉ xem, không sửa được nội dung.

**Tình huống 2:** Nhà đầu tư muốn tải Slide Pitch.

- Cấp Viewer, cho phép tải PDF nhưng không cấp quyền chỉnh sửa. Không tắt tính năng tải xuống. Đặt hạn truy cập 14 ngày.

**Tình huống 3:** Thành viên nghỉ việc.

- Vào Manage Access → Remove Access, xóa khỏi các nhóm chia sẻ và thu hồi quyền tài khoản liên quan.
