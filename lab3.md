 ## Xác định các phần tử thiết kế
 ### 1. Hệ thống con: BankSystem 

 ##### a. Biểu đồ ngữ cảnh

  ![Diagram](https://www.planttext.com/api/plantuml/png/P4zB2i903Dtd5Bc05t0XrUB2XL3GdNGHnbXBEnb9fa8HJ-R28ta5HssXO5R9UxnFNezdPf4qThu5SZ4evft5u5c7SqNIhFsb3JqpWBAB95NBNtpNMsIFDy0qXwLpePE8MnAgsBF4yaVibSIIMnq42msEpMgf1d8Zfw2UHl9QMzfAk0ECHN0sMqpZvbYmVaGuCJQO5lsNv6TsJO9Q4iUGiHpJnsy0003__mC0)
    
##### b. Mô tả hệ thống
BankSystem là một hệ thống quản lý ngân hàng cung cấp các dịch vụ tài chính cho khách hàng và nhân viên ngân hàng. Hệ thống này cho phép người dùng mở, đóng tài khoản, thực hiện giao dịch, và kiểm tra thông tin tài khoản.

##### c. Chức năng chính
 * Quản lý tài khoản:
   * Mở tài khoản mới.
   * Đóng tài khoản.
   * Cập nhật thông tin tài khoản.
* Xử lý giao dịch:
   * Chuyển tiền.
   * Rút tiền.
   * Gửi tiền.
* Cung cấp thông tin:
    Kiểm tra số dư.
    Lịch sử giao dịch.
##### d. Giao diện
 * Giao diện của BankSystem
  * openAccount()
    * Mô tả: Mở tài khoản mới.
    * Tham số: Customer customer, double initialDeposit
    * Trả về: Account
  * closeAccount()
    * Mô tả: Đóng tài khoản hiện tại.
    * Tham số: Account account
    * Trả về: boolean
  * transferFunds()
    * Mô tả: Chuyển tiền từ tài khoản này sang tài khoản khác.
    * Tham số: Account fromAccount, Account toAccount, double amount
    * Trả về: boolean
  * checkBalance()
    * Mô tả: Kiểm tra số dư tài khoản.
    * Tham số: Account account
    * Trả về: double 

![Diagram](https://www.planttext.com/api/plantuml/png/R91D2i8m48NtEKMM5Ng2hjegWcjFC4sd69hCb6Io4F5aBZoILx3OMF1dDZCytljupEDshwD0aEITiYGO1Z2e3otGU3n7GQylIh-69wJ664uaXKbHs6Eez3PVfRPanOBRuSJHIgLxJft3JQLpA6ECuuXl3YnxzSpkZjaXK7PB08e3XdsYFXP3ODzyHKej_Ak1NuIrn2VMdD2CBJWWW_zAB35rLJLIFx_c2G00__y30000)

##### e. UML Class Diagram

![Diagram](https://www.planttext.com/api/plantuml/png/R90n3i8m303tli8Z37oW4o24n0mVS1EtLAGsIbmn85x6m9Fu0YbDALHuiEIpPP_yl3-MGT5hsxZCE0m1LiP8omhN368i0FjwPtEeMHCiq24Roi5AMpXAL2vCFeUz-fghDmEGCt5QEPidPfm4caBroA4alstPXd7qIEQqxgz5UCkIvQ6RHgEryCTKH_PhYqrtQI9hKQF_9kO4IYzDaig7BmoRvMy3uEp5K1XrAz8limqfrYwylPV4DZxv1G00__y30000)

### 2. Hệ thống con: PrintService
##### a. Biểu đồ ngữ cảnh

![Diagram](https://www.planttext.com/api/plantuml/png/R8z12i9034NtEKKkq0kua89k50IXkf8kqZ4j0pCPoAHkn9Evy4XUmIajWc1MoIVly__x-QgpaTeO0v2pf7ZEhCkwEpL6VG-Wx8na28n7zM8DwyqxnZjWcSi-TNWWeO4ZYxMpk4rkdCv29CSvUnbQU01CzbXLwr-d5JPZ5xtX5xCqVy0IuX-p8N4SPXLB2gXPhgN91m00__y30000)

##### b. Mô tả hệ thống
PrintService là một hệ thống quản lý in ấn, cho phép người dùng gửi tài liệu để in, theo dõi trạng thái công việc in và hủy các công việc in khi cần thiết.

##### c. Chức năng chính
  * Quản lý công việc in:
    * Nhận tài liệu để in.
    * Theo dõi trạng thái công việc in.
  * Xử lý tài liệu in:
    * In tài liệu.
    * Hủy công việc in.
##### d. Giao diện
Giao diện của PrintService
  * printDocument()
    * Mô tả: Gửi tài liệu để in.
    * Tham số: Document document
    * Trả về: PrintJob
  * cancelPrintJob()
  * Mô tả: Hủy một công việc in.
  * Tham số: PrintJob job
  * Trả về: boolean

![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTcNabgKLfYSgg2Pq0Ha1ESMbIM2UHLSoc0GG58q2K_kJGtDQz48mNAi5A02MbQAO3rUUKdGNKa9-Obf-R013MoyfCGIe2ga_BpSr8JyxXgkHnIyrA0JW00003__mC0)
    
##### e. UML Class Diagram

![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niO9BVd9fRcfUYK8rbm8Gw2gaG0KyKwmKClDAeAB9-NabG44hXU2IeioyTAXeMdvHRYAge892Uce9p53FlBHy3KskMYwePG50PILU-KbmoxBoar3jWTbk1NSOL0Bex9BIOaohWi7YG4iW8gK5AOabgN31MYw7rBmKe6y10000__y30000)

### 3. Hệ thống con: ProjectManagementDatabase
##### a. Biểu đồ ngữ cảnh

![Diagram](https://www.planttext.com/api/plantuml/png/X90n2i9G38Rtd28NAEuEKi75GP2AK-aG-zB7apQlfD55F9c3H_8A5YtLBfen-Nx-ZpnkzxGpKZirDL1fKN6hySYbRKZ8imxBdL5L0MX_8F4rJwc6nLPaTA2EyGBOJpu0k9OgQaCMek27BjvGncrK2-8Bk09Ccp595ZzgvhXqRhPl7Tbeqy7BysyoOzF0vp7tBGafY-k_yGG00F__0m00)

##### b. Mô tả hệ thống
ProjectManagementDatabase là một hệ thống lưu trữ và quản lý thông tin liên quan đến các dự án. Hệ thống này cho phép người dùng thêm, cập nhật và truy xuất thông tin dự án.

##### c. Chức năng chính
  * Quản lý thông tin dự án:
    * Thêm dự án mới.
    * Cập nhật thông tin dự án.
    * Xóa dự án.
  * Cung cấp báo cáo:
    * Lấy thông tin dự án.
    * Báo cáo tiến độ dự án.
##### d. Giao diện
Giao diện của ProjectManagementDatabase
  * addProject()
    * Mô tả: Thêm một dự án mới.
    * Tham số: Project project
    * Trả về: boolean
  * updateProject()
    * Mô tả: Cập nhật thông tin dự án.
    * Tham số: Project project
    * Trả về: boolean
  * getProjectInfo()
    * Mô tả: Lấy thông tin dự án.
    * Tham số: int projectId
    * Trả về: Project

  ![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTcNabgKLfYSgg2Pq1HVbPgSeblObvYUcfkQbw9Is99Ob9YSQf2DPS262Icf40LQHH0Q2i5g82cbK9IVdvEQc8UL6rfGKfYIIhHojDJIw1Iddbf-J3rdYbM2a0NQiBrSTLoEQJcfG1T3W000F__0m00)

##### e. UML Class Diagram

![Diagram](https://www.planttext.com/api/plantuml/png/ND0n3i8m30NGFQVm20CNoDIX2nk24qIfLGKrJcMx4-9a33qILo1jWweqGoJ_oFfF-NxcHjInJd4mVd0YSEFqHA_mCf3F1SPjldOM0ca9oKMqy50Er9UeG_4SHWs93YzhGUiqRontIP6wGmRGevRw5jM5GKvdypOrx8vZuft7wrZh2jd-LtQ7JdB0-HGZajRn8Y7a3DlQLaQJnVcRVW000F__0m00)
