---
title: "Thiết Kế Kiến Trúc Phần Mềm"
subject: "Học phần: Thiết kế Kiến trúc Phần mềm"
author: "Pham Viet Loi"
date: "2026-01-05"
version: "1.0"
status: "Final"
---

# 📐 THIẾT KẾ KIẾN TRÚC PHẦN MỀM

---

## 📌 1. Giới thiệu

Tài liệu này mô tả **thiết kế kiến trúc phần mềm** cho một hệ thống ứng dụng tổng quát, nhằm minh họa cách phân tích, lựa chọn và trình bày kiến trúc theo các nguyên tắc chuẩn trong môn học *Thiết kế Kiến trúc Phần mềm*.

Mục tiêu chính của tài liệu là:
- Áp dụng các khái niệm kiến trúc phần mềm
- Phân tích yêu cầu và ràng buộc hệ thống
- Đề xuất kiến trúc phù hợp
- Đảm bảo tính mở rộng, bảo trì và hiệu năng

---

## 🎯 2. Mục tiêu hệ thống

- Xây dựng kiến trúc rõ ràng, có cấu trúc
- Phân tách trách nhiệm giữa các thành phần
- Đảm bảo hệ thống dễ mở rộng và bảo trì
- Giảm sự phụ thuộc chặt chẽ giữa các module
- Hỗ trợ phát triển và nâng cấp trong tương lai

---

## 🧾 3. Phạm vi hệ thống

Hệ thống được thiết kế nhằm:
- Quản lý dữ liệu người dùng
- Xử lý nghiệp vụ cốt lõi
- Cung cấp giao diện cho người dùng cuối
- Đảm bảo tính ổn định và an toàn thông tin

**Ngoài phạm vi:**
- Tối ưu phần cứng
- Triển khai hạ tầng chi tiết
- Tối ưu hiệu năng ở mức hệ điều hành

---

## 👥 4. Các bên liên quan (Stakeholders)

| Nhóm | Vai trò |
|----|-------|
| Người dùng | Sử dụng hệ thống |
| Nhà phát triển | Xây dựng & bảo trì |
| Giảng viên | Đánh giá kiến trúc |
| Quản lý | Ra quyết định kỹ thuật |

---

## 📋 5. Yêu cầu hệ thống

### 5.1 Yêu cầu chức năng
- Đăng nhập / đăng xuất
- Quản lý thông tin người dùng
- Xử lý nghiệp vụ chính
- Lưu trữ và truy xuất dữ liệu

### 5.2 Yêu cầu phi chức năng
- Khả năng mở rộng
- Tính bảo trì
- Tính sẵn sàng
- Hiệu năng
- Bảo mật

---

## 🧱 6. Tổng quan kiến trúc hệ thống

### 6.1 Phong cách kiến trúc lựa chọn

Hệ thống áp dụng **kiến trúc phân lớp (Layered Architecture)**, bao gồm:

- Presentation Layer
- Application Layer
- Business Logic Layer
- Data Access Layer

Phong cách này giúp:
- Dễ hiểu
- Dễ bảo trì
- Phù hợp với hệ thống quản lý

---

## 🏗️ 7. Mô tả các thành phần

### 7.1 Presentation Layer
- Giao diện người dùng
- Nhận input và hiển thị output
- Không xử lý logic nghiệp vụ

### 7.2 Application Layer
- Điều phối luồng xử lý
- Giao tiếp giữa UI và nghiệp vụ

### 7.3 Business Logic Layer
- Xử lý nghiệp vụ cốt lõi
- Áp dụng các quy tắc hệ thống

### 7.4 Data Access Layer
- Truy xuất dữ liệu
- Giao tiếp với hệ quản trị CSDL

---

## 🔄 8. Luồng hoạt động tổng quát

```text
Người dùng
   ↓
Giao diện
   ↓
Xử lý ứng dụng
   ↓
Nghiệp vụ
   ↓
Cơ sở dữ liệu
