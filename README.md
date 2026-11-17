# 📅 Công cụ tính lịch hẹn bệnh nhân

> Công cụ web tự động hóa chia nhóm bệnh nhân và xếp lịch hẹn tái khám theo chu kỳ, loại trừ ngày cuối tuần và ngày lễ.

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Author](https://img.shields.io/badge/Author-BS.%20Phạm%20Văn%20Thái-1e40af)]()

---

## 📖 Thông báo miễn trừ trách nhiệm

**Công cụ được bác sĩ Thái phát triển, đang trong quá trình thử nghiệm giao đoạn alpha, nên có thể còn lỗi xảy ra. Vui lòng kiểm tra lại kĩ lịch hẹn trước khi quyết định sử dụng**

---

## ✨ Tính năng

### 🎯 Nhập liệu linh hoạt
- **Nhập A (tổng số BN)** và chọn tính theo **B (số BN/nhóm)** hoặc **C (số nhóm)** — hệ thống tự động tính giá trị còn lại.
- Tự động điều chỉnh **C'** khi A không chia hết cho B, kèm cảnh báo minh bạch.
- Ngày bắt đầu tùy chọn; nếu rơi vào ngày nghỉ sẽ **tự động nhảy sang ngày làm việc kế tiếp**.
- Hỗ trợ xếp lịch **nhiều năm** (tối đa 20 năm) — mỗi năm một sheet Excel riêng.

### 🗓️ Quản lý ngày nghỉ thông minh
- Tự động loại bỏ **thứ Bảy và Chủ nhật**.
- Nhập ngày lễ theo 2 dạng:
  - Từng ngày: `01/01/2026`
  - Khoảng ngày: `30/04/2026 - 04/05/2026`
- Tự động **loại bỏ trùng lặp**, kiểm tra định dạng, giới hạn độ dài khoảng (≤ 366 ngày).
- Báo lỗi chi tiết theo từng dòng nếu có sai sót.

### 📊 Xuất Excel chuyên nghiệp
- File `.xlsx` chuẩn, mở được bằng **Excel, LibreOffice, Google Sheets**.
- **Mỗi năm một sheet** (`Năm 2026`, `Năm 2027`, …) hiển thị bảng lịch hẹn dạng ma trận.
- **Sheet `Báo cáo` đặt cuối cùng**, tổng hợp đầy đủ thông tin: cấu hình, thống kê, cảnh báo, danh sách ngày nghỉ đã áp dụng.
- **Định dạng chuyên nghiệp**: tiêu đề màu, section header, border, font, căn lề, chiều cao dòng tự động.

### 🖨️ In ấn tiện lợi
- Nút **"In năm này"** xuất bảng của năm đang chọn ra **A4 nằm ngang**.
- Bản in có header đầy đủ (tên công cụ, tác giả, cấu hình) — ẩn giao diện điều khiển.

### ⚡ Hiệu năng và trải nghiệm
- **Single-pass algorithm**: xử lý toàn bộ lịch một lần, không lặp lại theo năm.
- **Cache HTML** theo năm → chuyển tab tức thì.
- **Dirty state**: cảnh báo khi dữ liệu thay đổi sau khi đã xem trước → tránh xuất nhầm.
- **Phím tắt `Ctrl + Enter`** để xem trước nhanh.
- Giao diện **responsive**, hoạt động tốt trên mobile.
