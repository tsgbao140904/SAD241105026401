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

##### 1.4. Tạo Báo Cáo Lương (Generate Payroll Report)
* Mô tả: Ca sử dụng này cho phép người quản lý tạo các báo cáo liên quan đến lương và thời gian làm việc.
* Các bước thực hiện:
  - Chọn chức năng: Người quản lý chọn "Tạo báo cáo".
  - Chọn loại báo cáo: Cung cấp tùy chọn cho người quản lý chọn loại báo cáo cần tạo (theo tháng, quý, hoặc theo nhân viên).
  - Nhấn "Tạo báo cáo": Hệ thống sẽ xử lý việc tạo báo cáo.
  - Hiển thị báo cáo: Hệ thống hiển thị báo cáo trên màn hình hoặc cho phép tải xuống dưới dạng file.
  - Xem báo cáo: Người quản lý có thể xem chi tiết báo cáo và in nếu cần.
* Lý do: Cung cấp thông tin cho quản lý đánh giá hiệu suất làm việc và chi phí nhân sự.

* Bản vẽ UML - Ca Sử Dụng Tạo Báo Cáo Lương

![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aO9lObvYUceH5vHMqBLJq71FpKijIYn9LGX8h2pApybH24ejo2ygqUJ2AQEW2z8Nd9gJcbm25LC8gIn89QZ59REu82Un4cw3GsfU2j1n00000F__0m00)

#### 2. Mô Hình Ca Sử Dụng Tổng Thể

* Bản vẽ UML - Mô Hình Ca Sử Dụng Tổng Thể
  
