# Report 1 Page – FIT4012 Lab 2

## 1. Mục tiêu
Mục tiêu của bài lab là hoàn thiện hai thuật toán mã hóa cổ điển là Caesar Cipher và Rail Fence Cipher, đồng thời hiểu rõ cách mã hóa, giải mã và kiểm tra dữ liệu đầu vào. Ngoài ra, bài lab cũng giúp em luyện cách xử lý chuỗi trong C++, giữ lại dấu cách khi mã hóa, đọc dữ liệu từ file và kiểm thử chương trình với nhiều trường hợp khác nhau.

## 2. Cách làm
- Hoàn thiện Caesar Cipher cho chữ thường, dấu cách và giải mã.
- Hoàn thiện Rail Fence Cipher cho giải mã, giữ dấu cách, kiểm tra đầu vào và đọc file.
- Chạy thử trên nhiều test case.

## 3. Kết quả chính
### 3.1 Caesar Cipher
| Input | Key | Ciphertext / Plaintext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 3 | L ORYH BRX | Mã hóa đúng, giữ nguyên chữ hoa và dấu cách |
| hello world | 5 | mjqqt btwqi | Mã hóa đúng với chữ thường, dấu cách vẫn được giữ |
| LORYH BRX | 3 | ILOVE YOU | Giải mã đúng với khóa 3, dùng dịch ngược để khôi phục bản rõ |

### 3.2 Rail Fence Cipher
| Input | Rails | Ciphertext / Plaintext | Nhận xét |
|---|---:|---|---|
| I LOVE YOU | 2 | ILV O OEYU | Mã hóa đúng theo zigzag 2 hàng, dấu cách được giữ như ký tự bình thường |
| I LOVE YOU | 4 | I  EYLVOOU | Mã hóa đúng với 4 hàng, thứ tự ký tự thay đổi theo mẫu zigzag |
| IOEOLVYU | 2 | ILOVEYOU | Giải mã đúng với 2 hàng, khôi phục lại bản rõ ban đầu |

### 3.3 Input validation / file input
- Trường hợp đầu vào không hợp lệ:
- Kết quả đọc từ `data/input.txt`:

## 4. Kết luận
Qua bài lab này, em hiểu rõ hơn cách hoạt động của Caesar Cipher và Rail Fence Cipher, đặc biệt là sự khác nhau giữa cách dịch chuyển ký tự và cách sắp xếp ký tự theo dạng zigzag. Em cũng học được cách xử lý chuỗi, kiểm tra đầu vào hợp lệ và đọc dữ liệu từ file trong C++.
Khó khăn lớn nhất của em là phần giải mã Rail Fence Cipher vì phải xác định lại đúng vị trí zigzag trước khi khôi phục chuỗi gốc. Điều giúp em hiểu rõ hơn là vẽ thử đường đi của từng ký tự trên giấy và chạy từng bước bằng ví dụ ngắn. Nhờ đó em thấy rõ cách mã hóa và giải mã hoạt động trong thực tế.
