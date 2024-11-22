
## 1. Nhập thông tin thời gian làm việc

**Lý do thiết kế:**
- **Participants**: Employee và Timekeeping System - Để phản ánh chính xác việc nhân viên nhập thời gian làm việc vào hệ thống chấm công.
- **Steps**:
  1. **Employee nhập giờ làm việc hàng ngày vào Timekeeping System** - Nhấn mạnh hành động nhập liệu của nhân viên.
  2. **Timekeeping System lưu giờ làm việc vào Database** - Đảm bảo thông tin được lưu trữ an toàn và chính xác.
  3. **Database xác nhận lưu trữ thành công với Timekeeping System** - Đảm bảo hệ thống biết rằng dữ liệu đã được lưu thành công.
  4. **Timekeeping System gửi thông báo xác nhận đến Employee** - Tạo sự yên tâm cho nhân viên về việc giờ làm việc đã được ghi nhận.

## 2. Nhập thông tin đơn hàng (dành cho nhân viên hưởng hoa hồng)

**Lý do thiết kế:**
- **Participants**: Commissioned Employee và Sales System - Để phản ánh việc nhân viên nhập thông tin đơn hàng vào hệ thống bán hàng.
- **Steps**:
  1. **Commissioned Employee nhập chi tiết đơn hàng vào Sales System** - Tăng cường sự chính xác trong việc ghi nhận bán hàng.
  2. **Sales System lưu chi tiết đơn hàng vào Database** - Đảm bảo rằng thông tin bán hàng được ghi nhận và theo dõi.
  3. **Database xác nhận lưu trữ thành công với Sales System** - Đảm bảo hệ thống biết rằng dữ liệu đã được lưu thành công.
  4. **Sales System gửi thông báo xác nhận đến Commissioned Employee** - Tạo sự yên tâm cho nhân viên về việc đơn hàng đã được ghi nhận.

## 3. Thay đổi phương thức nhận lương

**Lý do thiết kế:**
- **Participants**: Employee và Payroll System - Để phản ánh việc nhân viên thay đổi phương thức nhận lương.
- **Steps**:
  1. **Employee chọn phương thức nhận lương trong Payroll System** - Nhấn mạnh sự tự do lựa chọn của nhân viên.
  2. **Payroll System lưu phương thức nhận lương vào Database** - Đảm bảo thông tin được lưu trữ an toàn.
  3. **Database xác nhận lưu trữ thành công với Payroll System** - Đảm bảo hệ thống biết rằng dữ liệu đã được lưu thành công.
  4. **Payroll System gửi thông báo xác nhận đến Employee** - Tạo sự yên tâm cho nhân viên về phương thức nhận lương đã được cập nhật.

## 4. Xem báo cáo cá nhân

**Lý do thiết kế:**
- **Participants**: Employee và Reporting System - Để phản ánh việc nhân viên xem báo cáo cá nhân.
- **Steps**:
  1. **Employee yêu cầu báo cáo cá nhân từ Reporting System** - Nhấn mạnh việc nhân viên có thể kiểm tra thông tin cá nhân.
  2. **Reporting System truy xuất dữ liệu báo cáo từ Database** - Đảm bảo rằng thông tin được lấy từ cơ sở dữ liệu chính xác.
  3. **Database gửi dữ liệu báo cáo về Reporting System** - Đảm bảo thông tin được truyền lại cho hệ thống báo cáo.
  4. **Reporting System hiển thị báo cáo cá nhân cho Employee** - Tạo sự rõ ràng và minh bạch cho nhân viên.

## 5. Quản lý thông tin nhân viên

**Lý do thiết kế:**
- **Participants**: Payroll Administrator và Payroll System - Để phản ánh việc quản trị viên quản lý thông tin nhân viên.
- **Steps**:
  1. **Payroll Administrator thêm/cập nhật/xóa thông tin nhân viên trong Payroll System** - Nhấn mạnh quyền quản lý của quản trị viên.
  2. **Payroll System lưu thay đổi vào Database** - Đảm bảo rằng thông tin được lưu trữ và cập nhật chính xác.
  3. **Database xác nhận lưu trữ thành công với Payroll System** - Đảm bảo hệ thống biết rằng dữ liệu đã được lưu thành công.
  4. **Payroll System gửi thông báo xác nhận đến Payroll Administrator** - Tạo sự yên tâm cho quản trị viên về việc thay đổi đã được ghi nhận.

## 6. Xử lý thanh toán tự động

**Lý do thiết kế:**
- **Participants**: Payroll System và Bank - Để phản ánh quá trình xử lý thanh toán tự động.
- **Steps**:
  1. **Payroll System truy xuất dữ liệu giờ làm việc và lương từ Database** - Nhấn mạnh sự tự động hóa trong việc lấy thông tin.
  2. **Database gửi dữ liệu nhân viên về Payroll System** - Đảm bảo thông tin được truyền chính xác.
  3. **Payroll System tính toán lương** - Phản ánh quá trình xử lý và tính toán.
  4. **Payroll System gửi yêu cầu thanh toán tới Bank** - Nhấn mạnh sự kết nối giữa hệ thống trả lương và ngân hàng.
  5. **Bank xác nhận thanh toán đã được xử lý** - Đảm bảo rằng thanh toán đã được thực hiện thành công.
  6. **Payroll System cập nhật hồ sơ lương trong Database** - Đảm bảo rằng thông tin về thanh toán được ghi nhận.
  7. **Database xác nhận hồ sơ đã được cập nhật** - Đảm bảo hệ thống biết rằng dữ liệu đã được lưu thành công.

## 7. Truy xuất thông tin dự án

**Lý do thiết kế:**
- **Participants**: Payroll System và Project Management Database - Để phản ánh việc hệ thống truy xuất thông tin dự án cần thiết cho tính toán lương.
- **Steps**:
  1. **Payroll System yêu cầu mã charge từ Project Management Database** - Nhấn mạnh sự cần thiết của thông tin dự án cho việc tính toán lương.
  2. **Project Management Database gửi mã charge về Payroll System** - Đảm bảo thông tin được cung cấp đúng và đầy đủ.
  3. **Payroll System tính toán lương sử dụng mã charge** - Phản ánh quá trình sử dụng thông tin dự án để tính lương chính xác.
---
