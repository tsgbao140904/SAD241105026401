### Thiết kế Ca Sử Dụng trong Hệ thống Payroll System

#### 1. Các Ca Sử Dụng Chính
##### 1.1. Đăng Nhập (Login)
* Mô tả: Ca sử dụng này cho phép người dùng (nhân viên hoặc quản lý) đăng nhập vào hệ thống.
* Các bước thực hiện:
  - Giao diện đăng nhập: Người dùng mở giao diện đăng nhập.
  - Nhập thông tin: Nhập tên người dùng và mật khẩu.
  - Xác thực: Hệ thống kiểm tra tính hợp lệ của thông tin.
    * Nếu thông tin hợp lệ:
      * Chuyển đến trang chính (Dashboard).
    * Nếu không hợp lệ:
      * Hiển thị thông báo lỗi và yêu cầu nhập lại thông tin.
  4. Quên mật khẩu: Cung cấp tùy chọn "Quên mật khẩu" để lấy lại quyền truy cập.
* Lý do: Bảo mật thông tin người dùng và quản lý quyền truy cập vào hệ thống.

* Bản vẽ UML - Ca Sử Dụng Đăng Nhập
  
  ![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aK9eSMeH5uXGqBLJqF39Jy_Cq-I2qWgw837VnCmyXO34z5GqSTUY8g1-tzJYOamvj_oYzFmIeAxYulByeXHDBeVKl1IWfG00003__mC0)

##### 1.2. Quản Lý Thời Gian Làm Việc (Maintain Timecard)
* Mô tả: Ca sử dụng này cho phép người quản lý thêm, cập nhật, xóa và xem thông tin thời gian làm việc của nhân viên.
* Các bước thực hiện:
  - Chọn chức năng: Người quản lý chọn "Quản lý thời gian làm việc".
  - Hiển thị danh sách nhân viên: Hệ thống hiển thị danh sách tất cả nhân viên cùng thông tin thời gian làm việc.
  - Thao tác với thời gian làm việc:
    * Thêm thời gian làm việc:
      * Nhập thông tin: ngày, giờ bắt đầu, giờ kết thúc.
      * Nhấn "Lưu" để ghi lại thông tin.
    * Cập nhật thời gian làm việc:
      * Chọn thời gian đã nhập từ danh sách.
      * Nhập thông tin mới và nhấn "Cập nhật".
    * Xóa thời gian làm việc:
      * Chọn thời gian cần xóa.
      * Xác nhận việc xóa.
- Xem thông tin: Cho phép người quản lý xem chi tiết thời gian làm việc của từng nhân viên.
- Hiển thị thông báo: Hệ thống hiển thị thông báo thành công hoặc lỗi sau khi thực hiện thao tác.
* Lý do: Đảm bảo theo dõi chính xác thời gian làm việc để tính lương chính xác cho nhân viên.

* Bản vẽ UML - Ca Sử Dụng Quản Lý Thời Gian Làm Việc

![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aO9lObvYUceH5vHMqBLJq82m5K8oSrEJ4ujIDBamH1HqGUeSKr88AmejI4ai8S8mbzISL6BKXMMcbYEfSaZDIm7w1W000F__0m00)

##### 1.3. Xử Lý Lương (Run Payroll)
* Mô tả: Ca sử dụng này cho phép hệ thống tính toán và xử lý lương cho nhân viên dựa trên thời gian làm việc và mức lương đã thiết lập.
* Các bước thực hiện:
  - Chọn chức năng: Người quản lý chọn "Xử lý lương".
  - Kiểm tra ngày phát lương: Hệ thống kiểm tra xem có phải là ngày phát lương hay không.
  - Nếu là ngày phát lương:
    * Lấy thông tin thời gian làm việc và mức lương cho từng nhân viên.
    * Tính toán lương cho từng nhân viên dựa trên công thức:
      * Lương = Giờ làm việc x Mức lương theo giờ.
    * Lưu thông tin lương vào cơ sở dữ liệu.
    * Cung cấp tùy chọn phát lương (chuyển khoản hoặc in phiếu lương).
  - Hiển thị thông báo: Hệ thống hiển thị thông báo thành công hoặc lỗi sau khi xử lý lương.
* Lý do: Đảm bảo quy trình thanh toán diễn ra suôn sẻ và chính xác, giảm thiểu sai sót trong việc tính toán.

* Bản vẽ UML - Ca Sử Dụng Xử Lý Lương

![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aO9lObvYUceH5vHMqBLJq0WgpLC8IAmioi_9qUH2uIdeWkITCrAJiq5YAOcLs1KavYINvYIMf2e49-Oa5c5Nv99PN5AKcLGAL1K0CiSXDIy5w2u00000__y30000)
  
