# 1. Sơ đồ Ngữ cảnh Hệ thống con

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
# 2. Ánh xạ lớp phân tích tới phần tử thiết kế

Bảng dưới đây thể hiện cách các lớp phân tích được ánh xạ sang các phần tử thiết kế của hệ thống. Điều này giúp làm rõ mối quan hệ giữa các khái niệm trong giai đoạn phân tích và các thành phần thực tế trong giai đoạn thiết kế.

| Lớp Phân Tích             | Phần Tử Thiết Kế                                     |
|---------------------------|------------------------------------------------------|
| **LoginForm**             | LoginForm                                            |
| **MaintainTimecardForm**  | MainEmployeeForm, TimecardForm, MainApplicationForm  |
| **TimecardController**    | TimecardController                                   |
| **SystemClockInterface**  | SystemClockInterface                                 |
| **PayrollController**     | PayrollController                                    |
| **Paycheck**              | Paycheck                                             |

**Ví dụ cụ thể:**

1. **LoginForm**  
   - **Phân tích**: Lớp này chịu trách nhiệm cho việc đăng nhập của nhân viên vào hệ thống.
   - **Thiết kế**: Được ánh xạ sang phần tử `LoginForm` trong giao diện người dùng, giúp nhân viên nhập tên đăng nhập và mật khẩu để truy cập vào hệ thống.

2. **MaintainTimecardForm**  
   - **Phân tích**: Lớp này xử lý việc nhập và quản lý thông tin thời gian làm việc của nhân viên.
   - **Thiết kế**: Được ánh xạ sang ba phần tử trong thiết kế:
     - `MainEmployeeForm`: Cung cấp giao diện để nhân viên truy cập thông tin cá nhân và các chức năng chính.
     - `TimecardForm`: Cho phép nhân viên nhập thời gian làm việc vào thẻ chấm công.
     - `MainApplicationForm`: Khung ứng dụng chính, từ đó nhân viên có thể truy cập các chức năng khác.

3. **TimecardController**  
   - **Phân tích**: Điều khiển các thao tác xử lý thẻ chấm công, như lưu trữ và kiểm tra thời gian làm việc.
   - **Thiết kế**: Được ánh xạ trực tiếp sang `TimecardController`, chịu trách nhiệm xử lý các thao tác liên quan đến thẻ chấm công trong hệ thống.

4. **SystemClockInterface**  
   - **Phân tích**: Lớp này cung cấp giao diện lấy thời gian từ hệ thống, đảm bảo các thao tác về thời gian luôn chính xác.
   - **Thiết kế**: Được ánh xạ thành `SystemClockInterface` trong thiết kế, cung cấp thời gian hệ thống cho các chức năng cần sử dụng.

5. **PayrollController**  
   - **Phân tích**: Quản lý quy trình tính lương và xử lý thanh toán cho nhân viên.
   - **Thiết kế**: Được ánh xạ trực tiếp sang `PayrollController`, xử lý tất cả các thao tác tính toán và quản lý dữ liệu thanh toán trong hệ thống.

6. **Paycheck**  
   - **Phân tích**: Lớp này đại diện cho chứng từ thanh toán lương của nhân viên.
   - **Thiết kế**: Được ánh xạ sang `Paycheck`, lưu trữ chi tiết thông tin về thanh toán lương, bao gồm số tiền và phương thức thanh toán.

---
# 3. Bảng ánh xạ Phần tử thiết kế vào Gói sở hữu

Dựa trên các yêu cầu của dự án, dưới đây là bảng ánh xạ các phần tử thiết kế vào các gói sở hữu phù hợp:

| Phần tử thiết kế           | "Gói sở hữu"                            |
|----------------------------|----------------------------------------|
| LoginForm                  | Middleware::Security::GUI Framework    |
| MainEmployeeForm           | Applications::Employee Activities      |
| TimecardForm               | Applications::Employee Activities      |
| MainApplicationForm        | Middleware::Security::GUI Framework    |
| TimecardController         | Applications::Payroll                  |
| SystemClockInterface       | Middleware::Utilities                  |
| PayrollController          | Applications::Payroll                  |
| Paycheck                   | Business Services::Payroll Artifacts   |
| EmployeeReportInterface    | Applications::Employee Reports         |
| PaymentProcessor           | Business Services::Payment Processing  |
| ProjectManagementInterface | Middleware::Integration::DB2 Interface |

Bảng này phân chia các phần tử thiết kế chính vào các gói hợp lý trong hệ thống. Các gói được cấu trúc để tách biệt các trách nhiệm, với các interface và controller được nhóm vào các lớp ứng dụng, dịch vụ kinh doanh, hoặc middleware tương ứng.

---

# 4. Các lớp kiến trúc và sự phụ thuộc của chúng

Các lớp kiến trúc cho hệ thống bảng lương có thể được thiết kế dựa trên chức năng và yêu cầu được chỉ định. Dưới đây là sơ đồ các lớp kiến trúc và sự phụ thuộc của chúng:

- **Lớp Giao diện người dùng (Presentation Layer)**: Lớp này xử lý giao diện người dùng, cho phép nhân viên tương tác với hệ thống (ví dụ: nhập thông tin thẻ giờ, truy cập báo cáo, và thay đổi các tùy chọn cá nhân).
  
- **Lớp Ứng dụng (Application Layer)**: Lớp này chứa logic nghiệp vụ để xử lý các chức năng bảng lương, bao gồm xử lý thẻ giờ, tính toán hoa hồng và tạo báo cáo.
  
- **Lớp Dịch vụ kinh doanh (Business Services Layer)**: Lớp này chịu trách nhiệm về các dịch vụ liên quan đến xử lý bảng lương, như tạo bảng lương và quản lý nhân viên.

- **Lớp Tích hợp (Integration Layer)**: Lớp này tạo điều kiện giao tiếp với các hệ thống bên ngoài, chẳng hạn như Cơ sở dữ liệu Quản lý Dự án DB2, thông qua các interface chuyên dụng.

- **Lớp Truy cập Dữ liệu (Data Access Layer)**: Lớp này quản lý việc lưu trữ dữ liệu, bao gồm truy cập dữ liệu nhân viên, lịch sử bảng lương và thông tin thẻ giờ.

Dưới đây là sơ đồ mô tả các lớp và sự phụ thuộc giữa chúng:

```mermaid
flowchart TD
    A[Lớp Giao diện người dùng] --> B[Lớp Ứng dụng]
    B --> C[Lớp Dịch vụ kinh doanh]
    B --> D[Lớp Tích hợp]
    D --> E[Lớp Truy cập Dữ liệu]



