
# BÀI LÀM ÔN TẬP NGÀY 1

## Phần A - Tổ chức thư mục bằng GUI

### A1. Bật hiển thị đuôi file và file ẩn

- Mở File Explorer.
- Chọn **View → Show → File name extensions** để hiển thị đuôi file.
- Chọn **View → Show → Hidden items** để hiển thị file ẩn.

### A2. Đổi tên thư mục gốc thành trung-tam-tieng-anh

- Chọn thư mục `Trung Tam Tieng Anh FINAL`.
- Click chuột phải, chọn **Rename**.
- Đổi tên thành `trung-tam-tieng-anh`.

### A3. Tạo 5 thư mục trong thư mục gốc

- Sử dụng tổ hợp phím `Ctrl + Shift + N` để tạo thư mục mới.
- Lần lượt tạo 5 thư mục:
  - `docs`
  - `media`
  - `data`
  - `logs`
  - `archive`

### A4. Đổi tên 5 file theo dạng snake_case

- `Logo Trung Tam.PNG` → `logo_trung_tam.png`
- `Anh Lop Hoc.JPG` → `anh_lop_hoc.jpg`
- `Lich Hoc.txt` → `lich_hoc.txt`
- `Hoc Vien Khoa 3.xlsx` → `hoc_vien_khoa_3.xlsx`
- `Access.log` → `access.log`
### A5. Chuyển file vào các thư mục tương ứng

#### Chuyển file Excel vào data

- Chọn file `hoc_vien_khoa_3.xlsx`.
- Nhấn `Ctrl + X` để cắt.
- Mở thư mục `data`.
- Nhấn `Ctrl + V` để dán.

#### Chuyển file log vào logs

- Chọn file `access.log`.
- Nhấn `Ctrl + X` để cắt.
- Mở thư mục `logs`.
- Nhấn `Ctrl + V` để dán.

#### Giữ các file còn lại tại thư mục gốc

- `logo_trung_tam.png`
- `anh_lop_hoc.jpg`
- `lich_hoc.txt`
- `temp_201.tmp`
- `temp_202.tmp`
- `.env`

### A6. Sao chép file Markdown vào thư mục gốc

- Mở thư mục `starter-kit`.
- Chọn file `bai_lam_ngay1.md`.
- Nhấn `Ctrl + C` để sao chép.
- Mở thư mục `trung-tam-tieng-anh`.
- Nhấn `Ctrl + V` để dán.
- Giữ nguyên file `.env` trong thư mục gốc, không mở nội dung hoặc upload lên GitHub.

---

## Phần B - Thao tác bằng CLI

Mở PowerShell tại thư mục `trung-tam-tieng-anh`.

### B1. Hiển thị đường dẫn tuyệt đối của thư mục hiện tại

**Lệnh:**

```powershell
pwd
```

**Kết quả:**

```text
Path
----
[Điền đường dẫn tuyệt đối thực tế trên máy]
```

### B2. Liệt kê nội dung, gồm cả file ẩn

**Lệnh:**

```powershell
ls -Force
```
**Kết quả cần kiểm tra:**

- 5 thư mục `docs`, `media`, `data`, `logs`, `archive`.
- 3 file `logo_trung_tam.png`, `anh_lop_hoc.jpg`, `lich_hoc.txt`.
- 2 file `temp_201.tmp`, `temp_202.tmp`.
- File `bai_lam_ngay1.md` và file ẩn `.env`.

### B3. Di chuyển file lịch học vào docs; logo và ảnh lớp học vào media

#### Di chuyển file lịch học vào docs

```powershell
mv .\lich_hoc.txt .\docs\
```

#### Di chuyển logo vào media

```powershell
mv .\logo_trung_tam.png .\media\
```

#### Di chuyển ảnh lớp học vào media

```powershell
mv .\anh_lop_hoc.jpg .\media\
```
### B4. Sao chép logo từ media vào archive

**Lệnh:**

```powershell
cp .\media\logo_trung_tam.png .\archive\
```
File logo gốc vẫn được giữ trong `media`.

### B5. Xóa 2 file .tmp tại thư mục gốc

#### Xóa file temp_201.tmp

```powershell
rm .\temp_201.tmp
```

#### Xóa file temp_202.tmp

```powershell
rm .\temp_202.tmp
```

### B6. Dùng đường dẫn tương đối vào logs, liệt kê nội dung rồi quay lại thư mục gốc

