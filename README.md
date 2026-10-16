# 3 bài tập Windows Forms (C#, .NET 8)

Mỗi bài là một project riêng trong một thư mục riêng. Mở file `.csproj` bằng Visual Studio 2022 (workload ".NET desktop development") rồi nhấn F5.

| Thư mục | Ứng dụng |
|---|---|
| Bai1_ClinicAppointmentManager | Quản lý lịch hẹn phòng khám |
| Bai2_LabEquipmentCheckout | Quản lý mượn trả thiết bị phòng thực hành |
| Bai3_RepairServiceTracker | Quản lý đơn đăng ký dịch vụ sửa chữa |

Giao diện được dựng hoàn toàn bằng code trong `MainForm.cs` (không có file Designer), nên không cần kéo thả control.

## Kiểm thử thủ công tối thiểu

### Bài 1
1. Nhập SĐT `12345` → bấm Thêm → ErrorProvider báo lỗi cạnh ô SĐT, không lưu.
2. Chọn ngày hẹn là hôm qua → bấm Thêm → báo lỗi cạnh ô ngày giờ.
3. Gõ `0987` vào ô tìm kiếm → chỉ còn lịch hẹn có SĐT chứa `0987`.
4. Sửa trạng thái, xóa một lịch, đổi bộ lọc → bảng và StatusStrip cập nhật số lượng.

### Bài 2
1. Chọn hạn trả trước ngày mượn → Thêm → báo lỗi cạnh ô Hạn trả.
2. Dòng PM002 (hạn trả đã qua, chưa trả) hiển thị "Quá hạn" và tô màu đỏ nhạt.
3. Chọn PM002 → "Đánh dấu đã trả" → tình trạng đổi thành "Đã trả", ngày trả = hôm nay, số phiếu quá hạn trên StatusStrip giảm 1.

### Bài 3
1. Nhập chi phí `-500` hoặc để trống mô tả lỗi → Thêm → báo lỗi, không lưu.
2. Chọn ảnh có tỷ lệ dài/rộng bất kỳ → ảnh hiển thị không bị méo (Zoom).
3. Đổi trạng thái đơn SC001 sang "Hoàn tất" hoặc sửa chi phí → tổng chi phí trên StatusStrip thay đổi.
