# Thiết kế Hệ thống Con trong Hệ thống Payroll System

## 1. Các Hệ thống con Chính

### 1. Hệ thống Đăng Nhập
- **Mô tả**: Quản lý việc xác thực người dùng (nhân viên và quản lý) khi đăng nhập vào hệ thống.
  - **Chức năng**:
    - Xác thực thông tin đăng nhập.
    - Cung cấp tùy chọn khôi phục mật khẩu.
  - **Thành phần**:
    - Giao diện đăng nhập.
    - Xử lý xác thực người dùng.
    - Cơ sở dữ liệu lưu trữ thông tin đăng nhập.
   
![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aK9eSMeHLr5gSabYNdfEgeAIJtvwPfv2S6LnIMgkaa8rbm8GWDGewDefQ80bDS5YK3POE2mn9pCbiIHLmRaeDIKrhoGpCQSOgWghb88kK1VOK2k5wE3IvEJKuk9OOjMx9MRcb1QbndBLSZcavgK0VG80003__mC0)

### 2. Hệ thống Quản Lý Thời Gian Làm Việc
- **Mô tả**: Quản lý thông tin thời gian làm việc của nhân viên.
  - **Chức năng**:
    - Thêm, cập nhật, xóa và xem thông tin thời gian làm việc.
    - Hiển thị danh sách thời gian làm việc của nhân viên.
  - **Thành phần**:
    - Giao diện người quản lý.
    - Xử lý các thao tác trên thời gian làm việc.
    - Cơ sở dữ liệu lưu trữ thông tin thời gian làm việc.
   
![Diagram](https://www.planttext.com/api/plantuml/png/V92z2i9048JxUuebbHPv0Gk9aDR6ltx93U7WxWnt6oM8JsRX8_aA9Y46ZUYMCz-mmpnkzomA1wcTLLp8CT2QFPS8Ag0GzgK59JlZCEWENcZRH85BwAAelI50wP9c1uCpTNZ1GSzxUw9Hsd4RI30uOTGfP-4XyCFiawzd2yfDh2mt8nI_ogoqddHvT_ULPi4V88V51t1L6Rnkbte2003__mC0)

### 3. Hệ thống Xử Lý Lương
- **Mô tả**: Tính toán và xử lý lương cho nhân viên dựa trên thời gian làm việc và mức lương.
  - **Chức năng**:
    - Kiểm tra ngày thanh toán.
    - Tính toán lương cho nhân viên.
    - Lưu thông tin lương vào cơ sở dữ liệu.
  - **Thành phần**:
    - Giao diện người quản lý.
    - Xử lý quy trình tính toán lương.
    - Cơ sở dữ liệu lưu trữ thông tin lương.

![Diagram](https://www.planttext.com/api/plantuml/png/P91B2i90343tSuhWIXUzW0ifrArGx0d266inpK0c5OfuCXSUoIlOrkd2cbrUNZxa_NpbqL2jQzcXjw1mGC6Qr2bvGwcPO5LYhu4PIWsUOcoaXggFHkqAxWw6I3sGxM1zx0HImsOg_X38HgUuaB-E3FPebBG5J2QoxtZ8eK96xMTtYRzsXJUQLurJCEd_VFBdixTG13atsg8rGTp3vIIduICV0000__y30000)

### 4. Hệ thống Tạo Báo Cáo
- **Mô tả**: Tạo và xuất các báo cáo liên quan đến lương và thời gian làm việc.
  - **Chức năng**:
    - Cho phép người quản lý chọn loại báo cáo.
    - Tạo và hiển thị báo cáo.
    - Xuất báo cáo ra định dạng file (PDF, Excel).
  - **Thành phần**:
    - Giao diện tạo báo cáo.
    - Xử lý tạo báo cáo.
    - Cơ sở dữ liệu lưu trữ dữ liệu báo cáo.
   
![Diagram](https://www.planttext.com/api/plantuml/png/R92n2i8m54NtVCMZamx5tK4AfZeLnBg9mwC-IY5DG_g45l7B7FmaVy7Of62n6UyxvtB9-_bAMaRBjre9BBYnaA76agomL33gKX54HpADvKgNaFSjKnt1NO1x0OLu0uizQRB811vU3i1V2l6NpKcvyf31gJSKy9c3DxPDRIerre14ng3CNRmZgzOex2U3VXUdtM1CzawpeMTKrd0-oDqgxGfI5_4G2Uch-xKF0000__y30000)

## 2. Mô Hình Kiến Trúc Hệ Thống
- **Frontend**: Giao diện người dùng cho các chức năng như đăng nhập, quản lý thời gian làm việc, xử lý lương và tạo báo cáo.
- **Backend**: Xử lý logic ứng dụng, bao gồm xác thực, tính toán lương, và quản lý dữ liệu.
- **Cơ sở dữ liệu**: Lưu trữ thông tin người dùng, thời gian làm việc và thông tin lương.

## 3. Cấu Trúc Dữ Liệu
- **Bảng Nhân Viên**:
  - `employee_id`: int (khóa chính)
  - `name`: String
  - `position`: String
  - `hourly_rate`: double
  - `password`: String (đã mã hóa)

- **Bảng Thời Gian Làm Việc**:
  - `timecard_id`: int (khóa chính)
  - `employee_id`: int (khóa ngoại tới Bảng Nhân Viên)
  - `date`: Date
  - `start_time`: Time
  - `end_time`: Time

- **Bảng Lương**:
  - `payroll_id`: int (khóa chính)
  - `employee_id`: int (khóa ngoại tới Bảng Nhân Viên)
  - `pay_period`: String
  - `total_hours`: double
  - `total_pay`: double

## 4. Kết luận
Việc thiết kế các hệ thống con trong Hệ thống Payroll System giúp đảm bảo rằng tất cả các chức năng cần thiết được phân chia rõ ràng và có thể quản lý hiệu quả. Thiết kế này tạo cơ sở cho việc phát triển và mở rộng hệ thống trong tương lai, đồng thời giúp dễ dàng bảo trì và cập nhật khi có yêu cầu mới.
