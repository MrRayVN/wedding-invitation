# Thiệp Cưới Online · Tấn Đạt & Lệ Quyên

> Hôn Lễ · Ngày 15 Tháng 05 Năm 2026 · Khánh Hòa

🔗 **Live URL**: https://mrrayvn.github.io/wedding-invitation/

---

## 📋 Cấu trúc

```
wedding-invitation/
├── index.html       (Single-page invitation site)
├── manifest.json    (PWA install)
└── README.md        (Hướng dẫn này)
```

**Tài nguyên (ảnh + nhạc) được reference cross-origin từ repo wedding-slideshow:**
`https://mrrayvn.github.io/wedding-slideshow/`

---

## 🎁 14 Sections

1. **Hero** — Monogram SVG + countdown đếm ngược đến giờ cưới
2. **Save the Date** — Visual calendar tháng 5/2026 với ngày 15 highlight
3. **Cô Dâu & Chú Rể** — Tên đầy đủ + bố mẹ
4. **Hành Trình** — Timeline 2021 → 2022 → 2025 → 2026
5. **Trân Trọng Kính Mời** — Lời mời truyền thống
6. **Lịch Trình** — 4 lễ với map link
7. **Dress Code** — Áo dài đỏ
8. **Album Cưới** — 8 ảnh grid + link slideshow
9. **RSVP** — Form xác nhận (cần setup Formspree)
10. **Mừng Cưới** — 2 QR VietQR Vietcombank + Agribank
11. **Sổ Lưu Niệm** — Form gửi lời chúc (cần setup Formspree)
12. **Live Stream** — Placeholder (cập nhật link gần ngày)
13. **Photo Upload** — Placeholder (cập nhật Google Drive folder)
14. **Footer** — Hashtag + Liên hệ

---

## ⚙️ Cần làm sau khi deploy

### 1. Setup Formspree cho RSVP form + Sổ lưu niệm

Hai form (RSVP và Guestbook) đang trỏ tới placeholder `REPLACE_WITH_YOUR_FORMSPREE_ID`. Cần:

1. Đăng ký tài khoản miễn phí tại https://formspree.io (50 submissions/tháng free)
2. Tạo form, lấy endpoint dạng: `https://formspree.io/f/xxxxxxxxxx`
3. Mở `index.html`, search `REPLACE_WITH_YOUR_FORMSPREE_ID`
4. Thay bằng ID thật (2 chỗ: form RSVP và form Sổ lưu niệm)
5. Commit + push

> Hoặc dùng Google Forms iframe embed nếu muốn không giới hạn submissions.

### 2. Live Stream link

Khi đã có link YouTube/Zoom live stream:
- Mở `index.html`, search `id="liveLink"`
- Thay `onclick="alert(...)..."` bằng `href="LINK_LIVESTREAM"`

### 3. Google Drive folder cho khách upload ảnh

Khi đã tạo folder Drive chia sẻ:
- Mở `index.html`, search `id="uploadLink"`
- Thay `onclick="alert(...)..."` bằng `href="LINK_GOOGLE_DRIVE_FOLDER"`

---

## 🎨 Design System

- **Background**: `#050407` (near-black)
- **Gold accent**: `#d4af6a` (chữ vàng kim)
- **Gold light**: `#f9e8c4` (highlight)
- **Red traditional**: `#b3262d` (dress code)
- **Fonts**:
  - Display: Playfair Display
  - Italic: Cormorant Garamond
  - Calligraphy: Great Vibes
  - Sans: Inter

---

## 🚀 Đồng bộ với wedding-slideshow

Site này KHÔNG host ảnh/nhạc riêng — tất cả load từ:
`https://mrrayvn.github.io/wedding-slideshow/`

Khi muốn đổi ảnh hero hoặc gallery, đổi đường dẫn ảnh trong `index.html`.
Format: `slide_XX_NAME.jpg` đúng theo repo slideshow.

---

## ❤️ Tính năng

- ✅ Countdown real-time
- ✅ Reveal animation on scroll (IntersectionObserver)
- ✅ Click STK → tự động copy
- ✅ QR VietQR chuyển khoản
- ✅ Background music toggle
- ✅ Responsive mobile
- ✅ PWA installable
- ✅ Open Graph share preview
- ✅ Film grain cinematic
- ✅ Light leaks animation
- ✅ Smooth scroll navigation

---

*Built with ♥ for Tấn Đạt & Lệ Quyên · 15.05.2026*
