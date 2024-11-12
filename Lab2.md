# Các chức năng chính của hệ thống Payroll System

### 1. Nhập thông tin thời gian làm việc
   - **Mục đích**: Nhân viên có thể tự nhập giờ làm việc hàng ngày của mình.
   - **Đối tượng sử dụng**: Nhân viên làm theo giờ và nhân viên hưởng lương.
   - **Chú ý**: Chỉ nhân viên mới có quyền chỉnh sửa giờ làm việc của chính mình.

### 2. Nhập thông tin đơn hàng (dành cho nhân viên hưởng hoa hồng)
   - **Mục đích**: Nhân viên hưởng hoa hồng có thể ghi nhận các đơn hàng bán được để tính hoa hồng.
   - **Đối tượng sử dụng**: Nhân viên nhận lương hoa hồng.
   - **Chú ý**: Chỉ nhân viên mới có quyền chỉnh sửa thông tin đơn hàng của mình.

### 3. Thay đổi phương thức nhận lương
   - **Mục đích**: Nhân viên có thể chọn cách nhận lương: nhận qua thư, chuyển khoản ngân hàng, hoặc nhận trực tiếp tại công ty.
   - **Đối tượng sử dụng**: Tất cả nhân viên.
   - **Chú ý**: Mỗi nhân viên chỉ chỉnh sửa được phương thức thanh toán của chính họ.

### 4. Xem báo cáo cá nhân
   - **Mục đích**: Nhân viên có thể xem các báo cáo cá nhân như: tổng giờ làm, số tiền đã nhận, thời gian nghỉ phép còn lại, v.v.
   - **Đối tượng sử dụng**: Tất cả nhân viên.
   - **Chú ý**: Nhân viên chỉ xem được báo cáo của chính mình.

### 5. Quản lý thông tin nhân viên
   - **Mục đích**: Payroll Administrator có thể thêm, xóa hoặc cập nhật thông tin nhân viên, bao gồm tên, địa chỉ, loại hình thanh toán (giờ, lương, hoa hồng).
   - **Đối tượng sử dụng**: Payroll Administrator.

### 6. Xử lý thanh toán tự động
   - **Mục đích**: Hệ thống tự động xử lý và phát lương cho nhân viên mỗi tuần vào thứ Sáu (cho nhân viên làm theo giờ) và vào ngày làm việc cuối tháng (cho nhân viên hưởng lương).
   - **Tần suất**: Tự động chạy hàng tuần và cuối tháng.

### 7. Truy xuất thông tin dự án
   - **Mục đích**: Hệ thống truy cập cơ sở dữ liệu quản lý dự án (chỉ đọc) để lấy mã charge cần thiết cho việc tính toán lương.
   - **Chú ý**: Hệ thống chỉ truy cập thông tin, không thay đổi gì.


# Viết code Java mô phỏng ca sử dụng Maintain Timecard.
```java
import java.time.LocalDate;
import java.util.ArrayList;
import java.util.List;

// Lớp Employee chứa thông tin nhân viên và danh sách thẻ thời gian
class Employee {
    private int employeeId;
    private String name;
    private List<Timecard> timecards;

    public Employee(int employeeId, String name) {
        this.employeeId = employeeId;
        this.name = name;
        this.timecards = new ArrayList<>();
    }

    public int getEmployeeId() {
        return employeeId;
    }

    public String getName() {
        return name;
    }

    public List<Timecard> getTimecards() {
        return timecards;
    }

    public void addTimecard(Timecard timecard) {
        timecards.add(timecard);
    }

    public void displayTimecards() {
        System.out.println("Timecards for employee: " + name);
        for (Timecard timecard : timecards) {
            System.out.println(timecard);
        }
    }
}

// Lớp Timecard lưu thông tin về ngày làm việc, số giờ làm và mã charge
class Timecard {
    private LocalDate date;
    private double hoursWorked;
    private String chargeNumber;

    public Timecard(LocalDate date, double hoursWorked, String chargeNumber) {
        this.date = date;
        this.hoursWorked = hoursWorked;
        this.chargeNumber = chargeNumber;
    }

    @Override
    public String toString() {
        return "Date: " + date + ", Hours Worked: " + hoursWorked + ", Charge Number: " + chargeNumber;
    }
}

// Lớp PayrollSystem quản lý nhân viên và thẻ thời gian
class PayrollSystem {
    private List<Employee> employees;

    public PayrollSystem() {
        employees = new ArrayList<>();
    }

    public void addEmployee(Employee employee) {
        employees.add(employee);
    }

    public Employee findEmployeeById(int employeeId) {
        for (Employee employee : employees) {
            if (employee.getEmployeeId() == employeeId) {
                return employee;
            }
        }
        return null;
    }

    public void addTimecard(int employeeId, Timecard timecard) {
        Employee employee = findEmployeeById(employeeId);
        if (employee != null) {
            employee.addTimecard(timecard);
            System.out.println("Timecard added for employee ID: " + employeeId);
        } else {
            System.out.println("Employee with ID " + employeeId + " not found.");
        }
    }

    public void displayEmployeeTimecards(int employeeId) {
        Employee employee = findEmployeeById(employeeId);
        if (employee != null) {
            employee.displayTimecards();
        } else {
            System.out.println("Employee with ID " + employeeId + " not found.");
        }
    }
}

// Lớp chính chạy thử chương trình
public class Main {
    public static void main(String[] args) {
        PayrollSystem payrollSystem = new PayrollSystem();

        Employee emp1 = new Employee(1, "John Doe");
        Employee emp2 = new Employee(2, "Jane Smith");

        payrollSystem.addEmployee(emp1);
        payrollSystem.addEmployee(emp2);

        Timecard timecard1 = new Timecard(LocalDate.of(2024, 11, 1), 8.0, "CHG001");
        Timecard timecard2 = new Timecard(LocalDate.of(2024, 11, 2), 9.0, "CHG002");

        payrollSystem.addTimecard(1, timecard1);
        payrollSystem.addTimecard(1, timecard2);

        payrollSystem.displayEmployeeTimecards(1);
        payrollSystem.displayEmployeeTimecards(3);
    }
}

---

