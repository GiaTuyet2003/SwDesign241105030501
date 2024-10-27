# 1. Phân tích kiến trúc
- Kiến trúc đề xuất: kiến trúc phân tầng
- Lý do lựa chọn:
  + Module hóa rõ ràng: Mỗi package phụ trách một phần việc riêng, giúp dễ bảo trì và mở rộng mà không ảnh hưởng đến phần khác.
  + Khi có lỗi hoặc thay đổi quy trình, chỉ cần chỉnh sửa ở package liên quan, giúp giảm rủi ro cho hệ thống.
  + Có thể tái sử dụng cho các hệ thống khác, tiết kiệm thời gian và chi phí.
  + Thêm tính năng mới dễ dàng mà không ảnh hưởng đến các phần khác.
  + Phân chia gọn gàng giúp hệ thống dễ quản lý, tránh rối khi phát triển thêm.
- Ý nghĩa từng thành phần trong kiến trúc:
  + Employee Management: Lưu thông tin nhân viên, quản lý chấm công và hoa hồng cho nhân viên bán hàng.
  + Payroll Processing: Tính toán lương theo giờ, lương cố định và hoa hồng; bao gồm lương tăng ca và tự động lên lịch thanh toán.
  + Payment Distribution: Cho phép lựa chọn các phương thức thanh toán gồm chuyển khoản, gửi phiếu lương qua bưu điện, hoặc nhận trực tiếp tại văn phòng.
  + Reporting: Cung cấp báo cáo cho nhân viên (giờ làm, thu nhập, nghỉ phép) và quản trị viên (quản lý nhân viên và thanh toán).
  + Payroll Administration: Quản lý thông tin nhân viên và các chế độ thanh toán, có quyền chỉnh sửa và tạo các báo cáo quản trị.
  + Legacy Integration: Kết nối với hệ thống DB2 hiện có để lấy mã dự án, không cập nhật dữ liệu trong đó.
