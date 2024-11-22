
## 1. Nhập thông tin thời gian làm việc

**Lý do thiết kế:**
- **Participants**: Employee và Timekeeping System - Để phản ánh chính xác việc nhân viên nhập thời gian làm việc vào hệ thống chấm công.
- **Steps**:
  1. **Employee nhập giờ làm việc hàng ngày vào Timekeeping System** - Nhấn mạnh hành động nhập liệu của nhân viên.
  2. **Timekeeping System lưu giờ làm việc vào Database** - Đảm bảo thông tin được lưu trữ an toàn và chính xác.
  3. **Database xác nhận lưu trữ thành công với Timekeeping System** - Đảm bảo hệ thống biết rằng dữ liệu đã được lưu thành công.
  4. **Timekeeping System gửi thông báo xác nhận đến Employee** - Tạo sự yên tâm cho nhân viên về việc giờ làm việc đã được ghi nhận.
  
![Diagram](https://www.planttext.com/api/plantuml/png/N91D3e9034RtFKN3dWkmC0GnqJKchYiKdS3Ca9cYuMmkF99Na17ymMMRzxv-wUDsJxsGarwt84fQneqHTdYmhb7cX5lREuyxKrkdIPGr05IATRZHNMi7PkX6MvMg8oCOxPNcXhaBQZ5uOHqXUGphQLpYEGaToVCBoZE0Toh6gnyfcKjLfDe1htErSwW6NoeuUPPWGHTUGYXsTATJa6SO_wMlhQcLqpFiHxzQv8xukzW7VZq3DNjF9uQKJHLU-0G00F__0m00)
## 2. Nhập thông tin đơn hàng (dành cho nhân viên hưởng hoa hồng)

**Lý do thiết kế:**
- **Participants**: Commissioned Employee và Sales System - Để phản ánh việc nhân viên nhập thông tin đơn hàng vào hệ thống bán hàng.
- **Steps**:
  1. **Commissioned Employee nhập chi tiết đơn hàng vào Sales System** - Tăng cường sự chính xác trong việc ghi nhận bán hàng.
  2. **Sales System lưu chi tiết đơn hàng vào Database** - Đảm bảo rằng thông tin bán hàng được ghi nhận và theo dõi.
  3. **Database xác nhận lưu trữ thành công với Sales System** - Đảm bảo hệ thống biết rằng dữ liệu đã được lưu thành công.
  4. **Sales System gửi thông báo xác nhận đến Commissioned Employee** - Tạo sự yên tâm cho nhân viên về việc đơn hàng đã được ghi nhận.

![Diagram](https://www.planttext.com/api/plantuml/png/N90z3i8m34PtdyBgpWKw85JQWOc14nXYKAJyLB51wjaOE19N84qBQjaIvtild_n-ldQYbFJk7QXLnzW5vOGdSYnuJ2QV3-4QaoUrCG3GHMF2QX-zjo9vn0OxtxiuC5T8WkFBTm1zLjkBxIaeLfFpD8YoBz4ocExhP4jAPv99s3O0IobkjakodXjBiSVIsB2ITGABs4YrJPt91w-o6j7Ctq7RuERVle_XQfEVqv9ni_PcO5dlHvI5eMSHkZ7iE9XnoHy0003__mC0)
## 3. Thay đổi phương thức nhận lương

**Lý do thiết kế:**
- **Participants**: Employee và Payroll System - Để phản ánh việc nhân viên thay đổi phương thức nhận lương.
- **Steps**:
  1. **Employee chọn phương thức nhận lương trong Payroll System** - Nhấn mạnh sự tự do lựa chọn của nhân viên.
  2. **Payroll System lưu phương thức nhận lương vào Database** - Đảm bảo thông tin được lưu trữ an toàn.
  3. **Database xác nhận lưu trữ thành công với Payroll System** - Đảm bảo hệ thống biết rằng dữ liệu đã được lưu thành công.
  4. **Payroll System gửi thông báo xác nhận đến Employee** - Tạo sự yên tâm cho nhân viên về phương thức nhận lương đã được cập nhật.

![Diagram](https://www.planttext.com/api/plantuml/png/P911Ri9034NtFeN5gfN81RgeK0XB9AISm2G6HinuHcCNAMTZqIFr2WoGL0fil_vx-lRVzNUbHjb-WWTpvXdN9v8Zuuw6m6AuPJl57e0wYnat8VauC4CgZEjSeb9Pb6wEtcCxg75O82cEqJEPjniosfFoezVK09CKg-yvzuKjU-uCqpWcFCRWHo3dbxWdEQDb4ZrmNgAJAd7MA9ymizorJLrSTE5NaqNinpdGr5YzBrX7ERWS9a2Bf7_r5sgwuHyWSr4AfKf7XXLBVt_n3G00__y30000)
## 4. Xem báo cáo cá nhân

**Lý do thiết kế:**
- **Participants**: Employee và Reporting System - Để phản ánh việc nhân viên xem báo cáo cá nhân.
- **Steps**:
  1. **Employee yêu cầu báo cáo cá nhân từ Reporting System** - Nhấn mạnh việc nhân viên có thể kiểm tra thông tin cá nhân.
  2. **Reporting System truy xuất dữ liệu báo cáo từ Database** - Đảm bảo rằng thông tin được lấy từ cơ sở dữ liệu chính xác.
  3. **Database gửi dữ liệu báo cáo về Reporting System** - Đảm bảo thông tin được truyền lại cho hệ thống báo cáo.
  4. **Reporting System hiển thị báo cáo cá nhân cho Employee** - Tạo sự rõ ràng và minh bạch cho nhân viên.

![Diagram](https://www.planttext.com/api/plantuml/png/P91B2i8m54NdMSN3UJVGWPGI7Oi5vy_sgO7yJ5wHhis1It8BfZzexIm9vznxoVVzAI9ZuDPemOermKNH2quKehEeuKpU1HO2QtO13iPhrn49dnHLAu-MOJSoojwXwYAJsG76IHmVrhX4nYj66Z1P2Z6dGhPVQNcwFLkA37wU4yOvIwgtP9d3aRX-J00qgGDkmPdXrBS9MKAsAQZ8DaldBpdnyxWSf8fUOxSPKwIC_lj-0000__y30000)
## 5. Quản lý thông tin nhân viên

**Lý do thiết kế:**
- **Participants**: Payroll Administrator và Payroll System - Để phản ánh việc quản trị viên quản lý thông tin nhân viên.
- **Steps**:
  1. **Payroll Administrator thêm/cập nhật/xóa thông tin nhân viên trong Payroll System** - Nhấn mạnh quyền quản lý của quản trị viên.
  2. **Payroll System lưu thay đổi vào Database** - Đảm bảo rằng thông tin được lưu trữ và cập nhật chính xác.
  3. **Database xác nhận lưu trữ thành công với Payroll System** - Đảm bảo hệ thống biết rằng dữ liệu đã được lưu thành công.
  4. **Payroll System gửi thông báo xác nhận đến Payroll Administrator** - Tạo sự yên tâm cho quản trị viên về việc thay đổi đã được ghi nhận.

![Diagram](https://www.planttext.com/api/plantuml/png/P90v3i8m44Lxds947z5J80YXe412oWc6U01BNYBFW9IpKN0ahe3Zi0NQh_SN_Vlrjc31A6TdbHYn15lqU2HOkzQ6ZWWs_X2YGp71AuMDX0YJ7NOnM0jBxOmtB16JF07aGL5jIZIDQT7B1wux5dAPUag3CgOh5DmZK-QgKgcS2CLyR9gb9Zqzjng5ffei2G6z9fkloIDN7rELCwZnGj2Sq1-9GGBePwcgIYZ-grR17qnqRmSdk_vDJhOyzOtdVd34dFvK2_AwF_a1003__mC0)
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

![Diagram](https://www.planttext.com/api/plantuml/png/T94zRiCm34PtdOB8dWju25B7w1mWo05OYKs4wWyYDVXi7NgaNg6INGTnasu2-HwfJ_h-_DgpO9RYdH8hZk2bIFGeLiCHnnoTWsEEcfXjk2YLAckrJHW4DWjm6bd8Rm1vSURAckunV4nCEwnR0mg-8TFK7dgbLcDWkwl53bv9z1N89nT78hZ6aXam661qc2sn6dhOLdXbTt2YojmqKtSzpl-Z7D3fub08qjnuD5gARdcRXdaAmggLdrtY4CExpVu6GffDCi_3dfEvMm-PTCpcluJBy5yAoYGRjQ_9sy_-0000__y30000)
## 7. Truy xuất thông tin dự án

**Lý do thiết kế:**
- **Participants**: Payroll System và Project Management Database - Để phản ánh việc hệ thống truy xuất thông tin dự án cần thiết cho tính toán lương.
- **Steps**:
  1. **Payroll System yêu cầu mã charge từ Project Management Database** - Nhấn mạnh sự cần thiết của thông tin dự án cho việc tính toán lương.
  2. **Project Management Database gửi mã charge về Payroll System** - Đảm bảo thông tin được cung cấp đúng và đầy đủ.
  3. **Payroll System tính toán lương sử dụng mã charge** - Phản ánh quá trình sử dụng thông tin dự án để tính lương chính xác.
  
![Diagram](https://www.planttext.com/api/plantuml/png/P90z3e9044RxFSM4dWjG6A8q5YH4JZ0k8wxP7zoTDU5i5Xx9AxW8XM3xpVjUPkRzV9M1qNCqMh1YJN0YzeeU18rtDv8CHtjntY0hPuKO4gka6j0oP0sEtcaDxHYOJ0OOO8dcP4CllXejzcGePHKodZ7GNAshlH0h0UIxRroahUwH0eEyeky9fEieY6a4-SJybWfeoNORyi-wRXnGowYH2ORbfXYKxTUICccdFtq0003__mC0)

---
