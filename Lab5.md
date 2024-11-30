Để thiết kế các **hệ thống con (subsystems)** trong hệ thống **Payroll System** dựa trên nội dung được cung cấp và tham chiếu đến thiết kế **ca sử dụng (use case design)** từ bài Lab4, chúng ta cần chia hệ thống thành các phần chính dựa trên chức năng và mục tiêu hoạt động. Dưới đây là thiết kế chi tiết:

---

### **1. Các hệ thống con chính trong Payroll System**
Hệ thống Payroll sẽ được chia thành các hệ thống con sau:

1. **Employee Management Subsystem (Quản lý nhân viên):**
   - Quản lý thông tin nhân viên.
   - Lưu trữ và chỉnh sửa dữ liệu cá nhân (ID, tên, chức danh, hệ số lương, tài khoản ngân hàng).
   - Xử lý trạng thái hợp đồng (full-time, part-time, thử việc, nghỉ việc).

2. **Work Schedule Subsystem (Quản lý lịch làm việc):**
   - Thiết lập và quản lý lịch làm việc.
   - Theo dõi thời gian làm việc thực tế của nhân viên.
   - Tính số giờ làm thêm giờ (overtime) hoặc thiếu giờ (under-time).

3. **Payroll Calculation Subsystem (Tính lương):**
   - Áp dụng công thức tính lương.
   - Tính lương cơ bản, phụ cấp, và khấu trừ.
   - Tính thuế thu nhập cá nhân (PIT) và bảo hiểm xã hội (BHXH).

4. **Payment Subsystem (Thanh toán lương):**
   - Kết nối với ngân hàng hoặc hệ thống thanh toán.
   - Phát hành bảng lương (pay slip).
   - Ghi nhận trạng thái thanh toán.

5. **Reports and Analytics Subsystem (Báo cáo và phân tích):**
   - Báo cáo tổng hợp lương theo tháng, quý, năm.
   - Báo cáo chi tiết về nhân viên (lương cao nhất, thấp nhất).
   - Phân tích dữ liệu để dự đoán chi phí nhân sự.

6. **Admin and Security Subsystem (Quản trị và bảo mật):**
   - Quản lý tài khoản người dùng.
   - Phân quyền truy cập cho admin, nhân viên, và kế toán.
   - Ghi nhật ký (logs) các hoạt động truy cập và thay đổi dữ liệu.

---

### **2. Mô tả chi tiết từng hệ thống con**

#### **2.1. Employee Management Subsystem**
- **Actors:**
  - HR Staff (Nhân viên nhân sự).
  - Admin.
- **Chức năng:**
  - Thêm/sửa/xóa nhân viên.
  - Quản lý trạng thái hợp đồng lao động.
  - Lưu và truy xuất thông tin chi tiết.
- **Thành phần chính:**
  - Bảng `Employee` trong database (ID, Tên, Chức danh, Mức lương cơ bản, Ngày vào làm).
  - Module CRUD nhân viên.

---

#### **2.2. Work Schedule Subsystem**
- **Actors:**
  - Manager (Quản lý).
  - Nhân viên.
- **Chức năng:**
  - Quản lý bảng chấm công hàng ngày.
  - Tích hợp dữ liệu từ hệ thống điểm danh (biometric hoặc manual input).
  - Tính toán thời gian làm việc thực tế.
- **Thành phần chính:**
  - Bảng `WorkSchedule` (Ngày, Giờ bắt đầu, Giờ kết thúc, Overtime).
  - API kết nối thiết bị chấm công.

---

#### **2.3. Payroll Calculation Subsystem**
- **Actors:**
  - Kế toán.
  - Admin.
- **Chức năng:**
  - Tính lương dựa trên:
    - Lương cơ bản.
    - Thời gian làm thêm.
    - Phụ cấp (ăn trưa, đi lại).
    - Khấu trừ (bảo hiểm, thuế).
  - Công thức:
    ```
    Net Salary = Basic Salary + Overtime Payment + Allowances - Deductions (Tax + Insurance)
    ```
- **Thành phần chính:**
  - Module tính toán (Payroll Engine).
  - Bảng `PayrollDetails` (EmployeeID, Tổng lương, Thuế, Lương thực nhận).

---

#### **2.4. Payment Subsystem**
- **Actors:**
  - Admin.
  - Kế toán.
- **Chức năng:**
  - Kết nối với hệ thống ngân hàng để chuyển khoản.
  - Xuất phiếu lương (PDF, email).
  - Ghi nhận trạng thái thanh toán.
- **Thành phần chính:**
  - Module tích hợp ngân hàng.
  - Bảng `PaymentStatus` (EmployeeID, Kỳ thanh toán, Trạng thái).
  - Template phiếu lương.

---

#### **2.5. Reports and Analytics Subsystem**
- **Actors:**
  - Admin.
  - HR Manager.
- **Chức năng:**
  - Tổng hợp chi phí nhân sự.
  - Xem báo cáo chi tiết hoặc tổng quan.
  - Phân tích dựa trên AI hoặc Machine Learning (dự đoán chi phí nhân sự trong tương lai).
- **Thành phần chính:**
  - Bảng `Reports` (Loại báo cáo, Ngày tạo, Dữ liệu).
  - BI (Business Intelligence) Dashboard.

---

#### **2.6. Admin and Security Subsystem**
- **Actors:**
  - Admin.
- **Chức năng:**
  - Tạo, chỉnh sửa, xóa tài khoản.
  - Phân quyền theo vai trò (admin, nhân viên, kế toán).
  - Ghi nhật ký hoạt động (audit log).
- **Thành phần chính:**
  - Module quản lý tài khoản.
  - Bảng `UserAccounts` (Tên đăng nhập, Vai trò, Mật khẩu).
  - API xác thực và phân quyền.

---

### **3. Mô hình tổng quan kiến trúc**
Dựa trên các hệ thống con, ta có thể triển khai theo kiến trúc **3-tiers (3 lớp):**
1. **Presentation Layer (Lớp giao diện):**
   - Hệ thống giao diện web/app (Angular, React).
   - Màn hình cho từng chức năng (Quản lý nhân viên, Báo cáo...).

2. **Business Logic Layer (Lớp xử lý nghiệp vụ):**
   - Chứa các module cho từng hệ thống con.
   - Tích hợp và thực hiện logic nghiệp vụ.

3. **Data Layer (Lớp dữ liệu):**
   - Database quan hệ (SQL Server, MySQL).
   - Chứa các bảng: `Employee`, `WorkSchedule`, `PayrollDetails`, `PaymentStatus`, `Reports`.

---

### **4. Kết luận**
Hệ thống Payroll System có thể được thiết kế với sự phân chia rõ ràng giữa các hệ thống con. Mỗi hệ thống con sẽ đảm bảo tính độc lập, khả năng bảo trì cao, và dễ dàng tích hợp. Nếu anh cần thêm chi tiết như sơ đồ UML hoặc công cụ cụ thể để triển khai, hãy cho em biết nhé! 😊
