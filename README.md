<h1 align="center"> 📩 HỆ THỐNG GỬI MAIL CÓ THỜI HẠN </h1>
 
<div align="center">

<p align="center">
<img src="logoDaiNam.png" alt="DaiNam University Logo" width="200"/>

</p>

</div>

# 📩 Gửi mail có thời hạn

Đây là hệ thống gửi và nhận tài liệu bảo mật sử dụng mã hóa AES-RSA, chữ ký số và giới hạn thời gian để đảm bảo tính an toàn, toàn vẹn và xác thực của dữ liệu.

# 📝 Giới thiệu
📤 Gửi tài liệu bảo mật: Người gửi chọn file .txt và hệ thống sẽ mã hóa nội dung bằng AES-CBC, ký số bằng RSA 2048-bit, gắn thời gian sống (TTL) 24 giờ và gửi sang phía người nhận.

🔏 Xác thực & Toàn vẹn: Gói tin gửi đi chứa khóa phiên đã mã hóa, chữ ký số và hàm băm SHA-512 nhằm đảm bảo tính xác thực và toàn vẹn nội dung.

⏳ Giới hạn thời gian: Gói tin chỉ có hiệu lực trong vòng 24 giờ, sau thời gian này sẽ bị từ chối giải mã.

📥 Nhận và giải mã: Người nhận nhấn “Nhận” để giải mã file. Nếu hash, chữ ký và thời hạn hợp lệ thì sẽ giải mã thành công và lưu lại file.

📂 Quản lý file đã nhận: Tất cả các file nhận được sẽ được lưu trữ, hiển thị cùng thời gian nhận và có thể tải về hoặc xóa.

🗑️ Tự động dọn dẹp: Sau khi giải mã xong, gói tin truyền (transmission.json) sẽ tự động bị xóa để đảm bảo bảo mật.

# 🛠️ Hệ thống
![image](https://github.com/user-attachments/assets/d6675b38-f399-461a-af56-65faa6732373)

# 🔧 Công nghệ sử dụng
## 🔐 Mã hóa & Bảo mật
- AES-CBC (Advanced Encryption Standard - Cipher Block Chaining)
→ Mã hóa nội dung file nhạy cảm.

- RSA 2048-bit (PKCS#1 v1.5)
→ Trao đổi khóa phiên và ký số metadata.

- SHA-512 (Secure Hash Algorithm)
→ Kiểm tra tính toàn vẹn của gói tin.

- Chữ ký số (RSA + SHA-512)
→ Xác thực người gửi và chống giả mạo.

## 🖥️ Ngôn ngữ & Framework
- Python 3.10+

- Flask – Web framework nhẹ, xử lý backend và routing.

- HTML/CSS/JavaScript – Giao diện người dùng (UI).

- Jinja2 – Template engine của Flask (render HTML động).

## 📦 Thư viện Python chính
- pycryptodome: Mã hóa AES, RSA, ký số và băm SHA-512.

- base64, json, os, datetime: Xử lý dữ liệu và thời gian.

## 🗂️ Quản lý file
- Thư mục received_files/ – Lưu các file đã giải mã thành công.

- File transmission.json – Gói tin truyền tạm thời giữa người gửi và người nhận.
  
## 📦 Cài đặt thư viện cần thiết
- Chạy lệnh sau trong terminal:
```pip install flask pycryptodome```
- Hoặc dùng requirements.txt:
📄 requirements.txt -> 
```flask```
```pycryptodome```

# 📚 Hướng dẫn chạy chương trình
## 🚀 Các bước chạy chương trình
