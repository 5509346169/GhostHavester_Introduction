# GhostHarvester - Phiên bản mã hóa

[![Version](https://img.shields.io/badge/version-2.2.4-blue.svg)](https://github.com/vsmz4laj7n/GhostHarvester)
[![Python](https://img.shields.io/badge/python-3.12+-green.svg)](https://www.python.org/downloads/)

Đây là **phiên bản mã hóa** của GhostHarvester - Công cụ phân tích và trích xuất dữ liệu Telegram nâng cao. Mã nguồn được bảo vệ bằng công nghệ mã hóa CodeEnigma để tăng cường bảo mật.

**Giá truy cập công cụ (toàn quyền sử dụng, không bao gồm hỗ trợ, cập nhật) này là 100 USD (100 USDT - Crypto = 2.500.000 VNĐ).**

## 🔒 Tính năng mã hóa

- **Bảo vệ mã nguồn**: Mã nguồn được mã hóa và bảo mật
- **Bảo mật thời gian chạy**: Thực thi bytecode an toàn với CodeEnigma runtime
- **Chức năng đầy đủ**: Tất cả tính năng của GhostHarvester gốc
- **Cài đặt dễ dàng**: Tự động cài đặt với quản lý phụ thuộc

## 📋 Yêu cầu

- **Python 3.12+** (Bắt buộc)
- **Công cụ xây dựng**: gcc, make (Linux/macOS) hoặc Visual Studio Build Tools (Windows)
- **Thông tin API Telegram** (api_id và api_hash từ [my.telegram.org](https://my.telegram.org))
- **Số điện thoại hợp lệ** (để xác thực Telegram)

## 🚀 Cài đặt nhanh

### Tùy chọn 1: Cài đặt tự động (Khuyến nghị)

1. **Chạy trình cài đặt tự động:**
   ```bash
   python install.py install
   ```

   Thao tác này sẽ:
   - Tạo môi trường ảo
   - Cài đặt tất cả các phụ thuộc
   - Xây dựng phần mở rộng mã hóa
   - Cài đặt gói phần mềm

### Tùy chọn 2: Cài đặt thủ công

1. **Tạo môi trường ảo:**
   ```bash
   python3.12 -m venv venv
   source venv/bin/activate  # Linux/macOS
   # hoặc
   venv\Scripts\activate     # Windows
   ```

2. **Cài đặt phụ thuộc:**
   ```bash
   pip install cython setuptools wheel
   pip install -r requirements.txt
   ```

3. **Xây dựng và cài đặt:**
   ```bash
   python setup.py build_ext --inplace
   pip install -e .
   ```

## ⚙️ Cấu hình

1. **Sao chép và chỉnh sửa cấu hình:**
   ```bash
   cp config_real.ini my_config.ini
   ```

2. **Chỉnh sửa `my_config.ini` với thông tin của bạn:**
   ```ini
   [CONFIGURATION]
   api_id=YOUR_API_ID
   api_hash=YOUR_API_HASH
   phone_number=+YOUR_PHONE_NUMBER
   data_path=/đường/dẫn/đến/thư/mục/dữ/liệu/
   ```

3. **Lấy thông tin API Telegram:**
   - Truy cập [my.telegram.org](https://my.telegram.org)
   - Đăng nhập bằng số điện thoại của bạn
   - Vào "API development tools"
   - Tạo ứng dụng mới để lấy `api_id` và `api_hash`

## 🧪 Kiểm tra

### Kiểm tra cài đặt

```bash
# Kiểm tra lệnh trợ giúp
python install.py test

# Hoặc kiểm tra thủ công
source venv/bin/activate
python -m ghavest --help
```

### Kiểm tra với cấu hình

```bash
# Kiểm tra với cấu hình của bạn
python -m ghavest connect --config my_config.ini
```

## 🚀 Sử dụng

Sau khi cài đặt, kích hoạt môi trường ảo:

**Linux/macOS:**
```bash
source venv/bin/activate
```

**Windows:**
```bash
venv\Scripts\activate
```

### Các lệnh có sẵn

```bash
# Hiển thị trợ giúp
python -m ghavest --help

# Kết nối với Telegram (thiết lập lần đầu)
python -m ghavest connect --config my_config.ini

# Tải nhóm và thành viên
python -m ghavest load_groups --config my_config.ini

# Tải tin nhắn
python -m ghavest download_messages --config my_config.ini

# Lắng nghe tin nhắn trực tiếp
python -m ghavest listen --config my_config.ini

# Tạo báo cáo
python -m ghavest report --config my_config.ini

# Xuất dữ liệu
python -m ghavest export_text --config my_config.ini
python -m ghavest export_html --config my_config.ini

# Phân tích dữ liệu
python -m ghavest analyze --config my_config.ini

# Hiển thị thống kê
python -m ghavest stats --config my_config.ini
```

## 🔧 Sử dụng nâng cao

### Quy trình xây dựng thủ công

Nếu cần xây dựng lại mã mã hóa:

```bash
# Xóa các bản build trước đó
python install.py clean

# Xây dựng lại
python setup.py build_ext --inplace
pip install -e .
```

### Chế độ phát triển

Để phát triển với phiên bản mã hóa:

```bash
# Cài đặt ở chế độ phát triển
pip install -e .

# Thực hiện thay đổi và cài đặt lại
pip install -e . --force-reinstall
```

## 📁 Cấu trúc thư mục

```
obfuscate/
├── ghavest/                    # Gói mã hóa
│   ├── core/                  # Chức năng cốt lõi (mã hóa)
│   ├── database/              # Quản lý cơ sở dữ liệu (mã hóa)
│   ├── modules/               # Mô-đun xử lý (mã hóa)
│   └── ...                    # Các mô-đun khác (mã hóa)
├── codeenigma_runtime.pyx     # Nguồn mở rộng thời gian chạy
├── codeenigma_runtime.so      # Phần mở rộng đã biên dịch
├── setup.py                   # Cấu hình xây dựng
├── install.py                 # Trình cài đặt tự động
├── requirements.txt           # Phụ thuộc
├── config_real.ini            # Mẫu cấu hình
├── pyproject.toml            # Siêu dữ liệu dự án
└── README.md                 # Tệp này
```

## 🐛 Khắc phục sự cố

### Các vấn đề phổ biến

1. **Lỗi phiên bản Python:**
   ```
   Error: Python 3.12+ is required
   ```
   **Giải pháp:** Cài đặt Python 3.12 hoặc cao hơn

2. **Thiếu phụ thuộc xây dựng:**
   ```
   error: Microsoft Visual C++ 14.0 is required
   ```
   **Giải pháp:** 
   - **Windows:** Cài đặt Visual Studio Build Tools
   - **Linux:** Cài đặt `build-essential`: `sudo apt-get install build-essential`
   - **macOS:** Cài đặt Xcode Command Line Tools: `xcode-select --install`

3. **Không tìm thấy Cython:**
   ```
   ModuleNotFoundError: No module named 'Cython'
   ```
   **Giải pháp:** `pip install cython`

4. **Lỗi nhập:**
   ```
   ImportError: No module named 'codeenigma_runtime'
   ```
   **Giải pháp:** Xây dựng lại phần mở rộng:
   ```bash
   python setup.py build_ext --inplace
   pip install -e .
   ```

5. **Vấn đề môi trường ảo:**
   ```
   Error: No such file or directory: venv/bin/pip
   ```
   **Giải pháp:** Tạo lại môi trường ảo:
   ```bash
   rm -rf venv
   python3.12 -m venv venv
   ```

## 🔒 Ghi chú bảo mật

- Đây là phiên bản mã hóa với bảo vệ mã nâng cao
- Mã nguồn được mã hóa và bảo vệ khỏi kỹ thuật đảo ngược
- Thực thi thời gian chạy được bảo mật thông qua CodeEnigma
- Tất cả chức năng giống hệt phiên bản gốc

---

**An toàn và được bảo vệ! 🔒**
