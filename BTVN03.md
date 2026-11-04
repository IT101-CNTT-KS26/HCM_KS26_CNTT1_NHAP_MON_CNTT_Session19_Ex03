#         BTVN 03 (SESSION 19) 
## 1.Báo cáo phân tích IPO : Xác định Input (Dấu hiệu nhiễm), Process (Các bước xử lý), Output (Hệ thống sạch).
### Input (Dấu hiệu nhiễm):
- FB, Gmail bị mất quyền kiểm soát liên tục,  bị đổi mật khẩu, đăng xuất đột ngột.
- Nghi vấn là dính Infostealer. 
### Process (Các bước xử lý):
- Ngắt kết nối mạn Wifi hoặc mạng LAN trên máy tính dính mã độc ngay lập tức để chặn và ngưng tải thêm các dữ liệu khác ra ngoài.
- Đổi mật khẩu và bật xác minh 2FA thực hiện đổi mật khẩu toàn bộ tài khoản quan trọng (Gmail, FB, GitHub, Banking...) từ các thiết bị mà không dính mã độc, kích hoạt 2FA ưu tiên dùng Authenticator App.
### Output (Hệ thống sạch):
- Tài khoản cá nhân được bảo vệ bởi  2FA trên thiết bị sạch.
- Máy tính bị nhiễm mã độc được dọn sạch, không còn nguy cơ bị đánh cắp dữ liệu tiếp diễn.
## 2.Triển khai: Mô tả chi tiết cách thực hiện "Đổi mật khẩu từ thiết bị khác" và "Revoke Token" trên GitHub. 
### Đổi mật khẩu từ thiết bị sạch:
- Sử dụng 1 thiết bị sạch như điện thoại cá nhân dùng 4G,5G hoặc laptop sạch. Chúng ta tuyệt đối không thao tác trên máy tính đã bị nhiễm mã độc.
- Quy trình:

  ->Truy cập vào trang quản lý tài khoản Google chọn vào phần Mật khẩu.
  
  ->Sau đó thực hiện đổi mật khẩu (chọn mật khẩu ngẫu nhiên hoặc dùng mật khẩu mạnh).

  ->Khi đổi mật khẩu thành công thì chúng ta sẽ đăng xuất tài khoản Google của mình ra trên các thiết bị khác.

  ->Kích hoạt 2FA qua Authenticator app tránh dùng SMS nếu nghi ngờ SIM điện thoại bị can thiệp.
### Revoke Token trên GitHub:
- **Thu hồi Personal Access Tokens (PAT):**
  
   ->Vào GitHub từ thiết bị sạch > click Avatar góc trên bên phải > Settings.

   ->Chọn Developer settings (ở cuối menu bên trái) > Personal access tokens (chọn cả Tokens (classic) và Fine-grained tokens).

   ->Kiểm tra danh sách token, bấm Delete hoặc Revoke toàn bộ token đang hoạt động để làm vô hiệu hóa API key bị lộ.
- **Thu hồi Active Sessions & Authorized OAuth Apps:**

   ->Trong Settings > chọn Sessions > Click Revoke all (hoặc Revoke từng phiên từ máy bị nhiễm).

   ->Vào Applications > Authorized OAuth Apps > Revoke các ứng dụng lạ hoặc ứng dụng liên quan đến thiết bị dính mã độc.

- **Thu hồi SSH Keys:**

   ->Trong Settings > SSH and GPG keys.

   ->Kiểm tra danh sách SSH Keys, bấm Delete đối với các Public Key tương ứng với Private Key lưu trên máy bị dính Infostealer.