- Biểu đồ package mô tả kiến trúc:
![Diagram](https://www.planttext.com/api/plantuml/png/Z9D1QzH068Rlyoi-zk1j_u2KfMuhjLXBnGWUl7nDncJePBBDp8X1F7degM3nBBgA50gBlNO7yP2o_sD-WN_1RsONccnBCPS9v7tVlD_p9N_Tdqrji3Qsb8pf8w6WhZHdHXZ9uObt9s0AxyvK3cC__q67N5mkfdGEOIoy-sZX-ioxpt20wH7cdB79yWO6Em8ho4Xpec0_NrnwzqL0rbwfV03l6T2LIjJwFk5hTVqfX5E3Knm0QjXvkSi-T5wI-FavbNdbtGna-tijUQ_AHGfFXIeWgr0LCM9ijL1Sw_Ymgqvgsq3gvxC9R7lt2sIePADd6mq-IbDoHODGXjTlC0q5sXcbcwgTAjXReecE5oYnRhPGfbQY4PLQDpwtWMSe3KaHHyu5gkXDHCcVeQ81IwvCRzwjnHIqTr_x3JSsGi53r7mqwXDOBQtRx02Rkf8omKF9kzBzelskuAreBvOj7fSJMJMSBuLKWjZ3S3Zg0uI7j42YBw1fBsp0Tsu7h2y9fbiyLiPJ0KNxhGGJEQu-hhi2-b3MtCStC4q79hlPMypeZXuI28i5KmUK3-YazR-Ze9y6iWxTzP0Ub_zFOPjSPU4l-mS00F__0m00).
# 2. Cơ chế phân tích
- Quản lý Thông tin Nhân viên: Lưu trữ thông tin chi tiết của 5,000 nhân viên, bao gồm phương thức thanh toán và loại lương (giờ công, tháng, hoa hồng).
- Nhập và Xử lý Thẻ Chấm Công: Nhân viên nhập thời gian làm việc, hệ thống ghi nhận để tính lương cho nhân viên theo giờ hoặc lương tháng.
- Xử lý Đơn Hàng Hoa Hồng: Lưu trữ đơn hàng để tính hoa hồng cho nhân viên có doanh số.
- Tính Lương: Tự động tính toán lương theo loại hình lương của từng nhân viên và áp dụng quy tắc làm thêm giờ.
- Chạy Tự động Lịch Thanh Toán: Tự động thực hiện thanh toán hàng tuần hoặc hàng tháng cho nhân viên theo lịch.
- Kết nối với Cơ sở Dữ liệu Dự án cũ: Truy xuất số hiệu công việc từ hệ thống hiện tại mà không thay đổi dữ liệu.
- Lựa chọn Phương thức Thanh toán: Hỗ trợ các tùy chọn như chuyển khoản, gửi bưu điện, hoặc nhận tại văn phòng.
- Báo cáo và Truy xuất Thông tin: Cung cấp báo cáo chi tiết về giờ làm việc, thu nhập năm, và thời gian nghỉ còn lại cho nhân viên và quản trị viên.
- Xác thực và Phân quyền: Đảm bảo nhân viên chỉ có thể xem và chỉnh sửa dữ liệu của họ, quản trị viên có quyền cao hơn.
- Sao lưu và Phục hồi Dữ liệu: Đảm bảo dữ liệu được sao lưu và phục hồi khi cần thiết.
- Bảo mật và Tuân thủ Pháp lý: Bảo vệ dữ liệu nhạy cảm của nhân viên, đảm bảo tuân thủ quy định về bảo mật.
# 3. Phân tích ca sử dụng Payment
- Ca sử dụng "Payment" là quy trình thanh toán lương cho nhân viên dựa trên giờ làm việc và phương thức thanh toán đã chọn.
1. Các Lớp Phân Tích
- Employee (Nhân viên):
  +Thuộc tính:-employeeID: Mã nhân viên
              -name: Tên nhân viên
              -paymentMethod: Phương thức thanh toán (chuyển khoản, bưu điện, nhận tại văn phòng)
- Payroll (Bảng lương):
  + Thuộc tính: -totalHours: Tổng số giờ làm việc
                -salary: Mức lương
                - commission: Hoa hồng (nếu có)
- PaymentProcessor (Xử lý thanh toán):
  + Thuộc tính:-paymentDate: Ngày thanh toán
               -paymentAmount: Số tiền thanh toán
- PaymentMethod (Phương thức thanh toán):
  + Thuộc tính:-methodType: Loại phương thức thanh toán (chuyển khoản, gửi qua bưu điện, nhận tại văn phòng)
2. Biểu đồ Sequence
![Diagram](https://www.planttext.com/api/plantuml/png/VD0nQiCm50RWNQVuoPuBU0Y1KBhKe253LqKHbK2MZFmo-0mvXGaTCWGoTB8f7GovXqwGAqI9uq1ewVh-x_tYwTpzp2iIWJQ5PKAI3tWfIkjhfLYPnaQQKZZ2X8iwU6id41NuhwXGZdZmKbML3uFv6-MAj5yF8cTiV0lJ6NY6rzWT34ZtN-u3P1oaZkrd0NaTC7vNo_xWDCZtZOCz7K_D8qlXGczYktTOnMwRciGe6Hz8dk4jTTOezR2QKEpsyjdcOzqon7O76zl6_BznQn_FoV2UBe7jlv_GNBdrzPyl0000__y30000)
3. Nhiệm vụ của từng lớp
- Employee: Gửi thông tin thời gian làm việc và yêu cầu thanh toán.
- Payroll: Tính toán lương dựa trên giờ làm việc và hoa hồng.
- PaymentProcessor: Nhận thông tin từ Payroll và xử lý thanh toán cho nhân viên.
-PaymentMethod: Cung cấp thông tin về phương thức thanh toán mà nhân viên đã chọn.
4. Quan hệ giữa các lớp
- Employee gửi thông tin cho Payroll.
- Payroll gửi yêu cầu thanh toán cho PaymentProcessor.
- PaymentProcessor sử dụng PaymentMethod để xác định cách thanh toán cho nhân viên.
5. Biểu đồ lớp
![Diagram](https://www.planttext.com/api/plantuml/png/T55DIiGm5Dxd58_PT-4s2nbX15q80tg1q6Pg8SahUI-B81v71C4BsCKivYGzmLp1T2Qj4yKi4jxtylsyv3ZiryJASx16r4OHmQtj3KQjuKL0MXNe3Dnl93ooxroR6qvP_GlgLRJQyOFcPsmaR2zByIgoHO8z6hCuCB8oTnWyITWPL9nnKaRvM68rMjiHTUXc_59sSjjwh3KH-aK_fzeeJdcdlSHlB0R7_ycTmozQzbG-nVvdzCHO7crrjOAgEXtpb1BQSVZiu5hCI7cfp2mX7Zu2rEFNUpXJolvVRWueWP8DDEFmvjh4N6lNJB_w3G00__y30000)
6. Giải thích biểu đồ lớp
- Employee (Nhân viên): Là người gửi thông tin giờ làm việc và nhận thanh toán.
- Payroll (Bảng lương): Tính toán số tiền mà nhân viên sẽ nhận.
- PaymentProcessor (Xử lý thanh toán): Thực hiện thanh toán cho nhân viên.
- PaymentMethod (Phương thức thanh toán): Xác định cách mà nhân viên muốn nhận lương.
# 4. Phân tích ca sử dụng Maintain Timecard
