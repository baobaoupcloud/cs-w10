---
title : "Bảo mật mật khẩu"
date :  "`r Sys.Date()`" 
weight : 2 
chapter : false
pre : " <b> 2. </b> "
---
### Mật khẩu

Mật khẩu là một trong những thành phần cơ bản nhưng quan trọng nhất của bảo mật kỹ thuật số. Tuy nhiên, mật khẩu yếu khiến tài khoản gặp rủi ro đáng kể.

Dưới đây là một số mật khẩu phổ biến mà mọi người thường sử dụng:

1. 123456
2. admin
3. 12345678
4. 123456789
5. 1234
6. 12345
7. password
8. 123
9. Aa123456
10. 1234567890

Nếu bạn đang sử dụng một trong những mật khẩu trên, rất có thể có hàng triệu người khácc cũng đang dùng mật khẩu giống bạn! Hacker cũng có thể đoán ra hầu hết các ký tự mà bạn thêm vào mật khẩu của mình. Họ có thể sử dụng các cuộc tấn công brute-force, sử dụng một từ điển mật khẩu để thử từng mật khẩu có thể có. Mật khẩu của bạn có thể không an toàn như bạn nghĩ đâu.

### Mật khẩu mạnh nên bao gồm:

- Tối thiểu từ 12–16 ký tự
- Kết hợp chữ hoa, chữ thường, số và ký tự đặc biệt
- Không chứa các cụm từ thông dụng hoặc các mẫu dễ đoán

Ví dụ: `G7!klpQr92@wD` là một mật khẩu an toàn hơn. 

Mật khẩu tám ký tự bao gồm chữ cái, số và ký tự đặc biệt có khoảng **6 triệu tỷ** khả năng kết hợp, làm cho các cuộc tấn công brute-force trở nên khó khăn hơn nhiều.

### Trình quản lý mật khẩu

Trình quản lý mật khẩu có thể được sử dụng để tạo các mật khẩu rất khó đoán và ghi nhớ chúng cho bạn. Khả năng mật khẩu được bảo vệ bằng trình quản lý mật khẩu bị phá vỡ là rất, rất thấp.

Tuy nhiên vẫn có rủi ro, nếu ai đó truy cập được vào trình quản lý mật khẩu của bạn, họ sẽ có quyền truy cập vào tất cả các mật khẩu của bạn. Vì vậy việc bảo vệ cho trình quản lý mật khẩu cũng cần được chú ý kỹ.

### Bảo mật điện thoại

Nhiều điện thoại được bảo vệ bằng mã bốn chữ số. Có 10,000 khả năng cho mật khẩu khi sử dụng mã bốn chữ số. Hình thức tấn công đơn giản nhất sẽ là brute-force thử tất cả các mật khẩu có thể có.

Nếu mất một giây cho mỗi lần đoán, sẽ mất tổng cộng 10,000 giây để phá mã. Tuy nhiên, nếu một lập trình viên tạo ra một chương trình để tạo tất cả các mã có thể, thời gian yêu cầu sẽ rất ít. Hãy xem mã Python sau:
```python
from string import digits
from itertools import product

for passcode in product(digits, repeat=4):
    print(passcode)
```

Mã trên có thể chỉ mất vài giây (tối đa!) để tìm ra mật khẩu của bạn. Chúng ta có thể cải thiện bảo mật của mình bằng cách chuyển sang mật khẩu bốn chữ cái. Điều này sẽ tạo ra 7,311,616 mật khẩu có thể. Bao gồm các ký tự viết hoa và viết thường sẽ tạo ra hơn 78 triệu khả năng.

Xem cách chúng ta có thể chỉnh sửa mã của bạn để tìm các mật khẩu này:
```python
from string import ascii_letters
from itertools import product

for passcode in product(ascii_letters, repeat=4):
    print(passcode)
```

Chúng ta thậm chí có thể thêm khả năng kiểm tra tất cả các mật khẩu tám chữ số có chữ cái, số và dấu câu:
```python
from string import ascii_letters, digits, punctuation
from itertools import product

for passcode in product(ascii_letters + digits + punctuation, repeat=8):
    print(passcode)
```

Mở rộng lên tám ký tự, bao gồm chữ cái viết hoa và viết thường, số và ký tự đặc biệt, sẽ tạo ra 6,095,689,385,410,816 kết hợp có thể.

Trong thế giới kỹ thuật số, bạn chỉ cần mật khẩu của mình tốt hơn mật khẩu của người khác để người khác bị tấn công trước bạn — vì bạn là mục tiêu bất tiện hơn.

Một nhược điểm của việc sử dụng mật khẩu dài như vậy là bạn phải ghi nhớ nó. Do đó, có các biện pháp phòng thủ khác thêm vào để làm chậm kẻ tấn công. 

Ví dụ: một số nhà sản xuất điện thoại khóa những ai đoán sai mật khẩu nhiều lần. An ninh lúc này chính là tìm kiếm một "điểm giao" giữa việc tăng cường bảo mật trong khi vẫn giữ được sự thuận tiện.

