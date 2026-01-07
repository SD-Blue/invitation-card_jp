# Hướng dẫn cập nhật đa ngôn ngữ cho thiệp cưới

## Đã hoàn thành
✅ Tạo file `js/i18n.js` - Hệ thống quản lý đa ngôn ngữ
✅ Tạo file `css/language-toggle.css` - Styling cho nút chuyển đổi
✅ Thêm nút chuyển đổi ngôn ngữ vào trang
✅ Thêm link CSS và JS vào index.html

## Cần làm thủ công

Để thiệp cưới hoạt động với đa ngôn ngữ, bạn cần thêm thuộc tính `data-i18n` vào các phần tử HTML cần dịch.

### Cách thêm thuộc tính data-i18n

Ví dụ:
```html
<!-- TRƯỚC -->
<a class="nav-link" href="#home">Trang chủ</a>

<!-- SAU -->
<a class="nav-link" href="#home" data-i18n="nav_home">Trang chủ</a>
```

### Danh sách các phần tử cần cập nhật

#### 1. NAVIGATION (khoảng dòng 1692-1702)
```html
<a class="nav-link smooth-scroll" href="#home" data-i18n="nav_home">Trang chủ</a>
<a class="nav-link smooth-scroll" href="#couple" data-i18n="nav_couple">Cô dâu & Chú rể</a>
<a class="nav-link smooth-scroll" href="#events" data-i18n="nav_events">Sự kiện</a>
<a ... data-i18n="nav_gallery">Thư viện ảnh</a>
```

#### 2. PHẦN CÔ DÂU & CHÚ RỂ (khoảng dòng 1716-1757)
```html
<div data-i18n="couple_subtitle">Một hành trình mới bắt đầu từ hôm nay</div>
<div class="couple-label" data-i18n="groom_family">NHÀ TRAI:</div>
<p><span data-i18n="mr">ÔNG:</span> NGUYỄN DỎ</p>
<p><span data-i18n="mrs">BÀ:</span> HUỲNH THỊ XÊ</p>
<div class="couple-label" data-i18n="bride_family">NHÀ GÁI:</div>
<p><span data-i18n="mr">ÔNG:</span> NGUYỄN VĂN HÀO</p>
<p><span data-i18n="mrs">BÀ:</span> HOÀNG THỊ DẬU</p>
```

#### 3. PHẦN SỰ KIỆN (khoảng dòng 1770-1916)
```html
<p data-i18n="events_title">Thư mời</p>
<p data-i18n="events_subtitle">Tham dự lễ cưới của Sỹ và Dung</p>

<!-- Tiệc cưới nhà trai -->
<h3 class="event-title" data-i18n="event_groom_reception">TIỆC CƯỚI NHÀ TRAI</h3>
<div class="day-text" data-i18n="thu_bay">Thứ Bảy</div>
<span class="month" data-i18n="month_1">Tháng 1</span>
<div class="lunar-date" data-i18n="lunar_date_29">(Tức ngày 29, tháng 11, năm Ất Tỵ)</div>

<!-- Tiệc cưới nhà gái -->
<h3 class="event-title" data-i18n="event_bride_reception">TIỆC CƯỚI NHÀ GÁI</h3>
<div class="day-text" data-i18n="thu_tu">Thứ Tư</div>
<span class="month" data-i18n="month_1">Tháng 1</span>
<div class="lunar-date" data-i18n="lunar_date_26">(Tức ngày 26, tháng 11, năm Ất Tỵ)</div>

<!-- Lễ thành hôn -->
<h3 class="event-title" data-i18n="event_wedding_ceremony">LỄ THÀNH HÔN</h3>
<div class="day-text" data-i18n="thu_7">Thứ 7</div>
<span class="month" data-i18n="month_1">Tháng 1</span>
<div class="lunar-date" data-i18n="lunar_date_29">(Tức ngày 29, tháng 11, năm Ất Tỵ)</div>
<h4 data-i18n="ceremony_will_start">Hôn lễ sẽ diễn ra sau:</h4>

<!-- Lễ vu quy -->
<h3 class="event-title" data-i18n="event_vu_quy">LỄ VU QUY</h3>
<div class="day-text" data-i18n="thu_4">Thứ 4</div>
<span class="month" data-i18n="month_1">Tháng 1</span>
<div class="lunar-date" data-i18n="lunar_date_26">(Tức ngày 26, tháng 11, năm Ất Tỵ)</div>
<h4 data-i18n="ceremony_will_start">Hôn lễ sẽ diễn ra sau:</h4>
```

#### 4. COUNTDOWN (có 2 chỗ, mỗi chỗ có 4 labels)
```html
<span class="count-label" data-i18n="days">Ngày</span>
<span class="count-label" data-i18n="hours">Giờ</span>
<span class="count-label" data-i18n="minutes">Phút</span>
<span class="count-label" data-i18n="seconds">Giây</span>
```

#### 5. ĐỊA ĐIỂM (khoảng dòng 1933-1964)
```html
<div data-i18n="location_title">🗺️ Địa điểm tổ chức</div>
<h3 class="location-title" data-i18n="location_groom">NHÀ TRAI</h3>
<a ... data-i18n="view_directions">XEM CHỈ ĐƯỜNG</a>
<h3 class="location-title" data-i18n="location_bride">NHÀ GÁI</h3>
<a ... data-i18n="view_directions">XEM CHỈ ĐƯỜNG</a>
```

#### 6. THƯ VIỆN ẢNH (khoảng dòng 1977)
```html
<div data-i18n="gallery_title">Love Story</div>
```

#### 7. TRÍCH DẪN TÌNH YÊU (4 câu)
```html
<p class="love-quote-text" data-i18n="quote_1">"Tình yêu không làm cho thế giới quay tròn..."</p>
<p class="love-quote-text" data-i18n="quote_2">"Được ai đó yêu sâu đậm..."</p>
<p class="love-quote-text" data-i18n="quote_3">"Tình yêu chân thành nhất..."</p>
<p class="love-quote-text" data-i18n="quote_4">"Trong tất cả những gì..."</p>
```

#### 8. QUÀ MỪNG (khoảng dòng 2145-2148)
```html
<h7 data-i18n="gift_title">Quà mừng đám cưới</h7>
<div data-i18n="gift_bank">Bank: @Thùy-Dung</div>
```

## Cách hoạt động

1. **Tự động phát hiện vị trí**:
   - Nếu truy cập từ Nhật Bản → Hiển thị tiếng Nhật
   - Nếu truy cập từ Việt Nam hoặc nơi khác → Hiển thị tiếng Việt

2. **Chuyển đổi thủ công**:
   - Click nút ở góc trên bên phải để chuyển đổi ngôn ngữ
   - Lựa chọn sẽ được lưu vào trình duyệt

3. **Nội dung không đổi**:
   - Tên riêng (Sỹ, Dung, Văn Sỹ, Thùy Dung) giữ nguyên
   - Số, ngày tháng giữ nguyên
   - Hình ảnh không thay đổi

## Lưu ý quan trọng

- Chỉ thêm `data-i18n` vào các text cần dịch
- KHÔNG thêm vào tên riêng, số, hoặc các thông tin cố định
- Sau khi thêm, mở file `index.html` trong trình duyệt để kiểm tra
- Nút chuyển đổi ngôn ngữ sẽ xuất hiện ở góc trên bên phải

## API sử dụng

Hệ thống sử dụng API miễn phí `ipapi.co` để phát hiện vị trí địa lý.
Không cần đăng ký hay API key.
