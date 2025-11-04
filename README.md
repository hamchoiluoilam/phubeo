# Tóm tắt cách chạy chương trình Ngân hàng điện tử
1. Giới thiệu chương trình
   Chương trình mô phỏng một hệ thống ngân hàng đơn giản cho phép người dùng:
      - Đăng ký nhiều loại tài khoản (Saving, Student, Business, Normal)
      - Thực hiện các thao tác xem thông tin tài khoản, nạp tiền, rút tiền, chuyển khoản, xem lịch sử giao dịch và đặt vé xem phim
      - Thực hiện các chức năng của từng loại tài khoản
      - Lưu toàn bộ thông tin tài khoản xuống file accounts.txt khi thoát
2. Cấu trúc chương trình
  Bao gồm các lớp :
   - Lớp cha : Account là lớp cơ sở, chứa thông tin tài khoản ( số tk, số dư, tên người dùng, lịch sử giao dịch )
   - Lớp con :
            - SavingAccount là tài khoản tiết kiệm có lãi suất
            - StudentAccount là tài khoản sinh viên có mức ưu đãi 50% khi rút tiền
            - BusinessAccount là tài khoản doanh nghiệm có mức phí giao dịch 2%
       
  - Các lớp con đều ghi đè (override) các hàm getType(), showInfo(), và một số hàm khác tùy loại.
  -  Các hàm hỗ trợ findAccount ( tìm tài khoản theo STK ) và saveAll ( Lưu tài khoản xuống file )
  -  Các cấu trúc mã nguồn gồm : 
      - title.cpp : Mã nguồn chính của chương trình
      - accounts.txt : File lưu danh sách tài khoản 
      - README.md : File hướng dẫn sử dụng

3. Cách chạy chương trình
- Bước 1 : Lưu mã nguồn vào file title.cpp
- Bước 2 : Biên dịch Chương trình
- Bước 3 : Chạy chương trình
- Bước 4 : Sau khi chạy chương trình
  - Chọn 1 để đăng kí tài khoản và chọn loại ngân hàng cần sử dụng.
  - Sau khi đăng kí tài khoản, chọn 2 để đăng nhập và sử dụng các chức năng của chương trình : 
    - Chọn 1 để xem thông tin tài khoản
    - Chọn 2 để nạp tiền vào tài khoản ( Tài khoản tiết kiệm được hưởng mức lãi suất 3%)
    - Chọn 3 để rút tiền từ tài khoản ( Tài khoản sinh viên được giảm 50%)
    - Chọn 4 để giao dịch với tài khoản khác ( Tài khoản doanh nghiệp phải chịu phí giao dịch 2%)
    - Chọn 5 để xem lịch sử giao dịch
    - Chọn 6 để đặt vé xem phim và lưu vào lịch sử giao dịch
    - Chọn 0 để đăng xuất
- Bước 5 : Khi thoát, toàn bộ dữ liệu tài khoản sẽ được lưu vào file accounts.txt trong thư mục.

5. Ghi chú
      - Số dư khởi tạo = 0 (khi đăng ký mới)
      - Không có nạp/rút âm tiền
      - Khi đăng nhập sai mật khẩu hoặc STK không tồn tại thì chương trình báo lỗi
      - Mỗi lần chạy chương trình mới, file accounts.txt sẽ được ghi đè
           
