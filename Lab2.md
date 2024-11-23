### Phân tích Chi tiết Các Ca Sử Dụng trong Hệ thống Payroll System
  #### 1. Các Ca Sử Dụng Chính
  ##### 1.1. Employee Management
  * Mô tả: Quản lý thông tin nhân viên trong hệ thống.
  * Các bước thực hiện:
    * Thêm nhân viên mới:
      * Nhập thông tin: tên, ID, vị trí, mức lương.
      * Lưu vào cơ sở dữ liệu.
    * Cập nhật thông tin nhân viên:
      * Chọn nhân viên.
      * Cập nhật thông tin cần thiết.
      * Lưu thay đổi.
    * Xóa nhân viên:
      * Chọn nhân viên cần xóa.
      * Xác nhận xóa.
  ##### 1.2. Timecard Management
  * Mô tả: Quản lý thời gian làm việc của nhân viên.
  * Các bước thực hiện:
    * Nhập thời gian làm việc:
      * Chọn nhân viên.
      * Nhập ngày, giờ bắt đầu và giờ kết thúc.
      * Lưu thông tin.
    * Cập nhật thời gian làm việc:
      * Chọn thời gian đã nhập.
      * Cập nhật ngày, giờ.
      * Lưu thay đổi.
    * Xóa thời gian làm việc:
      * Chọn thời gian làm việc cần xóa.
      * Xác nhận xóa.
    * Xem thời gian làm việc:
      * Hiển thị danh sách thời gian làm việc của nhân viên.
##### 1.3. Payroll Processing
  * Mô tả: Tính toán và xử lý lương cho nhân viên.
  * Các bước thực hiện:
    * Tính lương:
      * Dựa trên thời gian làm việc và mức lương.
      * Lưu trữ thông tin lương:
      * Lưu vào cơ sở dữ liệu.
    * Phát lương:
      * Thực hiện chuyển tiền vào tài khoản của nhân viên.
##### 1.4. Reporting
  * Mô tả: Tạo báo cáo liên quan đến lương và thời gian làm việc.
  * Các bước thực hiện:  
    * Tạo báo cáo lương:
      * Tạo báo cáo theo tháng, quý.
    * Tạo báo cáo thời gian làm việc:
      * Tạo báo cáo tổng hợp thời gian làm việc của từng nhân viên.
#### 2. Ca Sử Dụng: Maintain Timecard
##### 2.1. Mô tả
* Ca sử dụng Maintain Timecard cho phép người quản lý (Manager) quản lý thời gian làm việc của nhân viên bằng cách thêm, cập nhật, xóa và xem thông tin thời gian.
##### 2.2. Actors
* Manager: Người quản lý có quyền chỉnh sửa thông tin thời gian làm việc.
* Employee: Nhân viên có thể xem thời gian làm việc của mình.
##### 2.3. Các bước thực hiện
  * Nhập Thời Gian Làm Việc:
    * Người quản lý chọn nhân viên từ danh sách.
    * Nhập thông tin thời gian làm việc: ngày, giờ bắt đầu, giờ kết thúc.
    *Nhấn nút lưu để lưu thông tin vào hệ thống.
  * Cập Nhật Thời Gian Làm Việc:
    * Người quản lý chọn thời gian đã nhập từ danh sách.
    * Nhập thông tin mới: ngày, giờ bắt đầu, giờ kết thúc.
    * Nhấn nút lưu để cập nhật thông tin.
  * Xóa Thời Gian Làm Việc:
    * Người quản lý chọn thời gian làm việc cần xóa từ danh sách.
    * Xác nhận việc xóa (hệ thống có thể yêu cầu xác nhận).
  * Xem Thời Gian Làm Việc:
    * Người quản lý có thể xem danh sách tất cả thời gian làm việc của nhân viên, bao gồm ngày, giờ vào và giờ ra.
#### 3. Sơ đồ UML cho Ca Sử Dụng Maintain Timecard
##### 3.1. Sơ đồ Ca Sử Dụng

![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aO9lObvYUceHbEUQMv2JNvcQoiLLMfoQd5YSgg3ac9AY49AP2-GLfIWf91OhX3eR8cH32r8IIrBH5HWX5BYavgHYAZ16A0ZBJ2s7InT3vKsukA0EKz3LjGDRYSetGkCRe_5Dk61UWGiufEQb0FqD0000__y30000)

