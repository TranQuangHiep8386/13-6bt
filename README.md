# 13-6bt
CÁO BÀI TẬP LỚN
MÔN: PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG - TEE0419
PHẦN 1: NHÀ PHÁT MINH ỨNG DỤNG MIT
1.1 Giới thiệu MIT App Inventor
MIT App Inventor là công cụ cài đặt kéo dài giúp tạo ứng dụng Android mà không cần phải viết mã truyền thống.

Các thành phần chính
Designer : Thiết kế giao diện.
Blocks : Kéo-thả block để lập trình logic.
Giao diện làm việc
<img width="1726" height="845" alt="image" src="https://github.com/user-attachments/assets/24be4228-7e68-4a55-8707-fbf06db2d906" />
<img width="740" height="334" alt="image" src="https://github.com/user-attachments/assets/bf26468d-294d-4da3-b702-5541da80205b" />
<img width="1115" height="768" alt="image" src="https://github.com/user-attachments/assets/889a4fb7-cf5a-4461-916f-d568dbc4cfe8" />
<img width="1104" height="325" alt="image" src="https://github.com/user-attachments/assets/ecb021d5-f14e-4979-9f73-9a20971084e3" />
<img width="1172" height="786" alt="image" src="https://github.com/user-attachments/assets/174a1ea5-ba89-4b90-b288-130e95c9883a" />
#app1 Xem Danh Ngôn
1. Thuật toán đọc dữ liệu từ Assets (App 1)
Vấn đề: Đọc dữ liệu tĩnh đã chuẩn bị sẵn trong bộ nhớ app.
Các bước:
i.
Dùng assets.open("quotes.txt") để mở luồng đọc file.
ii.
Dùng bufferedReader() để đọc toàn bộ nội dung file thành một chuỗi (String).
iii.
Dùng hàm split("\n") để cắt chuỗi đó thành một danh sách (List) các câu nói.
iv.
Hiển thị: Mỗi khi bấm nút, dùng hàm Random.nextInt(size) để lấy một chỉ số ngẫu nhiên trong danh sách và hiển thị lên màn hình.
<img width="828" height="297" alt="image" src="https://github.com/user-attachments/assets/baf9f9d2-685f-4b84-beec-45be27c8f3aa" />

<img width="352" height="755" alt="image" src="https://github.com/user-attachments/assets/e4391555-31e5-485e-8888-d43376ec4aec" />
<img width="360" height="734" alt="image" src="https://github.com/user-attachments/assets/63876aea-0c5c-48bb-90da-f32f9f8d7bce" />
<img width="376" height="746" alt="image" src="https://github.com/user-attachments/assets/2836ce52-6fdb-485c-b461-31ff9a5b14cc" />


#app2 Giải phương trình và gửi dữ liệu lên server
2. Thuật toán Giải toán & Kết nối API (App 2)
•
Bài toán: Giải phương trình $ax + b = c$.
•
Logic giải toán:
◦
Chuyển phương trình về dạng $ax = c - b$.
◦
Nếu $a = 0$: Kiểm tra $b$ có bằng $c$ không để kết luận vô nghiệm hoặc vô số nghiệm.
◦
Nếu $a \neq 0$: Nghiệm $x = (c - b) / a$.
•
Gửi API (Networking):
i.
Đóng gói kết quả vào một đối tượng dữ liệu (Object) gồm: mã SV (k225480106018), dữ liệu đầu vào (a, b, c) và kết quả đầu ra.
ii.
Sử dụng Retrofit để tự động chuyển đối tượng này sang định dạng JSON.
iii.
Thực hiện phương thức POST gửi đến https://k58kmt.tdh.io.vn/api.
iv.
Nhận phản hồi (Callback) từ server để thông báo cho người dùng (Thành công/Thất bại).
3. Thuật toán WebView & Truyền tham số
•
Vấn đề: Hiển thị trang web cá nhân hóa.
•
Cách làm:
i.
Khởi tạo WebViewClient để app không mở trình duyệt bên ngoài.
ii.
Kích hoạt JavaScript (javaScriptEnabled = true).
iii.
Nối chuỗi URL: base_url + "?masv=" + masv_cua_ban.
iv.
Gọi lệnh loadUrl() để tải trang.
<img width="881" height="495" alt="image" src="https://github.com/user-attachments/assets/a23ef6b1-d9a7-44c6-98e0-2763000a8c95" />

<img width="343" height="734" alt="image" src="https://github.com/user-attachments/assets/a201ac0b-0a6e-4077-955b-04bc9f2dc6f3" />
<img width="353" height="755" alt="image" src="https://github.com/user-attachments/assets/c26f86c4-500d-4288-8383-25fbc78c72ae" />
<img width="355" height="746" alt="image" src="https://github.com/user-attachments/assets/dd603287-e747-44f0-b841-dfc4934384a7" />
<img width="353" height="733" alt="image" src="https://github.com/user-attachments/assets/0ca88846-99c7-4826-b730-17fc6aad8e9d" />
