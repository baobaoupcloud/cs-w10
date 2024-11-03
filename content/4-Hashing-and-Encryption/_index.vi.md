---
title : "Băm và Mã hóa"
date :  "`r Sys.Date()`" 
weight : 4 
chapter : false
pre : " <b> 4. </b> "
---
Khi mật khẩu được lưu trữ, chúng không bao giờ nên được lưu dưới dạng văn bản rõ. **Băm** và **mã hóa** là hai kỹ thuật thiết yếu bảo vệ dữ liệu nhạy cảm.

### Băm

Băm chuyển đổi một mật khẩu thành một chuỗi ký tự độc nhất và không thể đảo ngược. Khi bạn đăng nhập, mật khẩu được nhập sẽ được băm và hệ thống so sánh nó với giá trị băm đã lưu.

Phương pháp băm một chiều cho phép các dịch vụ trực tuyến không bao giờ lưu trữ mật khẩu gốc mà người dùng nhập vào. Chỉ có giá trị băm của các mật khẩu này. Theo đó, nếu có sự cố, chỉ giá trị băm bị lộ.

Bảng cầu vồng (rainbow tables) là các từ điển khổng lồ mà hacker sử dụng để cố gắng băm trước các mật khẩu có thể để phá vỡ thuật toán băm.

Như một quy trình bổ sung để tăng cường bảo mật, các lập trình viên đôi khi sẽ dùng "muối" (salting) để giảm khả năng nhiều người dùng có cùng giá trị băm đại diện cho mật khẩu của họ.

### Mã hóa

Mã hóa chuyển đổi dữ liệu thành định dạng không thể đọc được và chỉ có thể giải mã bởi người có khóa giải mã chính xác. Có hai loại khóa được sử dụng:
- **Khóa công khai**: Dùng để mã hóa dữ liệu, có thể chia sẻ công khai.
- **Khóa riêng**: Giữ bí mật, dùng để giải mã dữ liệu.

Mã hóa là rất quan trọng để bảo vệ dữ liệu và truyền thông nhạy cảm khỏi truy cập trái phép.

**Mã hóa đầu cuối** (được sử dụng bởi các ứng dụng như iMessage và WhatsApp) đảm bảo chỉ người gửi và người nhận mới có thể đọc tin nhắn, ngăn chặn các bên thứ ba chặn dữ liệu.
