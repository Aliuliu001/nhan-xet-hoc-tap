# Đề kiểm tra tối ưu cho NotebookLM phân tích

Mục tiêu: mỗi mục % NotebookLM tính **không cần suy đoán**, % đủ chi tiết để phân biệt được bé.

## Nguyên tắc
1. **Mỗi mục ≥ 15 câu** → 1 sai = ≤6.7%. 10 câu thì 1 sai = 10% → bé nào cũng 70/80/90%, không phân biệt.
2. **Bội số của 3** (9/15/18) → % làm tròn đẹp.
3. **Tách phần "hình ảnh" và "cách viết"** trong từ vựng → không phải suy % nữa.
4. **Đáp án kèm trong prompt** → NotebookLM chỉ việc đếm.

## Cấu trúc đề xuất (73 câu + thi nói)

| Mục | Số câu | 1 câu = | Lấy được |
|---|---|---|---|
| Từ vựng A – hình ảnh | 9 | 11.1% | % hình ảnh |
| Từ vựng B – cách viết từ | 9 | 11.1% | % cách viết (sắp xếp chữ / chính tả) |
| Nghe | 15 | 6.7% | % nghe |
| Đọc | 15 | 6.7% | % đọc |
| Viết | 10 | 10% | % viết (điền 4 từ + sắp xếp 6 câu) |
| Ngữ pháp | 15 | 6.7% | % ngữ pháp |
| Nói (thi miệng, riêng) | 5-6 tình huống | ×2 | % nói = điểm × 10 |
| Tổng | 73 | | /10 |

### Vì sao chia vậy
- **9+9**: hiện tại 1 câu xài cho 2 thứ → em phải đoán; tách ra NotebookLM trả 2 số thật.
- **15 câu cho Nghe/Đọc/Ngữ pháp**: 10 câu quá thô; 15 câu có 14/15=93.3%, 13/15=86.7% → thấy khác biệt.
- **Viết 10 mục cố định**: chấm theo từ khóa, không chấm tự do.
- **Nói tách thi miệng** (đã có cột Điểm bài KT nói).

## Prompt dán vào NotebookLM
```
BÀI KIỂM TRA THÁNG [X] – LỚP [TÊN]
Thời gian: [dd/mm - dd/mm]

=== BẢNG ĐIỂM (mỗi bé 1 dòng, đúng tên cột) ===
Họ tên | V-A hình ảnh (9) | V-B cách viết (9) | Nghe (15) | Đọc (15) | Viết (10) | Ngữ pháp (15) | Tổng (/10) | Nói (/10)
Nguyễn A | 8/9 | 7/9 | 14/15 | 13/15 | 7/10 | 12/15 | 8.4 | 8.5

=== BẢNG PHÂN TÍCH ===
Họ tên | Điểm mạnh | Điểm yếu | Lỗi phổ biến

=== ĐÁP ÁN ===
1A:B, 2A:A …

YÊU CẦU: Trả về đúng bảng, mỗi ô là số câu đúng/tổng, KHÔNG suy đoán, thiếu ghi "thiếu".
```

**Tên cột phải cố định y hệt** (copy prompt là chạy lại, không sửa). Trả về 2 bảng: bảng điểm + bảng điểm mạnh/yếu (dùng làm chất liệu 3 phần nhận xét).
