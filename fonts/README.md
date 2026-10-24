# Fonts

Các font mà `index.html` đang dùng. Trong `index.html`, cả ba font đã được nhúng sẵn dạng base64, nên trang không cần thư mục này để chạy; thư mục này để lưu và tái sử dụng.

| Tệp | Font gốc | Dùng cho | Ghi chú |
|---|---|---|---|
| `YanKaiSub.woff2` | 華康正顏楷體 W5 (DFYanKaiW5-B5), DynaComware | 原文, câu chữ Hán trích dẫn, tiêu đề lớn và tiêu đề cảnh (phiên bản 中文) | Bản cắt gọn, gồm khoảng 1.850 chữ Hán và dấu câu có trong trang. Font thương mại của DynaComware; việc dùng và phân phối tuân theo giấy phép của người sở hữu. |
| `KaiShuSub.woff2` | 華康楷書體 W5 (P) (DFPKaiShuW5-B5), DynaComware | Chữ Khải: tiêu đề, nhãn chữ Hán, bản đồ, thanh chặng, chữ đề trên tranh; toàn bộ phiên bản 中文 | Bản cắt gọn, gồm khoảng 1.850 chữ Hán và dấu câu có trong trang. Font thương mại của DynaComware; việc dùng và phân phối tuân theo giấy phép của người sở hữu. |
| `FangSongSub.woff2` | 華康仿宋體 W4 (DFFangSongW4-B5), DynaComware | Chữ phụ: chú thích «按：…» trong 白話, số trang «第 N 頁», nhãn 原文/白話, tên chương; trong phiên bản 中文 thêm chú thích tranh, dòng mô tả, hướng dẫn, ghi chú, nguồn | Bản cắt gọn, gồm khoảng 1.850 chữ Hán và dấu câu có trong trang. Font thương mại của DynaComware; việc dùng và phân phối tuân theo giấy phép của người sở hữu. |
| `GuYinSub.woff2` | 華康古印體 (DFGuYinMedium-B5), DynaComware | Con dấu «孔子世家» trên thanh đầu trang | Bản cắt gọn chỉ gồm 4 chữ 孔子世家. Font thương mại của DynaComware; việc dùng và phân phối tuân theo giấy phép của người sở hữu. |
| `KmSerifSub-400.woff2` | Noto Serif Khmer, Regular | Toàn bộ phiên bản tiếng Khmer | Bản cắt gọn theo ký tự Khmer có trong trang. Giấy phép SIL Open Font License 1.1. |
| `KmSerifSub-600.woff2` | Noto Serif Khmer, SemiBold | Tiêu đề trong phiên bản tiếng Khmer | Như trên. |

Chữ Việt lấy từ font có sẵn trên máy người xem.

## Dùng trong CSS

```css
@font-face{font-family:"GuYinSub";src:url(fonts/GuYinSub.woff2) format("woff2");font-display:swap}
@font-face{font-family:"FangSongSub";src:url(fonts/FangSongSub.woff2) format("woff2");font-display:swap}
@font-face{font-family:"KaiShuSub";src:url(fonts/KaiShuSub.woff2) format("woff2");font-display:swap}
@font-face{font-family:"YanKaiSub";src:url(fonts/YanKaiSub.woff2) format("woff2");font-display:swap}
@font-face{font-family:"KmSerifSub";src:url(fonts/KmSerifSub-400.woff2) format("woff2");font-weight:400;font-display:swap}
@font-face{font-family:"KmSerifSub";src:url(fonts/KmSerifSub-600.woff2) format("woff2");font-weight:600 700;font-display:swap}
```

Vì là bản cắt gọn, các font này chỉ hiển thị được những ký tự có trong trang hiện tại. Khi thêm nội dung mới, cần cắt lại từ font gốc (ví dụ bằng `pyftsubset` của fontTools).
