# BÀI LÀM – THI THỬ HACKATHON 01

- **Mã đề:** Thi thử
- **Họ tên: Nguyễn Quỳnh Chi** 
- **Lớp:CNTT2** 
- **Link repository:https://github.com/chiqn2k8elsa-cyber/HN-KS26-CNTT2_Nhap-mon-CNTT_ThiThu** 
- **Hệ điều hành (Windows/macOS):Windows** 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
#### pwd
#### ls -Force
#### mv nhap_hang.txt docs
#### mv logo_van_phong_pham.png media
#### cp media\logo_van_phong_pham.png backup
#### rm temp_131.tmp
#### cd logs
#### ls
#### cd ..


```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
 Directory: C:\Users\admin\Downloads\starter-kit(2)\starter-kit\van-phong-pham-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/23/2026   8:51 AM                backup
d-----        10/23/2026   8:42 AM                data
d-----        10/23/2026   8:48 AM                docs
d-----        10/23/2026   8:42 AM                logs
d-----        10/23/2026   8:48 AM                media
------        10/19/2026   9:41 AM             78 .env
-a----        10/19/2026   9:41 AM           6053 backip
-a----        10/19/2026  10:00 AM           2253 bai_lam.md


    Directory: C:\Users\admin\Downloads\starter-kit(2)\starter-kit\van-phong-pham-website\backup


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026   9:41 AM           6053 logo_van_phong_pham.png


    Directory: C:\Users\admin\Downloads\starter-kit(2)\starter-kit\van-phong-pham-website\data


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026   9:41 AM           6105 don_hang_thang_10.xlsx


    Directory: C:\Users\admin\Downloads\starter-kit(2)\starter-kit\van-phong-pham-website\docs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026   9:41 AM             51 nhap_hang.txt


    Directory: C:\Users\admin\Downloads\starter-kit(2)\starter-kit\van-phong-pham-website\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026   9:41 AM           1053 shop.log


    Directory: C:\Users\admin\Downloads\starter-kit(2)\starter-kit\van-phong-pham-website\media


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/19/2026   9:41 AM           6053 logo_van_phong_pham.png

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
# Ghi lệnh vào đây (xoá dòng này)
#### get-content logs/shop.log | select-string "ERROR" > logs/daily_report.txt
#### get-content logs/daily_report.txt
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-10-28 08:24:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:30:28 [ERROR] Thanh toan bi tu choi

```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.
- [x] Heading 1: tên dự án
- [x] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [x] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [x] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [x] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [x] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
#### Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
#### .\auto_report.ps1
```

### Nội dung file logs/auto_report.txt

```text
=== BAO CAO LOI ===

2025-10-28 08:24:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:30:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:33:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 08:39:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 08:42:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 09:12:28 [ERROR] Thanh toan bi tu choi

```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
####  get-content logs/shop.log | select-string "ERROR" | Measure-Object

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
Count: 6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
#### "===TONG HOP LOG===" > logs/tong_hop.txt
#### get-content logs/shop.log | select-string "WARNING" >> logs/tong_hop.txt
#### get-content logs/shop.log | select-string "ERROR" | Measure-Object  >> logs/tong_hop.txt

```

### Nội dung file logs/tong_hop.txt

```text
===TONG HOP LOG===

2025-10-28 08:51:28 [WARNING] Thoi gian tai trang cham
2025-10-28 08:54:28 [WARNING] Anh san pham dung luong lon
2025-10-28 08:57:28 [WARNING] Thoi gian tai trang cham

Count    : 6
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property : 

```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/don_ban_thang_10.xlsx`, không cần ghi vào đây.
