### **1. Các hệ thống con chính trong Payroll System**

#### 1. **Employee Management Subsystem (Quản lý nhân viên)**

- **Chức năng**:
  - Quản lý thông tin nhân viên.
  - Lưu trữ và chỉnh sửa dữ liệu cá nhân (ID, tên, chức danh, hệ số lương, tài khoản ngân hàng).
  - Xử lý trạng thái hợp đồng (full-time, part-time, thử việc, nghỉ việc).

- **Sơ đồ Use Case**:
  
  ![Use Case Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aOAIHv12S4bYMfgIGcAnWaSGJDWn9JSp3om6Pd5n0TNfwjefQ3Ycf2YuvXRav5Ucfch2HKCBKX9BKh58kAJcf6AL2CjCBOSBAxYabYHcvXHhSd61hSDc5P84Xcr8SXWM8idXiDCXDIy552800000__y30000)

- **Sơ đồ Class**:
  
 ![Class Diagram](https://www.planttext.com/api/plantuml/png/X50x3i8m3Drx2ekT2sH0_0K32D4JMAbRHIGEIjm18Kx6m96u0gI5bWNOtaVFVdhtwsqS1OFKpcRQOeomS4VhJqHmpW1WFLUmPg6AGg9RTAGWbs2uIdpden7Z-LFBqM8upJoLfT66M1GihKT9tXJvCD7Qrqdj8pFF4b1BBYXrx9nBzkgqsZ-TicmhDV1NhousAPpXDjJ0Fw7tb-5mrA-WOB11nehY86llVRN7n4NQyG400F__0m00)

- **Sơ đồ Sequence**:
  
  ![Sequence Diagram](https://www.planttext.com/api/plantuml/png/F8yz3eCm34RtdC9Yvm8C5QAfn0mdS8aZHSeFnKubpjQXH-eL6YXbi_o-xyd-lDuj2owIWrSuILgWwWSO1Qsj01dwGSq5kydD60MgSMMXiACoAeE2TsI2wXPcdrOYqCTgp-XEgUAhBrkwWO4UcLX04g0nG4T75RXbTDV0Y4yw0HWIT9wLxg3-IwufMhS459VYhrb8FpHmdb3SP83pD16ppTwlggLejX-_0000__y30000)

#### 2. **Work Schedule Subsystem (Quản lý lịch làm việc)**

- **Chức năng**:
  - Thiết lập và quản lý lịch làm việc.
  - Theo dõi thời gian làm việc thực tế của nhân viên.
  - Tính số giờ làm thêm giờ (overtime) hoặc thiếu giờ (under-time).

- **Sơ đồ Use Case**:
  
  ![Use Case Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aOAIRs9UOdfgaP92Oh42b0sJSiqjoCclJ4q5oy4uN5nGLGgwkdOA6iv5gOabgGhX-KNP2i796QaffJcfcgXAGWjIu4eyyakBYj7adHDpaajpG4hyorABIZ9pWGOufEQbW1m90000__y30000)

- **Sơ đồ Class**:
  
  ![Class Diagram](https://www.planttext.com/api/plantuml/png/V91D2i8m48NtESNGVI-GXIYqnIxyWHPSXpRKO9f8CXL4F9aBZ-GLp6YhPkDcoFloPjumZzjzxb4u77hD6YsyXvrrXwhPotRG4YuC03A1ahyggOhijUe3eaeeDsqCQej2B-tWF8T2Mu44DoVfC1WYVcLZx4eOqKdtJXn5cN4e3Shm9BeMb56XKwRxDkRzKTkp77UTrB_MeBVMArJM_8wRDaZJMNm43id2UzKPdx3eWvoV-E0gh4lON9gMhla4003__mC0)

- **Sơ đồ Sequence**:
  
  ![Sequence Diagram](https://www.planttext.com/api/plantuml/png/F8yn3i8m34NtdCBgtWjqGAXaOUZKWTaaReb8aofsa7es1ex45KWBPOlytljIti_NaGMJvCahD18JL1q672bLW0pTcDHSi3DknY1GzGiBJHihJsLHy8fCK5rYklVcHZPx0lqxRvvkbIexK1_Mf85pcBC0xwubGUTP5ROgkcsWnmVz1QLRgFVs5CFWqeJYOlWMXPJnqknx9X4AMU1i334FsVj57IdOzOiV0000__y30000)

#### 3. **Payroll Calculation Subsystem (Tính lương)**

- **Chức năng**:
  - Áp dụng công thức tính lương.
  - Tính lương cơ bản, phụ cấp, và khấu trừ.
  - Tính thuế thu nhập cá nhân (PIT) và bảo hiểm xã hội (BHXH).

- **Sơ đồ Use Case**:
  
  ![Use Case Diagram](https://www.planttext.com/api/plantuml/png/X8z12W8n34NtSuemAsSnLv2fkd6j5mX95mET59eKzMopy4XUmHR12eBkahnF7l-ntYSrJ9QNq25PJD0xefZ5KAm7L2Zhc_0oo-jOfwuh3CPn2viz1ie1pSCETIOuOS1q6rh0COCB8LvGoEi7E7ZEP736grT0OJYAvbHJG_bVDNyCBVBbQEYNPVB2jVuJ003__mC0)

- **Sơ đồ Class**:
  
  ![Class Diagram](https://www.planttext.com/api/plantuml/png/V9112i8m44NtESNGVI-GXLIjGZUbs1CCwRG4feaaKwI89tFXaRo212tMZSl_OERn__F-AA9Wa6baPHXZX0Rdu9dXgW3WC9xPpqHLgQ5oGWE5X7SOhMcHCSmQZknH4jqo-miwGt45I-ec8zQxDQn9VgzlwcDVX7_rDOwaePLWtP1ouwDDYZLx_zzxwdjhB3bPgPQAURxv2ZLa9-efK2gGgO9SbqPv0G00__y30000)

- **Sơ đồ Sequence**:
  
  ![Sequence Diagram](https://www.planttext.com/api/plantuml/png/L90nhW8n34JxdCBQdWjG8FX0Z-049ckaIDvaYHsad8tY7-bVuJk1bQ1BPfvcHlvx_cv5CMkPsA7Nb67OUPzAL8mw00hOryr611zcqs2uL56QkcTFDwBY5OLWE4upfqe4XxVK6LCFFn_K2MjEpD-GYGOvwuBLfiMkuKptGg8Wo9WhU6HV63MawCnlM4zkeEP03m9Q-aTI32mBryFNS45ZbXWQONuDSTs6rTAxJ_4MylJHP8uDQm5VIon2YlSaSYlCrMqfZksC_m000F__0m00)

#### 4. **Payment Subsystem (Thanh toán lương)**

- **Chức năng**:
  - Kết nối với ngân hàng hoặc hệ thống thanh toán.
  - Phát hành bảng lương (pay slip).
  - Ghi nhận trạng thái thanh toán.

- **Sơ đồ Use Case**:

  ![Use Case Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aOAIOqfkPfwIGcAn0fW55qvEpY_DAqdCAu789ITpSO4LAEZgsYbe11Jb9wSM5oi495OMvUVaWEZSrBmIJMGrxgbvgKM99QaWIONWdCm25DdGWXIe74YZGd19OabfiIRGakHaGbR0L62p02Q7mtY7rBmKaES10000__y30000)
  
- **Sơ đồ Class**:

  ![Class Diagram](https://www.planttext.com/api/plantuml/png/P8z12i8m44NtESNGVI-GXLYfGXTAGJt068TQR2QIJ1P5F9aBZ-GLDDXAqTNm_ypynt_U7_CWw2NQJfaEGu0QUqiiS5K0ewXA3HKBDUIJkxINplL4F_RQiPmqb2YKP65TPD6mwXnAChQ24eD-Jzzoesvg82wGpqLTVOWxZnpGIEiunG-tASwObBU9za1-kfXy_1F6Dda--t8qPFj08LDpucCg_W800F__0m00)

- **Sơ đồ Sequence**:

  ![Sequence Diagram](https://www.planttext.com/api/plantuml/png/P90xZiCm34Hxde9mdmkuMEJNR1VaSm2kJ0D6R4aHgS9dIx57sYiifSG8WdJapF29rD_zTorAIVCq0ZaD2PkDSo5x9QyDag2r42qnk26QXirf5kMfUbP2Hqe_98pDWUQ9BR5_AZLYudxx3jYIl-Bcy5tzqW3O8xZwAhmMZtpBB8hnWGCJYrU2BPuJUUavOPzz9r1HgsMocdR543owuFiXJLIQ1L5tQV4IRMTU-6ZtQnQevekr-vWtnzPiSJapfk1OX3kKx4hLvt6SOSs-Ax_v3m00__y30000)

---

Các hệ thống con này có thể tích hợp với nhau để cung cấp một hệ thống quản lý lương đầy đủ và hiệu quả, giúp các nhà quản lý tính toán và thanh toán lương cho nhân viên một cách chính xác và minh bạch.
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
