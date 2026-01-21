# Giải mã HEX sang Text - Chrome Extension

Extension Chrome (Manifest V3) mạnh mẽ giải mã chuỗi hexadecimal sang văn bản với **3 chế độ hoạt động song song**:

1. **Chế độ Inline** - Bôi đen HEX trên trang → nút giải mã → hiện kết quả tại chỗ
2. **Chế độ Popup** - Click icon extension → dán HEX → giải mã trong popup
3. **Chế độ Chuột phải** - Bôi đen HEX → chuột phải → chọn "Giải mã HEX"

Extension cung cấp giải mã HEX nhanh chóng, trực quan với **phát hiện URL**, **hỗ trợ ẩn danh**, **dark mode**, và **UX hiện đại**.

## ✨ Tính năng

- **🎯 3 Chế độ Hoạt động**
  - Giải mã bôi đen inline
  - Giải mã thủ công qua popup  
  - Menu chuột phải trên văn bản đã chọn
  
- **🔓 Giải mã Thông minh**
  - Hỗ trợ ASCII & UTF-8
  - Xử lý khoảng trắng và xuống dòng
  - Hỗ trợ ký tự đa byte (Tiếng Việt, emoji, v.v.)
  
- **🔗 Phát hiện URL**
  - Tự động phát hiện URL trong văn bản đã giải mã
  - Mở trong tab thường
  - Mở trong chế độ ẩn danh
  
- **🎨 UX Hiện đại**
  - UI bong bóng nổi
  - Hỗ trợ dark mode
  - Animation mượt mà
  - Tự động đóng
  
- **🔒 Ưu tiên Bảo mật**
  - Xử lý hoàn toàn local
  - Không gửi dữ liệu ra ngoài
  - Hoạt động offline hoàn toàn

## 📦 Cài đặt

### Load Extension (Chế độ Developer)

1. **Mở trang Chrome Extensions**
   - Truy cập `chrome://extensions/`
   - Hoặc Menu → Công cụ khác → Tiện ích mở rộng

2. **Bật chế độ Developer**
   - Bật công tắc "Chế độ nhà phát triển" ở góc trên bên phải

3. **Load Extension**
   - Click "Tải tiện ích mở rộng đã giải nén"
   - Chọn thư mục `hex2text`
   - Extension sẽ xuất hiện trên toolbar

4. **(Tùy chọn) Bật chế độ ẩn danh**
   - Click "Chi tiết" trên thẻ extension
   - Bật "Cho phép trong chế độ ẩn danh"

## 🚀 Cách sử dụng

### Chế độ Inline

1. Truy cập bất kỳ trang web nào
2. Bôi đen văn bản HEX (ví dụ: `48656c6c6f20576f726c64`)
3. Click nút "🔓 Giải mã HEX" xuất hiện
4. Xem kết quả trong bong bóng
5. Nếu kết quả là URL, click "Mở link" hoặc "Mở ẩn danh"

### Chế độ Popup

1. Click icon extension trên toolbar
2. Dán chuỗi HEX vào textarea
3. Click nút "Giải mã"
4. Xem kết quả và tùy chọn sao chép hoặc mở URL

### Chế độ Chuột phải (MỚI)

1. Bôi đen văn bản HEX trên bất kỳ trang web nào
2. Click chuột phải
3. Chọn "🔓 Giải mã HEX" trong menu
4. Bong bóng kết quả sẽ xuất hiện

## 📝 Ví dụ

### Văn bản cơ bản
```
Input:  48656c6c6f20576f726c64
Output: Hello World
```

### URL
```
Input:  68747470733a2f2f676f6f676c652e636f6d
Output: https://google.com
```

### UTF-8 (Tiếng Việt)
```
Input:  5869e1baa720636861cc8820566965cc82744e616d
Output: Xin chào Việt Nam
```

### HEX nhiều dòng
```
Input:  48 65 6c 6c 6f
        57 6f 72 6c 64
Output: HelloWorld
```

## 🔧 Chi tiết kỹ thuật

- **Phiên bản Manifest**: V3
- **Quyền**: `tabs`, `scripting`, `activeTab`, `contextMenus`
- **Quyền Host**: `<all_urls>`
- **Content Script**: Inject vào tất cả trang
- **Background**: Service worker

## 🐛 Xử lý sự cố

### Chế độ ẩn danh không hoạt động
- Vào `chrome://extensions/`
- Tìm "Giải mã HEX sang Text"
- Click "Chi tiết"
- Bật "Cho phép trong chế độ ẩn danh"

### Chế độ inline không xuất hiện
- Đảm bảo văn bản bôi đen là HEX hợp lệ
- Kiểm tra console trình duyệt xem có lỗi
- Reload lại trang

### Popup không giải mã
- Xác minh định dạng HEX đúng
- Phải có số chẵn ký tự hex
- Chỉ cho phép 0-9, a-f, A-F

### Menu chuột phải không xuất hiện
- Phải bôi đen văn bản trước
- Reload extension
- Kiểm tra quyền `contextMenus`

## 📄 Giấy phép

MIT License - Thoải mái sử dụng và chỉnh sửa!
