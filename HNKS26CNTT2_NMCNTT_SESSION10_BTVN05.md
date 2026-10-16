# Bài 5 : Xây dựng bộ tài liệu kỹ thuật cho dự án Smart Farm
## *Phần 1. Phân tích*
- Input (đầu vào): Dữ liệu nhiệt độ, độ ẩm đất từ cảm biến và lệnh điều khiển
- Output (đầu ra): Bật hoặc tắt máy bơm để tưới cây tại trang trại Lan
---
**Sơ đồ phối hợp phần cứng của hệ thống trang trại**
Cảm biến IoT
Đo nhiệt độ và độ ẩm đất
 
          |
          V
Bộ điều khiển / CPU
Xử lý dữ liệu theo chương trình

          |
          v
Mạch điều khiển và máy bơm
Thực hiện tưới cây khi cần

## *Phần 2. Triển khai*

## Smart-Farm – Trang trại thông minh

### 1. Mô tả dự án

**Smart-Farm** là hệ thống ứng dụng IoT để theo dõi nhiệt độ, độ ẩm đất và tự động điều khiển máy bơm, giúp người nông dân chăm sóc cây trồng thuận tiện hơn

### 2. Hướng dẫn cài đặt
1. Kết nối cảm biến với bộ điều khiển
2. Kết nối máy bơm qua mạch điều khiển phù hợp
3. Cài đặt chương trình theo hướng dẫn của thiết bị
4. Bật nguồn và kiểm tra dữ liệu cảm biến

### 3. Tính năng

- [x] Đọc dữ liệu nhiệt độ và độ ẩm đất
- [x] Kiểm tra độ ẩm theo ngưỡng cài đặt
- [ ] Tự động bật/tắt máy bơm khi cần tưới
- [ ] Theo dõi dữ liệu trên màn hình quản lý

### 4. Bảng thông số

| Thành phần | Chức năng |
|---|---|
| Cảm biến | Đo nhiệt độ và độ ẩm đất |
| CPU / Bộ điều khiển | Xử lý dữ liệu và thực hiện lệnh |
| RAM | Lưu dữ liệu tạm thời khi hệ thống hoạt động |
| Bộ nhớ lưu trữ | Lưu chương trình và nhật ký |
| Máy bơm | Tưới nước cho cây |

## *Phần 3. Kiểm thử*
### 5. Lưu ý

- Kiểm tra dây nối và nguồn điện trước khi sử dụng
- Nếu RAM đầy, hãy giảm dữ liệu tạm và kiểm tra chương trình
- Lưu nhật ký vào ổ cứng để tránh làm đầy RAM
- Sao lưu trước khi xóa nhật ký cũ để tránh mất dữ liệu

