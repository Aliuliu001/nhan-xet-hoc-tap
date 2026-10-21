---
name: student-feedback
version: 1.0.0
author: Ngọc Trương + Hermes
license: private
metadata:
  hermes:
    tags: [teaching, feedback, excel, vietnamese, education]
    related_skills: [student-monthly-comments, xlsx]
description: Use when writing monthly student feedback for 4 classes.
---

# Nhận xét học tập tháng (Student Feedback)

## When to Use (Khi nào dùng)
Viết nhận xét tháng cho 4 lớp: Pumpkin Seed → Pineapple → Tiramisu → Cashew.
Form này thầy Trương duyệt ngày 19/10/2026, áp dụng **Tháng 10/2026 trở đi**, cả 4 lớp.

## Dữ liệu thầy Trương gửi
1. **Điểm chi tiết**: điểm bài KT giấy, điểm bài KT nói, % bài kiểm tra (từ vựng, nghe, đọc, viết, ngữ pháp, tổng /10)
2. **Ghi chú cá nhân từng bé**: tính cách, thái độ học, vấn đề đặc biệt (1-2 dòng/bé)

Thiếu phần nào → hỏi lại. **% từ vựng em tự suy** từ điểm + bảng phân tích điểm mạnh/yếu (thầy đã duyệt).

## Form 3 phần (mẫu đã duyệt)

### 1. Từ vựng (1 đoạn)
Quy tắc: % hình ảnh = % từ vựng trong bài kiểm tra; % cách viết từ = trung bình(% từ vựng, % kỹ năng viết), làm tròn 5.
Cấu trúc: *% hình ảnh → đánh giá phát âm → % cách viết từ → lý do cụ thể (sai chính tả / thừa thiếu chữ / viết theo cách nói).*

`Ở unit này con nhớ khoảng 85-90% số từ vựng ở dạng hình ảnh, con phát âm tốt và rõ ràng. Con thuộc khoảng 70-75% cách viết từ, nhưng đôi khi con viết còn sai chính tả hoặc nhầm lẫn số ít số nhiều.`

### 2. Skills (mỗi kỹ năng 1 đoạn riêng, có % + GIẢI THÍCH TẠI SAO)
```
Kỹ năng nói: (X%) …
Kỹ năng nghe: (X%) …
Kỹ năng đọc: (X%) …
Kỹ năng viết: (X%) …
Ngữ pháp (X%): …
```
Mỗi đoạn nêu **điểm mạnh + nguyên nhân/khó khăn cụ thể của bé đó**, không chung chung. Đề viết & nghe ghi chung chung (bài viết của con / bài nghe).

### 3. Nhận xét chung (dài, cá nhân hóa)
Bố cục: **điểm mạnh → vấn đề → nguyên nhân → xu hướng → lời khuyên cho con**.
Cuối bài có thể thêm đoạn `Kính nhờ quý Phụ Huynh …` — **chỉ cho bé giảm nhiều ở 2-3 kỹ năng**.
Lấy chất liệu từ ghi chú của thầy (tính cách, thái độ, vấn đề riêng) — mẫu đã duyệt: Hân (mất động lực), Khôi (mặt chữ), Đăng (chăm viết), Nguyên (nói nhanh nuốt chữ).

## TUYỆT ĐỐI KHÔNG ĐƯỢC (tự check trước khi giao)
- Chữ "thầy" / "cô" → dùng "con"
- Chữ "soát bài" → đổi thành "kiểm tra" (dặn 20/10/2026)
- Số câu đúng/tổng số câu (chỉ hiện %)
- Điểm nói dạng X/10 → chỉ hiện %
- So sánh % với tháng 8/tháng trước
- Nhầm tên bé (trùng tên → hỏi thầy đặt tên gọi riêng)
- Lặp lại cấu trúc câu y hệt giữa các bé

## Xuất file
Excel `.xlsx` header: `STT | Ca | Tháng | Full_name | Class | Từ ngày | Đến ngày | Điểm bài KT giấy | Điểm bài KT nói | Từ vựng | Skills | Nhận xét chung`
- Header fill #4472C4, chữ trắng bold, border mỏng, word wrap, cột J/K/L width 60, hàng ~120
- Điểm giữ dạng số
- Kèm bản `.md` để thầy đọc nhanh trên Telegram

## Quy trình từng lớp
Nhận điểm + ghi chú → viết 7 bé theo form → tự check mục cấm → xuất Excel + md → hỏi thầy góp ý → sửa → sang lớp kế

## Đề kiểm tra tối ưu
Cấu trúc số câu để NotebookLM lọc % tự động: xem `references/de-kiem-tra.md`.