 ### 1. Phân tích Kiến Trúc
Đề xuất kiến trúc:

Kiến trúc đề xuất cho hệ thống "Payroll System" là kiến trúc 3-tầng (3-Tier Architecture), gồm:
- Tầng Presentation (Giao diện): Phụ trách giao tiếp với người dùng cuối, cung cấp các form và giao diện để quản lý thanh toán và nhập liệu.
- Tầng Application (Ứng dụng): Xử lý nghiệp vụ, thực hiện các ca sử dụng như "Select Payment" và "Maintain Timecard".
- Tầng Data Access (Truy cập dữ liệu): Quản lý việc lưu trữ và truy xuất dữ liệu từ cơ sở dữ liệu.
  
Lý do lựa chọn mô hình này vì :

Kiến trúc 3-tầng giúp hệ thống dễ mở rộng và bảo trì. Mỗi tầng xử lý một khía cạnh riêng của hệ thống, giúp các thành phần ít bị phụ thuộc lẫn nhau, nâng cao tính linh hoạt và khả năng tái sử dụng.

* Biểu đồ Package UML cho Kiến trúc 3-Tầng : 

![Diagram](https://www.planttext.com/api/plantuml/png/T91D2i9034RtSugX-rv1MX3NHRr0I8CCpX_9A9JYoLnu9A_WM12dCcRvFNZvakVzqKa2JXTdLGGymubqCp09-GJ91D_eMUayQ4543p2vJ7Q1NP4UZIC47fVufhwYFaPhyB_dG7mrI1NLXvIsBIJGFIA9L6rxYa5C2ZnLX0NCpfyJstQpBglMrHTUhbST-V7zinS0003__mC0)

 ### 2. Cơ chế phân tích
Các cơ chế quan trọng cần được giải quyết bao gồm:

- Xử lý và lưu trữ thông tin thanh toán: Đảm bảo tính chính xác và bảo mật cho dữ liệu thanh toán.
- Quản lý thời gian làm việc: Cung cấp cơ chế để nhập liệu và lưu trữ thông tin chấm công của nhân viên.
- Tính toán lương: Xử lý các công thức tính lương dựa trên dữ liệu chấm công và các quy định.
- Bảo mật thông tin: Đảm bảo dữ liệu nhạy cảm không bị truy cập trái phép.
 ### 3. Phân tích ca sử dụng "Select Payment"
Mô tả ca sử dụng "Select Payment":

- Người dùng có thể chọn một khoản thanh toán để xem thông tin chi tiết như ngày, số tiền, phương thức thanh toán.
- Ca sử dụng này yêu cầu xử lý yêu cầu từ người dùng, truy vấn thông tin thanh toán từ kho dữ liệu, và hiển thị chi tiết thanh toán.
* Biểu đồ lớp (Class Diagram) cho "Select Payment" Use Case

  ![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bToJc9niK90OcLkQbw9GZMN0X3eAcIcM2bavfL0UOcv-QLv9LOAAVcbIJcfKC6Kn99KAmKN80aLo4qjoSW7wWikAShCI-UgvK8rEpYrg2mpEHLgXO92Uce9L4O3Qfkc5KmjXkQWr8ByuioI_A9AkFwqr9Ba3Bmce5cigsi7byKjXR29oo4rBmKKH000003__mC0)
* Biểu đồ tuần tự (Sequence Diagram) cho "Select Payment" Use Case
  
  ![Diagram](https://www.planttext.com/api/plantuml/png/UhzxlqDnIM9HIMbk3bTYSab-aK9eSMeH5uXGqBLJ24Yip4tDAt7BByfLi58eJir9JIw1YcbafcXo8SiZb0Ud5fLb9gS2TQIdObCEaqVe24ejo2_E15fV2TIKbbgId8556v8YNMoM5K04N19B4Z5iml0BL36g3u2gm3wtKaZ9B2x8IQo4ALD8IIr9pCmfvd98pKi1XHK0003__mC0)
  ### 4. Phân tích ca sử dụng "Maintain Timecard"
 Mô tả ca sử dụng "Maintain Timecard":

 * Người dùng có thể nhập hoặc cập nhật thời gian làm việc của nhân viên.
 * Ca sử dụng này yêu cầu giao diện để nhập liệu, xử lý logic lưu trữ và cập nhật vào cơ sở dữ liệu.
 
 * Biểu đồ lớp (Class Diagram) cho "Maintain Timecard" Use Case 

 ![Diagram](https://www.planttext.com/api/plantuml/png/V93F2i8m3CRlVOeS9zWNs45syE9L1S-r2LXirz4_Wp5yCWy-agzW1xMo3SmXa7nVyWjvFr-D3yA5Q3IJMdWFPsL82eSmCaZ1GM4DgWsv8jDfEn0TPjsRZSvVhBjJQgEDLqrPGH6eXdtAxC4MY1EvNadA9021-9Mg8ElYssGzTjEsOic7RM7kNM6Er5clWdL38NdHKxKQMzx5-QuO_ee_0ckenUcP7m000F__0m00)

 * Biểu đồ tuần tự (Sequence Diagram) cho "Maintain Timecard" Use Case
 
 ![Diagram](https://www.planttext.com/api/plantuml/png/X92x3G8n38RxJ94IYbk00bt503m6i1mZB5tEoCuTOZOAHc850bAaG91eN5ZVvyV_kDrxIw1fYeC3JAB-OAJkLNotzdkEXA1X8nhzoaC8fRC8b807MxeFfd9sf3CZ_TCALfbREejnFkQQPOEPMgj2kfyxRK8aitPD-nNAU6IDNuzaxfr27dMIIu4WiOokfp7an9u0003__mC0)
 
  ### 5. Hợp nhất kết quả phân tích
Từ hai ca sử dụng trên, ta có thể xây dựng một mô hình chung gồm các lớp xử lý chính cho hệ thống như PaymentService, TimecardService, PaymentRepository, và TimecardRepository. Kiến trúc và các cơ chế được đề xuất giúp hệ thống dễ mở rộng, quản lý tốt các chức năng thanh toán và chấm công của nhân viên.
