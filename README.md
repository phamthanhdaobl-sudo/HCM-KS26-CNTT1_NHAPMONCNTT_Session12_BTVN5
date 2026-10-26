# NetGuard — Session12 Ex05

## Thành phần
- `NetGuard_Incident_Log.xlsx`: nhật ký hệ thống + cơ sở dữ liệu virus; AutoFilter và công thức VLOOKUP/TRIM.
- `NetGuard_Incident_Report.docx`: báo cáo sự cố, Heading và trường mục lục tự động.
- `NetGuard_Defense_3_Layers.pptx`: slide phòng thủ 3 tầng, Montserrat/Inter, không dùng Times New Roman.

## Phần 1 — AutoFilter là “Google Search” của bảng tính
AutoFilter đặt bộ lọc ở hàng tiêu đề, giúp tìm/lọc nhanh theo mã độc, thiết bị, thời gian hoặc mức độ. Ví dụ lọc cột **Mức độ** bằng **Nghiêm trọng** để xem sự cố ưu tiên cao, hoặc lọc cột **Mã độc thô** để rà một họ mã độc. Có thể kết hợp điều kiện và xóa bộ lọc để hiện lại mọi dòng; dữ liệu bị ẩn không bị xóa. Khác Google Search, AutoFilter chỉ tìm trong vùng dữ liệu được chọn, không tìm trên Internet.

## Phần 2 — Triển khai
### Excel
- Sheet `Nhat ky he thong`: cảnh báo thô, mã độc chuẩn hóa và kết quả tra cứu.
- Sheet `Co so du lieu virus`: mã độc chuẩn, tên hiển thị và khuyến nghị.
- Công thức ví dụ: `=IFERROR(VLOOKUP(TRIM(D2),'Co so du lieu virus'!$A$2:$C$20,2,FALSE),"Chưa xác định")`
- `TRIM(D2)` loại bỏ khoảng trắng thừa; `FALSE` yêu cầu khớp chính xác; `IFERROR` gắn nhãn giá trị chưa có trong từ điển.

### Word
Mở bằng Microsoft Word, nhấp phải mục lục > **Update Field** > **Update entire table** để cập nhật số trang. Có thể nhấn `Ctrl+A`, rồi `F9` để cập nhật các trường.

### PowerPoint
Sơ đồ phân cấp thể hiện Tầng 1 Phòng ngừa, Tầng 2 Phát hiện, Tầng 3 Ứng phó & phục hồi. Font thiết kế Montserrat và Inter; nếu máy trình chiếu thiếu font, cài font hoặc thay bằng sans-serif tương đương rồi kiểm tra bố cục.

## Lưu ý
Dữ liệu trong gói là **minh họa phục vụ bài tập**, không đại diện cho cuộc điều tra an ninh mạng thực tế. Đổi tên ZIP theo mẫu `[Tên Lớp]_[Môn Học]_Session10_Ex05` trước khi nộp.
