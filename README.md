# Hướng dẫn cài đặt cảm biến độ ẩm DHT22

## 1. Giới thiệu

Cảm biến DHT22 giúp đo nhiệt độ và độ ẩm không khí tại trang trại Lan. Raspberry Pi nhận dữ liệu và sử dụng Python để hiển thị kết quả.

## 2. Chuẩn bị thiết bị

- Cảm biến DHT22.
- Raspberry Pi.
- Dây nối Dupont.
- Nguồn điện và kết nối Internet.

## 3. Các bước cài đặt

### Bước 1: Kiểm tra Python

Mở Terminal và nhập lệnh:

```bash
python3 --version
```

### Bước 2: Cài đặt công cụ

```bash
sudo apt update
sudo apt install -y git python3-pip
```

### Bước 3: Viết chương trình Python

# Gia tri do am khong khi (%)
humidity = 67

# Kiem tra do am
if humidity < 60:
    print("Do am thap, can kiem tra moi truong!")
else:
    print("Do am binh thuong!")

# Hien thi ket qua
print("Do am hien tai:", humidity, "%")

**Giải thích:**

Lưu ý: Cần cài thư viện tương thích trước khi chạy chương trình.

### Bước 4: Chạy chương trình

```bash
python3 read_dht22.py
```

Kết quả minh họa:

```Do am binh thuong!
Do am hien tai: 67 %
```

## 4. Sơ đồ kết nối

| Chân DHT22 | Raspberry Pi | Chức năng |
|---|---|---|
| VCC | 3.3V | Cấp nguồn |
| GND | GND | Nối đất |
| DATA | GPIO4 | Truyền dữ liệu |
| NC | Không kết nối | Không sử dụng |

*Kiểm tra đúng thứ tự chân của cảm biến trước khi đấu nối.*

## 5. Bảng so sánh cảm biến độ ẩm đất

| Tiêu chí | Cảm biến cũ | Cảm biến mới |
|---|---|---|
| Loại | Điện trở | Điện dung |
| Giá thành | Thấp | Thường cao hơn |
| Ăn mòn | Dễ hơn | Ít hơn |
| Độ bền | Thấp hơn trong môi trường ẩm | Thường tốt hơn |

*Bảng trên so sánh cảm biến độ ẩm đất, không phải cảm biến DHT22 đo độ ẩm không khí.*

## 6. Checklist kiểm tra thiết bị

- [ ] Kiểm tra cảm biến và dây nối.
- [ ] Kiểm tra nguồn điện.
- [ ] Cài đặt Python và thư viện phù hợp.
- [ ] Chạy chương trình đọc cảm biến.
- [ ] Kiểm tra nhiệt độ và độ ẩm hiển thị.
