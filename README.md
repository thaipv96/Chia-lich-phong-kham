# 📅 Công cụ tính lịch hẹn bệnh nhân

![Version](https://img.shields.io/badge/version-v5.0--beta-0b57d0?style=flat-square)
![Status](https://img.shields.io/badge/trạng_thái-Đang_thử_nghiệm_(Beta)-fbbc04?style=flat-square)
![Platform](https://img.shields.io/badge/nền_tảng-Single--File_HTML5_%7C_Offline-34a853?style=flat-square)
![UI](https://img.shields.io/badge/giao_diện-Google_Material_Design_3-4285f4?style=flat-square)

**Công cụ tính lịch hẹn bệnh nhân** được thiết kế nhằm hỗ trợ bác sĩ, điều dưỡng và nhân viên hành chính y tế phân nhóm và lập lịch tái khám định kỳ cho số lượng lớn bệnh nhân một cách tự động, trực quan và chính xác.

---

> [!WARNING]
> **THÔNG BÁO PHIÊN BẢN ĐANG TRONG QUÁ TRÌNH THỬ NGHIỆM (BETA)**
>
> Phiên bản hiện tại (**v5.0-beta**) đang trong giai đoạn thử nghiệm và hoàn thiện tính năng. Các thuật toán chia nhóm, tính giãn cách ngày tái khám và xuất tệp Excel đang tiếp tục được kiểm thử trên nhiều kịch bản thực tế khác nhau.
> - Vui lòng **kiểm tra và đối chiếu lại bảng lịch xuất ra** trước khi áp dụng chính thức cho công tác điều hành phòng khám hoặc cấp phát thuốc ngoại trú.
> - Nếu phát hiện sai sót tính toán, lỗi hiển thị hoặc có đề xuất cải tiến, vui lòng tạo **Issue** trực tiếp trên kho GitHub này để tác giả cập nhật.

---

## 🚀 Hướng dẫn sử dụng

### 1. Thiết lập thông số xếp lịch (Cột bên trái)
| Tham số | Ký hiệu | Ý nghĩa & Cách nhập |
| :--- | :---: | :--- |
| **Tổng số bệnh nhân** | `A` | Tổng số bệnh nhân cần quản lý/xếp lịch (đánh số liên tục từ `1` đến `A`, mặc định `1300`). |
| **Định mức mỗi ngày** | `B` | Số lượng bệnh nhân khám tối đa trong 1 ngày làm việc (mặc định `50` BN/ngày). |
| **Số nhóm chia** | `C` | Số nhóm tiêu chuẩn. Khi thay đổi `B` hoặc `C`, hệ thống tự động đồng bộ tham số còn lại. |
| **Ngày bắt đầu / kết thúc** | — | Khoảng thời gian áp dụng lịch hẹn (mặc định tính 01 năm kể từ ngày hiện tại). |
| **Ngày nghỉ cần bỏ qua** | — | Nhập từng dòng theo định dạng `dd/mm/yyyy` hoặc `dd/mm/yyyy - dd/mm/yyyy` (có thể kèm ghi chú trong ngoặc đơn), hoặc bấm **`+ Chọn lịch`** để thêm nhanh. |

### 2. Xem kết quả, tra cứu và xuất dữ liệu (Khu vực bên phải)
1. **Xem lịch hẹn:** Chọn tab **Bảng lịch hẹn** để theo dõi ngày khám dự kiến của từng nhóm và số ngày giãn cách giữa các lần hẹn.
2. **Tra cứu bệnh nhân:** Gõ số thứ tự bệnh nhân vào ô **`Tra cứu STT bệnh nhân...`** ở góc trên bên phải bảng để tìm nhanh nhóm khám tương ứng.
3. **Kiểm tra thống kê:** Chuyển sang tab **Báo cáo** để rà soát bảng tổng hợp số ngày làm việc, số ngày nghỉ lễ/cuối tuần đã loại trừ theo từng năm.
4. **Xuất file & In ấn:**
   - Bấm **`Xuất Excel (.xlsx)`** trên thanh tiêu đề để tải bảng lịch hoàn chỉnh về máy.
   - Bấm **`In bảng lịch hẹn`** để in trực tiếp ra giấy khổ A4 ngang.

---

## ⚠️ Thông báo miễn trừ trách nhiệm (Disclaimer)

1. **Mục đích hỗ trợ hành chính:** Công cụ này được phát triển nhằm mục đích hỗ trợ tính toán, phân bổ và sắp xếp lịch hẹn hành chính định kỳ. Đây **không phải là phần mềm y tế chuyên dụng (SaMD)** và không thay thế cho hệ thống quản lý bệnh viện (HIS) hay bệnh án điện tử (EMR).
2. **Không thay thế quyết định lâm sàng:** Khoảng cách giữa các lần tái khám được tính toán thuần túy dựa trên phép chia toán học và lịch hành chính. Bác sĩ điều trị cần căn cứ vào tình trạng lâm sàng cụ thể của từng người bệnh, phác đồ chuyên môn và quy định kê đơn/cấp phát thuốc bảo hiểm y tế hiện hành để hẹn tái khám phù hợp.
3. **Trách nhiệm sử dụng:** Tác giả cung cấp mã nguồn theo nguyên trạng (*"AS IS"*). Người sử dụng tự chịu trách nhiệm kiểm tra tính chính xác của dữ liệu đầu vào, danh sách ngày nghỉ lễ theo quy định từng năm và rà soát kết quả đầu ra trước khi áp dụng trong thực tế.

---

## 👨‍💻 Tác giả

- **Phát triển bởi:** Bác sĩ Phạm Văn Thái
- **Giấy phép:** Mã nguồn mở phục vụ mục đích học tập, nghiên cứu và hỗ trợ công tác quản lý y tế.