![Diagram](https://www.planttext.com/api/plantuml/png/Z9913e8m44NtFKMNik0A1YE96qsCWFkndM1ZBMGeCPpDXKVo2hOM3KGDxgR_lywVJdg_tfB60jdsh1a8Mn4l6gI-t821qfsOrtWyvxDrLIeJiTvuIg7ckJgZ099ZSzSQleMEAgt7nWeD4bXykNo7TKKsOgpFu75ehdo34YFs4HI8XPI3x1zGKKkVDScbgF4VRg_mCgI6pmp4yeZYv3K9tNS0j6Yrdoe33VGTIbLZIHtQi2U7_5fRm3Ctlh2znlEkniahBg7MqBtNdw2HxYyy0000__y30000)

#### 3. Thiết Kế Kiến Trúc và Cấu Trúc Dữ Liệu
##### 3.1. Kiến trúc Hệ thống
  * Frontend: Giao diện người dùng với các chức năng như đăng nhập, quản lý thời gian làm việc, xử lý lương và tạo báo cáo.
  * Backend: Xử lý logic ứng dụng, bao gồm xác thực người dùng, tính toán lương và quản lý dữ liệu.
  * Cơ sở dữ liệu: Lưu trữ thông tin người dùng, thời gian làm việc và thông tin lương.
##### 3.2. Cấu trúc dữ liệu
* Bảng Nhân Viên:
  * employee_id: int
  * name: String
  * position: String
  * hourly_rate: double
  * password: String (đã mã hóa)
* Bảng Thời Gian Làm Việc:
  * timecard_id: int
  * employee_id: int (khóa ngoại)
  * date: Date
  * start_time: Time
  * end_time: Time
* Bảng Lương:
  * payroll_id: int
  * employee_id: int (khóa ngoại)
  * pay_period: String
  * total_hours: double
  * total_pay: double
#### 4. Mã Nguồn Java
##### 4.1. Lớp Nhân Viên (Employee)

![Diagram](https://www.planttext.com/api/plantuml/png/R95D3e8m48Ntd6AMaE05MB4XqOqXUe9YHsnIEgGj668ycGkFv1KifF9hbszUvtilytczKsEPjaqbWujana1MrP8wH7W4uDuEq0i7de1GrgkALPZ0sMgXIY_LP8GLf5RoZHejknEppi-fAIJ-_0vt9yr7_w33c21SaUC5DDxmuZ-eU4E9FAL4cutxmsZg1c0MerKAvsn9y6dBqONg_yzA3_f-3DDFPyq1MjJYskK-MIXKtTXydJE1WaWYKy4pI55nTw8l0000__y30000)

##### 4.2. Lớp Thời Gian Làm Việc (Timecard)

![Diagram](https://www.planttext.com/api/plantuml/png/R95D3i8W48NtFSKismGlq5KNccZYpYQk4IQcaHR3py8OJ-R28ta5WG99iQo6zy6yD_1zVpfjg39s51KJL6leXn4PLHoU5RYr0HE50szXc4nKSRmB-K1SgfmQRE4e6HLRLqOrEFY-4VaojPbu2GA1dACk_4bfJKfNicf8LhoQwEMsp0ftTI-jqcUfRiZhfWKkxKLWF7H5q-SedgQn0zhbK7_8P_BYyba2EgMWcUUtcRlEaPVqLNLk5FTZFm000F__0m00)

##### 4.3. Lớp Xử Lý Lương (PayrollProcessor)

![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niK90OcLHVavEG55-ScfnSNwHGZMN0X3eAfHavgOc9nQb55if-6GMbzY4GFbsKFdKt8AS_ChKL9YyAvHlnmLMe81XiWPE4tLm6wO9DQm0OWhKJ0rDAuMo_CmKhbekXzIy5A1l00000F__0m00)

##### 4.4. Lớp Tạo Báo Cáo (PayrollReport)

![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niK90OcLHVavEK6f1Vb69GZMN0X3eAXH0H8kj57moYqjie8hikC3I2gYQD70ereGgJa_DIorAB4c5gjQqKYZBpqpXgkLoICrB0Je40000__y30000)

##### 4.5. Biểu đồ lớp UML Tổng Thể 

![Diagram](https://www.planttext.com/api/plantuml/png/T5H1QiCm4Bpx5Jege7uWb9130osKOj92pugrJKLbhP7a55FwiXxwf7wXiYt9ZkBu9C-kPcPtZFz-VhVMSUFQMXMLujQINTqex038Lq7ySqCW00zYJQHs0TMyXZLvTaRgOu0QjD99r1dyZgrHtPuxto-mFIY8_Lxk4ur8_GDEaWEQARCpKNQXnnQas8NAAgWSmUqIFrrDin5YpqgP2zzvGYacbYTlghy_6th0xvEPlZgRd90J6FdMbS4PbRffNPdxN9C3eWAkY-yYPFCYQwYu4IaR5u3pR9OJ4yDQ7h7YwiuV0pgat_E6Kd-CD5haXU0_-g2PFikbMQxA5WNPWbRCoRzMhV9N-ttQLpGV86OBJRifUMTGgT9W1TQYkTYHzUJIkjjeVfDjAzPZz9iuRSvChpAowsHnd6Pa2PmqVatv67jeqBWqGpEYaJKqvGx7I_HAy_JXQp1-dw5xSh3r8VZ_m3y0003__mC0)

#### 5. Lý Do Chọn Thiết Kế Này
* Đáp ứng nhu cầu thực tế: Các ca sử dụng này phản ánh đúng các chức năng cần thiết trong việc quản lý lương và thời gian làm việc của nhân viên, đảm bảo tính hiệu quả trong quy trình làm việc.
* Tính khả thi: Thiết kế này có thể được triển khai dễ dàng dựa trên mã nguồn đã có từ các bài lab trước, giúp tiết kiệm thời gian và công sức.
* Bảo mật và quản lý hiệu quả: Các ca sử dụng đảm bảo việc truy cập vào hệ thống được kiểm soát và quản lý hiệu quả, bảo vệ thông tin nhạy cảm của doanh nghiệp.
* Nâng cao hiệu suất: Giúp quản lý theo dõi và tối ưu hóa hiệu suất làm việc của nhân viên thông qua việc ghi nhận thời gian làm việc, từ đó có thể đưa ra quyết định hợp lý về quản lý nhân sự.
#### 6. Kết luận
Thiết kế ca sử dụng này sẽ tạo ra một khung làm việc rõ ràng cho các chức năng cần có của hệ thống Payroll System. Nó không chỉ giúp định hình các yêu cầu mà còn tạo cơ sở cho việc phát triển và triển khai hệ thống trong các bài lab tiếp theo. Việc thực hiện các ca sử dụng này sẽ cải thiện quy trình làm việc, tiết kiệm thời gian và nâng cao tính chính xác trong quản lý lương và thời gian làm việc của nhân viên. Thiết kế này cũng góp phần tạo ra một môi trường làm việc chuyên nghiệp và hiệu quả hơn cho cả nhân viên và quản lý.



