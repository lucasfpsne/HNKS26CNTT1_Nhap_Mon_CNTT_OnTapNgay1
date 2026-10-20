# BÀI LÀM – ÔN TẬP NGÀY 1

- **Họ tên:Nguyễn Đặng Hoàng Minh**
- **Lớp HN_KS26_CNTT1:**
- **Link repository:https://github.com/lucasfpsne/HNKS26CNTT1_Nhap_Mon_CNTT_OnTapNgay1**
- **Hệ điều hành (Windows/macOS):Windows**

## Phần A. Tổ chức thư mục bằng GUI

> Phần A được chấm qua kết quả B1 (tên thư mục gốc) và kết quả liệt kê toàn bộ dự án B8 ở Phần B, không cần ghi thêm ở đây.

## Phần B. Thao tác bằng CLI

### Các lệnh đã chạy (B1–B7)

```shell
# B1
pwd

# B2
ls -Force

# B3
mv .\lich_hoc.txt .\docs\
mv .\logo_trung_tam.png .\media\
mv .\anh_lop_hoc.jpg .\media\

# B4
cp .\media\logo_trung_tam.png .\archive\

# B5
rm .\temp_201.tmp
rm .\temp_202.tmp

# B6
cd .\logs\
ls -Force
cd ..

# B7
cd .\docs\
cp ..\media\anh_lop_hoc.jpg ..\archive\
cd ..

```

### Kết quả B1 (pwd)

```text
Path
----
C:\Users\admin\Desktop\trung-tam-tieng-anh

```

### Kết quả liệt kê toàn bộ dự án – B8 (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
PS C:\Users\admin\Desktop\trung-tam-tieng-anh> Get-ChildItem -Recurse -Force

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

## Tự chấm (điền sau khi có đáp án)

- **Điểm tự chấm:** ..../100
- **Lỗi mình đã mắc và cách sửa:**