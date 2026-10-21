# (Bài Tập Tổng Hợp) Tech Lead của Cyber Arena
## Phần 1 – Lĩnh vực CNTT và đơn vị lưu trữ
### 1. Lựa chọn nhân sự kỹ thuật
- **Lựa chọn:** Chọn ứng viên B (Lĩnh vực Mạng máy tính / Quản trị hệ thống).
- **Giải thích:** Nhu cầu cốt lõi của Cyber Arena là duy trì phòng máy hoạt động ổn định, sửa chữa phần cứng kịp thời và đảm bảo hạ tầng mạng cho livestream/tập luyện. Việc viết phần mềm đặt lịch chưa phải ưu tiên cấp thiết bằng việc giữ cho hệ thống máy tính và mạng không gặp sự cố.
### 2. Sắp xếp đơn vị lưu trữ theo thứ tự tăng dần
Byte < KB < MB < GB < TB
## Phần 2 – Mô hình IPO và lĩnh vực CNTT
### 1. Bảng mô hình IPO cho hệ thống quay và xem lại trận đấu
|Thành phần |	Trong hệ thống quay/xem lại trận đấu|
|---|---|
|Input | Tín hiệu hình ảnh/âm thanh từ màn hình chơi game và micro|
|Process |	CPU/GPU mã hóa và nén tín hiệu thô thành định dạng video|
|Output |	Video hiển thị lên màn hình để phân tích hoặc phát trực tiếp lên YouTube|
|Storage |	Ổ cứng SSD dùng để lưu trữ các file video trận đấu (.mp4, .mkv)|
### 2. Lĩnh vực CNTT gắn với hoạt động của Cyber Arena
- **Mạng máy tính & Truyền thông:** Đảm bảo đường truyền internet ổn định để livestream trực tiếp lên YouTube và giảm độ trễ (ping) khi thi đấu.
- **Khoa học dữ liệu & Phân tích:** Sử dụng dữ liệu video quay lại để phân tích hành vi, chiến thuật của tuyển thủ nhằm đưa ra quyết định nâng cao hiệu suất thi đấu.


## Phần 3 – Tính toán dung lượng và tốc độ mạng
### 1. Tính dung lượng lưu trữ
20 trận × 500MB = 10,000MB

**Đổi sang GB:**

  10,000MB ÷ 1024 ≈ 9.77GB
  
**Sức chứa SSD 512GB:**

-	SSD 512 GB chứa thoải mái video của 1 tháng.
-	Dung lượng còn trống sau 1 tháng vận hành:
512GB – 9.77GB = 502.23GB
### 2. Tính tốc độ mạng
**Đổi 100Mbps sang MB/s:**

Tốc độ (MB/s) = 100 ÷ 8 = 12.5MB/s
  
**Thời gian upload đoạn video 200MB:**

Thời gian = 200MB ÷ 12.5MB/s = 16 giây
  
**Lý do thực tế lâu hơn con số tính được:**

Do hao hụt băng thông (network overhead), nhiễu tín hiệu đường truyền hoặc server nhận (YouTube) giới hạn tốc độ tải lên tại thời điểm đó.
## Phần 4 – Phần cứng và mô hình DIKW
### 1. Quyết định nâng cấp phần cứng
- **Lựa chọn:** Nâng cấp CPU.
-	**Giải thích:** Việc vừa chơi game nặng vừa quay video livestream đòi hỏi năng lực tính toán và phân luồng xử lý rất cao của CPU. Dung lượng RAM 16 GB hiện tại đã đủ đáp ứng nhu cầu chạy nền cơ bản, trong khi CPU bị quá tải mới là nguyên nhân chính gây ra hiện tượng giật lag.
### 2. Áp dụng mô hình DIKW
| |	Nội dung trong tình huống |	Vì sao thuộc tầng này|
|---|---|---|
|Data |	Tuyển thủ bị hạ gục trong các trận đấu. |	Đây là những sự kiện được ghi nhận từ trận đấu.|
|Information |	Tuyển thủ hay chết ở phút 15–20 |	Dữ liệu được tổng hợp để nhận ra một mẫu lặp lại theo thời gian.|
|Knowledge |	Chết do thiếu tầm nhìn bản đồ |	Huấn luyện viên phân tích thông tin để tìm ra nguyên nhân.|
|Wisdom	Huấn | luyện viên yêu cầu mua thêm mắt (Ward) cho trận sau |	Huấn luyện viên sử dụng tri thức để đưa ra quyết định cải thiện chiến thuật.|
