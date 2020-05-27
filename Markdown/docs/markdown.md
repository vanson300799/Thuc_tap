[1. Thẻ tiêu đề.](#1)

[2. Chèn link, chèn ảnh.](#2)

[3. Ký tự in đậm, in nghiêng.](#3)

[4. Trích dẫn, bo chữ.](#4)

[5. Gạch đầu dòng.](#5)

[6. Tạo bảng:](#6)

# I. Ngôn ngữ markdown:
Ngôn ngữ này khá đơn giản, bạn có thể đọc tại [đây](https://daringfireball.net/projects/markdown/syntax) để biết cách sử dụng.

Nhưng với tôi, tôi không dùng hết từng ấy thứ cho nên tôi chỉ nhớ một số cái tôi hay dùng, cách tôi dùng như sau:

Tạo một file có tên bất kỳ với đuôi .md. Có thể dùng `notepad`, `notepad++`, `vi`, `nano'`... hay bất cứ thứ gì bạn muốn.

Một số phương pháp hay sử dụng:
## 1.Thẻ tiêu đề.  <a name="1"></a>
Markdown sử dụng ký tự # để bắt đầu cho các thẻ tiêu đề, có thể dùng từ 1 đến 6 ký tự # liên tiếp. Mức độ tiêu đề giảm từ 1 đến 6.

Tùy vào mục đích và ý thích bạn có thể sử dụng cách này để thể hiện các chỉ mục khác nhau.

Ví dụ:

```
# 1. Tiêu đề cấp 1
```
# 1. Tiêu đề cấp 1
```
## 2. Tiêu đề cấp 2
```
## 2. Tiêu đề cấp 2
```
###### 6. Tiêu đề cấp 6
```
###### 6. Tiêu đề cấp 6 
## 2. Chèn link, chèn ảnh. <a name="2"></a>
Để chèn hyperlink chỉ cần paste luôn link đó vào file.md

```
https://github.com
```

https://github.com

Hoặc bạn cũng có thể sử dụng cú pháp sau để thu ngắn đường dẫn của link

```
[đây](https://github.com)
```

Kết quả là:

[đây](https://github.com)

Để chèn ảnh thì bạn hãy sử dụng cú pháp sau:

```
<img src="link-hình-ảnh">
```

## 3. Ký tự in đậm, in nghiêng. <a name="3"></a>
- Để in đậm 1 đoạn text cần làm như sau:

```
**Từ cần in đậm**
```
**Từ cần in đậm**

- Để in nghiêng một đoạn text chỉ cần làm như sau:

```
*Từ cần in nghiêng*
```

*Từ cần in nghiêng*

## 4. Trích dẫn, bo chữ. <a name="4"></a>
Để bo một đoạn text thì bạn chỉ cần sử dụng cú pháp sau:

```
`Đoạn text cần bo`
```
Kết quả là: `Đoạn text cần bo`

Để làm nổi bật một đoạn, chẳng hạn như một đoạn shell hay file cấu hình bạn có thể sử dụng cú pháp như ví dụ sau:

```
    ```sh
    auto eth0
    iface eth0 inet static
    ipaddress 10.10.10.10
    netmask 255.255.255.0
    gateway 10.10.10.1
    dns-nameservers 8.8.8.8
    ```
```
Kết quả như sau:
 ```
 sh
auto eth0
iface eth0 inet static
ipaddress 10.10.10.10
netmask 255.255.255.0
gateway 10.10.10.1
dns-nameservers 8.8.8.8
```
## 5. Gạch đầu dòng.  <a name="5"></a>
Để sử dụng gạch đầu dòng bạn cần sử dụng cú pháp như sau:
```
- Gạch đầu dòng thứ nhất

    - Thụt với đầu dòng 1

    - Thụt với đầu dòng 1
- Gạch đầu dòng thứ hai

    - Thụt với đầu dòng 2
    - Thụt với đầu dòng 2
```
kết quả là:
- Gạch đầu dòng thứ nhất

    - Thụt với đầu dòng 1

    - Thụt với đầu dòng 1
- Gạch đầu dòng thứ hai

    - Thụt với đầu dòng 2

    - Thụt với đầu dòng 2

## 6. Tạo bảng:  <a name="6"></a>
Bạn có thể sử dụng cú pháp sau để tạo bảng:
```
| | Cột 1 | Cột 2 | Cột 3|
|-|-------|-------|------|
| Hàng 1 | 1 x 1 | 1 x 2 | 1 x 3 |
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 |
```
Kết quả:

| | Cột 1 | Cột 2 | Cột 3|
|-|-------|-------|------|
| Hàng 1 | 1 x 1 | 1 x 2 | 1 x 3 |
| Hàng 2 | 2 x 1 | 2 x 2 | 2 x 3 |
| Hàng 3 | 3 x 1 | 3 x 2 | 3 x 3 |

### Mẹo:
- Sử dụng trang http://markdownlivepreview.com/ paste vào đó đoạn markdown bạn viết và xem trước để chỉnh sửa cho phù hợp.

- Cũng có thể sử dụng những đoạn markdown của người khác đã viết trước để tham khảo.

Như vậy bạn đã có thể trình bày github của mình một cách sáng sủa bằng markdown.
> git


