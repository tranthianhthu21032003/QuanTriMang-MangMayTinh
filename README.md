# 📘 Windows Server Update Services (WSUS) Project

> 📚 Đồ án nghiên cứu và triển khai hệ thống WSUS trong môi trường doanh nghiệp

---

## 📖 Mục lục

- [1. Lý thuyết đề tài](#1-lý-thuyết-đề-tài)
  - [1.1 Định nghĩa và chức năng cơ bản của WSUS](#11-định-nghĩa-và-chức-năng-cơ-bản-của-wsus)
  - [1.2 Lợi ích và ý nghĩa trong doanh nghiệp](#12-lợi-ích-và-ý-nghĩa-trong-doanh-nghiệp)
  - [1.3 Kiến trúc của WSUS](#13-kiến-trúc-của-wsus)
    - [1.3.1 Các thành phần chính](#131-các-thành-phần-chính)
    - [1.3.2 Luồng hoạt động cập nhật](#132-luồng-hoạt-động-cập-nhật)
    - [1.3.3 Cơ sở dữ liệu WSUS](#133-cơ-sở-dữ-liệu-wsus)
    - [1.3.4 Group Policy, GPO, Active Directory](#134-group-policy-gpo-active-directory)
  - [1.4 Vai trò của WSUS](#14-vai-trò-của-wsus)
  - [1.5 Clean Up trong WSUS](#15-clean-up-trong-wsus)
  - [1.6 Quy trình cập nhật](#16-quy-trình-cập-nhật)
    - [1.6.1 Quy trình cập nhật WSUS](#161-quy-trình-cập-nhật-wsus)
    - [1.6.2 Phân phối cập nhật](#162-phân-phối-cập-nhật)

- [2. Thực hành](#2-thực-hành)
  - [2.1 Mô hình mạng](#21-mô-hình-mạng)
  - [2.2 Yêu cầu đề tài](#22-yêu-cầu-đề-tài)
    - [2.2.1 Yêu cầu](#221-yêu-cầu)
    - [2.2.2 Chuẩn bị](#222-chuẩn-bị)

- [3. Hướng dẫn thực hành](#3-hướng-dẫn-thực-hành)
  - [3.1 Cấu hình IPv4](#31-cấu-hình-ipv4)

---

## 1. Lý thuyết đề tài

### 1.1 Định nghĩa và chức năng cơ bản của WSUS
**WSUS (Windows Server Update Services)** là dịch vụ của Microsoft cho phép quản trị viên quản lý và phân phối các bản cập nhật cho hệ điều hành Windows trong mạng nội bộ.

### 1.2 Lợi ích và ý nghĩa trong doanh nghiệp
- 🔹 Giảm băng thông internet
- 🔹 Quản lý cập nhật tập trung
- 🔹 Tăng cường bảo mật hệ thống
- 🔹 Kiểm soát nội dung và thời điểm cập nhật

### 1.3 Kiến trúc của WSUS

#### 1.3.1 Các thành phần chính
- WSUS Server  
- Client Machines  
- Database  
- Update Source (Microsoft Update)  

#### 1.3.2 Luồng hoạt động cập nhật
WSUS Server tải bản cập nhật từ Microsoft và phân phối đến các máy client dựa trên chính sách đã cấu hình.

#### 1.3.3 Cơ sở dữ liệu WSUS
Lưu trữ thông tin về:
- Bản cập nhật  
- Trạng thái client  
- Cấu hình hệ thống  

#### 1.3.4 Group Policy, GPO, Active Directory
Sử dụng để cấu hình và quản lý cách các client nhận cập nhật từ WSUS Server.

### 1.4 Vai trò của WSUS
- ✅ Quản lý cập nhật tập trung  
- ✅ Tăng tính bảo mật  
- ✅ Tiết kiệm tài nguyên mạng  

### 1.5 Clean Up trong WSUS
Giúp:
- Xóa các bản cập nhật không cần thiết  
- Giải phóng dung lượng  
- Tăng hiệu suất hệ thống  

### 1.6 Quy trình cập nhật

#### 1.6.1 Quy trình cập nhật WSUS
1. Đồng bộ bản cập nhật từ Microsoft  
2. Phê duyệt cập nhật  
3. Triển khai đến client  

#### 1.6.2 Phân phối cập nhật
WSUS phân phối bản cập nhật đến server và client dựa trên chính sách đã thiết lập.

---

## 2. Thực hành
