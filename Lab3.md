# Sơ đồ Ngữ cảnh Hệ thống con

## 1. BankSystem
![Sơ đồ BankSystem](https://www.planttext.com/api/plantuml/png/R58xRiCm3Drz2i9JCkG2Hc5ayD027OAw5r1aeXKgVo9A0OoY9-kG8-KA4IEbbenEaXxVutkaVVszxCaAOrsl2wa54HoC6kmRdXoIXUy204nul3HGGMjz-ODHHsXMqCJIztd233qvePMTCynxMaSvv8wzUXXljhvs7bN75Vc9ygkzA-vurFmKZyHYxd68OQVmM2KJ_UWyeu9cT4UD2R4HbkFo4KOO9HB5bakCnOndRD6SbSHiFQ-As82FftI7TMAMSG9KBxEdgatiwjafdAvb5JLQi23SqknPwjskphzo1UMp63gDLFx3_EjR7e8Zq_OuTFpFt0000F__0m00)

Hệ thống con **BankSystem** quản lý tất cả các giao dịch ngân hàng và tích hợp với các dịch vụ ngân hàng bên ngoài. Chức năng của nó bao gồm quản lý chuyển khoản ngân hàng, chuyển khoản bảng lương, và thông tin tài khoản ngân hàng của nhân viên. BankSystem tương tác trực tiếp với Payroll System để tự động xử lý thanh toán và đảm bảo các giao dịch tài chính an toàn cho nhân viên.

### Các Thành phần chính:
- **Quản lý Tài khoản Ngân hàng**: Quản lý thông tin tài khoản ngân hàng của nhân viên cho các khoản chuyển khoản trực tiếp.
- **Xử lý Giao dịch**: Xử lý chuyển tiền và xác thực thanh toán.
- **Bảo mật và Tuân thủ**: Đảm bảo giao dịch tuân thủ các tiêu chuẩn ngân hàng.

---

## 2. PrintService
![Sơ đồ PrintService](https://www.planttext.com/api/plantuml/png/R58xRiCm3Drz2i9JCkG2Hc5ayD027OAw5r1aeXKgVo9A0OoY9-kG8-KA4IEbbenEaXxVutkaVVszxCaAOrsl2wa54HoC6kmRdXoIXUy204nul3HGGMjz-ODHHsXMqCJIztd233qvePMTCynxMaSvv8wzUXXljhvs7bN75Vc9ygkzA-vurFmKZyHYxd68OQVmM2KJ_UWyeu9cT4UD2R4HbkFo4KOO9HB5bakCnOndRD6SbSHiFQ-As82FftI7TMAMSG9KBxEdgatiwjafdAvb5JLQi23SqknPwjskphzo1UMp63gDLFx3_EjR7e8Zq_OuTFpFt0000F__0m00)

Hệ thống con **PrintService** quản lý tất cả các tác vụ liên quan đến in ấn, chẳng hạn như tạo phiếu lương, báo cáo và các tài liệu bảng lương khác cho nhân viên. Nó đảm bảo rằng các tài liệu được định dạng chính xác và có thể được in an toàn hoặc gửi qua email khi cần.

### Các Thành phần chính:
- **Tạo tài liệu**: Tạo các file có thể in được cho phiếu lương và hồ sơ nhân viên.
- **Định dạng và Xuất**: Đảm bảo tài liệu sẵn sàng để in, tuân thủ các tiêu chuẩn của công ty.
- **Phân phối**: Hỗ trợ gửi tài liệu in qua phương thức in ấn thực tế hoặc email.

---

## 3. Hệ thống con ProjectManagementDatabase
![Sơ đồ ProjectManagementDatabase](https://www.planttext.com/api/plantuml/png/X9913e8m44NtdA9nfGilO0n1O2696XDFCE04CRIOjYoCyMGkF99Ni2DLAQAk6dxcpxm_m-ro3PG6gMjUUba9Ih6rhFQOQNRo66E7vYE9sOHjj2n4tb9NmD7H7vrYqAJIGngARKV9KTiPCMeeIZKSlRkSFOiHxK3ckAfvYh9XoLfAFr17RGmpNjL2q_ogJiidGTF-5u1bN8A073aA2WOfA7GsioWKzQPdQXr-5xPTquxbkzi8Zqay_4n2RBR2OG-FwsVj5rVFG9FkUwxns7zTVy86Sr23FzNEaOmbgeHPg32-mDoT_gax0000__y30000)

Hệ thống con **ProjectManagementDatabase** chịu trách nhiệm lưu trữ và quản lý dữ liệu liên quan đến dự án, bao gồm mã charge và mã chi phí của dự án. Hệ thống con này không thể chỉnh sửa bởi Payroll System nhưng cung cấp thông tin quan trọng để theo dõi giờ làm và dự án.

### Các Thành phần chính:
- **Quản lý Mã Charge Dự án**: Duy trì danh sách các mã charge dự án đang hoạt động.
- **Phân bổ Dự án**: Đảm bảo rằng nhân viên có thể ghi nhận giờ làm việc theo từng dự án cụ thể.
- **Truy cập Chỉ-đọc**: Cho phép Payroll System truy xuất thông tin dự án mà không làm thay đổi dữ liệu.

---
## 2. Ánh xạ lớp phân tích tới phần tử thiết kế

Bảng dưới đây thể hiện cách các lớp phân tích được ánh xạ sang các phần tử thiết kế của hệ thống. Điều này giúp làm rõ mối quan hệ giữa các khái niệm trong giai đoạn phân tích và các thành phần thực tế trong giai đoạn thiết kế.

| Lớp Phân Tích             | Phần Tử Thiết Kế                                     |
|---------------------------|------------------------------------------------------|
| LoginForm                 | LoginForm                                            |
| MaintainTimecardForm      | MainEmployeeForm, TimecardForm, MainApplicationForm  |
| TimecardController        | TimecardController                                   |
| SystemClockInterface      | SystemClockInterface                                 |
| PayrollController         | PayrollController                                    |
| Paycheck                  | Paycheck                                             |

**Giải thích:**
- **LoginForm**: Được ánh xạ trực tiếp tới phần tử thiết kế cùng tên, thực hiện chức năng đăng nhập.
- **MaintainTimecardForm**: Tương ứng với các phần tử thiết kế như `MainEmployeeForm`, `TimecardForm`, và `MainApplicationForm`, chịu trách nhiệm về các thao tác trên thẻ chấm công của nhân viên.
- **TimecardController**: Điều khiển thao tác và luồng công việc liên quan đến thẻ chấm công, được ánh xạ tới `TimecardController` trong thiết kế.
- **SystemClockInterface**: Cung cấp giao diện làm việc với đồng hồ hệ thống, đảm bảo các thao tác về thời gian được xử lý chính xác.
- **PayrollController**: Điều khiển toàn bộ quá trình tính lương, đảm bảo các chức năng thanh toán được thực thi chính xác.
- **Paycheck**: Tương ứng với phần tử thiết kế `Paycheck`, đại diện cho chứng từ thanh toán của nhân viên.

---



