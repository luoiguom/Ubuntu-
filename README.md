# Ubuntu-Vscode
Cài VSCode bằng file deb ổn định hơn
Dùng lệnh apt (Khuyên dùng khi dùng Terminal)
Lệnh apt tự động tìm và cài đặt các gói phụ thuộc (dependencies) đi kèm. 
Linuxize
 Mở Terminal (Ctrl + Alt + T).
 Di chuyển đến thư mục chứa tệp hoặc gõ đường dẫn đầy đủ:
 bash
 sudo apt install ./ten-tep.deb
 Hãy thận trọng khi sử dụng mã.
 (Nhớ thêm ./ ở trước tên tệp nếu bạn đang đứng trong cùng thư mục chứa tệp đó).


Trong vscode các ký tự tiếng việt bị khoanh trong ô vuông làm sao để tắt đi

Đây là tính năng Unicode Highlight của VS Code, nó đánh dấu các ký tự "không phải ASCII" hoặc dễ gây nhầm lẫn. Bạn có thể tắt như sau:

Cách 1: Qua giao diện Settings

Nhấn Ctrl + , (hoặc Cmd + , trên Mac) để mở Settings.
Gõ unicode highlight vào ô tìm kiếm.
Bỏ tick các mục:
Editor › Unicode Highlight: Non Basic ASCII
Editor › Unicode Highlight: Ambiguous Characters
Editor › Unicode Highlight: Invisible Characters (tùy chọn)

Cách 2: Sửa trực tiếp settings.json

Nhấn Ctrl + Shift + P, gõ Open User Settings (JSON).
Thêm các dòng sau:
json
{
  "editor.unicodeHighlight.nonBasicASCII": false,
  "editor.unicodeHighlight.ambiguousCharacters": false,
  "editor.unicodeHighlight.invisibleCharacters": false
}

Lưu ý:

Nếu chỉ thấy ô vuông ở một số ký tự cụ thể (ví dụ dấu bị tách rời), có thể file đang dùng dạng Unicode tổ hợp (NFD) thay vì dựng sẵn (NFC). Khi đó bạn nên chuyển văn bản về NFC để tránh lỗi hiển thị.
Nếu ký tự hiện ô vuông trống chứ không phải bị khoanh viền, đó là vấn đề font. Hãy đổi editor.fontFamily sang font hỗ trợ tiếng Việt như Consolas, Fira Code hay JetBrains Mono.
