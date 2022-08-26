Install HomeBrew (Kiểm tra có rồi thì bỏ qua bước này)
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Install Openssl
```bash
brew install openssl@3
```

Install libssh2
```bash
brew install libssh2
```

Mở terminal tại folder build:
```bash
sh runRoom.sh
```
Các biến mối trường (chỉnh sửa trong file runRoom.sh): \
NUMBER_CLIENT: số lượng client giả lập để loadtest \
ENABLE_AUDIO: bật/tắt audio 

Các lỗi thường gặp: 

Operation not permitted: (Thử lần lượt các cách) \
Cách 1:
```bash
Cấp quyền full disk access cho terminal. System Preferences -> Security & Privacy -> Privacy -> Full Disk Access \
-> Unlock(góc dưới bên trái) -> tích dấu cộng -> tìm tới Application -> search và chọn Terminal
```
Cách 2:
```
xattr -d com.apple.quarantine ./runRoom.sh
xattr -d com.apple.quarantine ./broadcaster
```
