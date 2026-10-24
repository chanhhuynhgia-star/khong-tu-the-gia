# Fonts

Các font mà `index.html` đang dùng. Trong `index.html`, cả ba font đã được nhúng sẵn dạng base64, nên trang không cần thư mục này để chạy; thư mục này để lưu và tái sử dụng.

| Tệp | Font gốc | Dùng cho | Ghi chú |
|---|---|---|---|
| `YanKaiSub.woff2` | 華康正顏楷體 W5 (DFYanKaiW5-B5), DynaComware | 原文 và các câu chữ Hán trích dẫn | Bản cắt gọn, chỉ gồm khoảng 1.145 chữ Hán có trong trang. Font thương mại của DynaComware; việc dùng và phân phối tuân theo giấy phép của người sở hữu. |
| `KmSerifSub-400.woff2` | Noto Serif Khmer, Regular | Toàn bộ phiên bản tiếng Khmer | Bản cắt gọn theo ký tự Khmer có trong trang. Giấy phép SIL Open Font License 1.1. |
| `KmSerifSub-600.woff2` | Noto Serif Khmer, SemiBold | Tiêu đề trong phiên bản tiếng Khmer | Như trên. |

Các font còn lại (chữ Việt, chữ Hán cho 白話 và tiêu đề) lấy từ font có sẵn trên máy người xem.

## Dùng trong CSS

```css
@font-face{font-family:"YanKaiSub";src:url(fonts/YanKaiSub.woff2) format("woff2");font-display:swap}
@font-face{font-family:"KmSerifSub";src:url(fonts/KmSerifSub-400.woff2) format("woff2");font-weight:400;font-display:swap}
@font-face{font-family:"KmSerifSub";src:url(fonts/KmSerifSub-600.woff2) format("woff2");font-weight:600 700;font-display:swap}
```

Vì là bản cắt gọn, các font này chỉ hiển thị được những ký tự có trong trang hiện tại. Khi thêm nội dung mới, cần cắt lại từ font gốc (ví dụ bằng `pyftsubset` của fontTools).