#### Di chuyển vào logs

```powershell
cd .\logs\
```

#### Liệt kê nội dung

```powershell
ls -Force
```

#### Quay lại thư mục gốc

```powershell
cd ..
```

### B7. Đứng tại docs, sao chép ảnh lớp học từ media sang archive bằng đường dẫn tương đối

#### Di chuyển vào docs

```powershell
cd .\docs\
```

#### Sao chép ảnh từ media sang archive

```powershell
cp ..\media\anh_lop_hoc.jpg ..\archive\
```

#### Quay lại thư mục gốc

```powershell
cd ..
```

Lệnh sao chép được thực hiện khi đang đứng trong `docs`.

### B8. Liệt kê toàn bộ dự án kể cả file ẩn

**Lệnh:**

```powershell
ls -Recurse -Force
```

**Kết quả:**

## B8. Liệt kê toàn bộ dự án kể cả file ẩn

**Lệnh:**

```powershell
ls -Recurse -Force
```

**Kết quả:**

```text
PS C:\Users\admin\Desktop\trung-tam-tieng-anh> ls -Recurse -Force

    Directory: C:\Users\admin\Desktop\trung-tam-tieng-anh

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/20/2026   3:20 PM                archive
d-----        10/20/2026   3:03 PM                data
d-----        10/20/2026   3:21 PM                docs
d-----        10/20/2026   3:07 PM                logs
d-----        10/20/2026   3:19 PM                media
-a----        10/20/2026   2:40 PM            128 .env
-a----        10/20/2026   3:11 PM           1861 bai_lam_ngay1.md


    Directory: C:\Users\admin\Desktop\trung-tam-tieng-anh\archive

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/20/2026   2:43 PM              0 anh_lop_hoc.jpg
-a----        10/20/2026   2:43 PM              0 logo_trung_tam.png


    Directory: C:\Users\admin\Desktop\trung-tam-tieng-anh\data

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/20/2026   2:59 PM              0 hoc_vien_khoa_3.xlsx


    Directory: C:\Users\admin\Desktop\trung-tam-tieng-anh\docs

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/20/2026   2:44 PM              0 lich_hoc.txt


    Directory: C:\Users\admin\Desktop\trung-tam-tieng-anh\logs

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/20/2026   2:59 PM              0 access.log


    Directory: C:\Users\admin\Desktop\trung-tam-tieng-anh\media

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/20/2026   2:43 PM              0 anh_lop_hoc.jpg
-a----        10/20/2026   2:43 PM              0 logo_trung_tam.png

PS C:\Users\admin\Desktop\trung-tam-tieng-anh>
```

**Nhận xét:**

- Đã liệt kê toàn bộ file và thư mục trong dự án.
- Các file đã được sắp xếp vào đúng thư mục.
- Hai file `temp_201.tmp` và `temp_202.tmp` đã được xóa.
- File `.env` vẫn được giữ tại thư mục gốc trên máy.
- Thư mục `archive` chứa bản sao của logo và ảnh lớp học.

### Cấu trúc thư mục cần đạt sau khi hoàn thành

```text
trung-tam-tieng-anh/
│
├── docs/
│   └── lich_hoc.txt
│
├── media/
│   ├── logo_trung_tam.png
│   └── anh_lop_hoc.jpg
│
├── data/
│   └── hoc_vien_khoa_3.xlsx
│
├── logs/
│   └── access.log
│
├── archive/
│   ├── logo_trung_tam.png
│   └── anh_lop_hoc.jpg
│
├── bai_lam_ngay1.md
└── .env
```
# Tổng kết

Qua bài thực hành, em đã ôn tập các thao tác quản lý file và thư mục bằng GUI và CLI.

- Biết cách đổi tên file theo quy tắc snake_case.
- Biết cách tạo và tổ chức thư mục.
- Sử dụng `pwd` để xem đường dẫn tuyệt đối.
- Sử dụng `ls -Force` để liệt kê file ẩn.
- Sử dụng `cd` để di chuyển giữa các thư mục.
- Sử dụng `mv` để di chuyển file.
- Sử dụng `cp` để sao chép file.
- Sử dụng `rm` để xóa file.
- Hiểu và sử dụng đường dẫn tương đối `.` và `..`.
- Biết cách kiểm tra cấu trúc toàn bộ dự án bằng `ls -Recurse -Force`.
