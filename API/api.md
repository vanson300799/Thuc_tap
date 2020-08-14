# Table of Contents:
1. [API](#API)
2. [REST RESTful](#REST_RESTful)
3. [JSON, XML](#JSON_XML)

# 1. API? <a name="API"></a>

- API là viết tắt của Application Programming Interface (Giao diện lập trình ứng dụng), một phần mềm trung gian cho phép hai ứng dụng nói chuyện với nhau.

- Nó cung cấp khả năng truy xuất đến một tập các hàm hay dùng từ đó có thể trao đổi dữ liệu giữa các ứng dụng.

- **Các đặc điểm nổi bật của API**:

    - API sử dụng mã nguồn mở, dùng được với mọi client hỗ trợ XML, JSON.

    - API có khả năng đáp ứng đầy đủ các thành phần HTTP: URL, request/response headers, caching, versioning, content forma... Bạn có thể sử các host nằm trong phần ứng dụng hoặc trên IIS.

    - Mô hình web API được dùng để hỗ trợ MVC như: unit test, injection, ioc container, model binder, action result, filter, routing, controller. Ngoài ra, nó cũng hỗ trợ RESTful đầy đủ các phương thức như: GET,POST,PUT, DELETE các dữ liệu.

    - Được đánh giá là một trong những kiểu kiến trúc hỗ trợ tốt nhất với các thiết bị có lượng băng thông bị giới hạn như smartphone, tablet... 

- **Ưu nhược điểm của API**

    - **Ưu điểm**:

        - Giao tiếp hai chiều phải được xác nhận trong các giao dịch sử dụng API. Cũng chính vì vậy mà các thông tin rất đáng tin  cậy.

        - API là công cụ mã nguồn mở có thể kết nối mọi lúc nhờ Internet. 

        - Hỗ trợ chức năng RESTful 1 cách đầy đủ.

        - Cấu hình đơn giản khi được so sánh với WCF. Cung cấp trải nghiệm thân thiện cho người dùng.

    - **Nhược điểm**:

        - Tốn nhiền chi phí phát triển, vận hành và chỉnh sửa.

        - Đòi hỏi kiến thức chuyên sâu.

        - Có thể gặp vấn đề bảo mật khi bị tấn công hệ thống.

- **Ứng dụng của API**:

    - **Web API**: Là hệ thống API được sử dụng trong hầu hết các hệ thống website. Hầu hết các website đều cung cấp hệ thống API cho phép bạn kết nối, lấy dữ liệu hoặc cập nhật cơ sở dữ liệu. Đa số web API được thiết kế theo tiêu chuẩn RESTful.

    - **API trên hệ điều hành**: Giúp lập trình viên có thể tạo ra các phần mềm ứng dụng có thể tương tác trực tiếp với hệ điều hành.

    - **API của thư viện phần mềm (Framework)**: API mô tả và quy định các hành động mong muốn mà các thư viện cung cấp. Một API có thể có nhiều cách triển khai khác nhau, giúp cho một chương trình viết bằng ngôn ngữ này có thể sử dụng được thư viện viết bằng ngôn ngữ khác.

# 2. REST, RESTful API: <a name="REST_RESTful"></a>

**REST**

- REST (REpresentational State Transfer) là một dạng chuyển đổi cấu trúc dữ liệu, là một phong cách kiến ​​trúc cho việc thiết kế các ứng dụng có kết nối.

- Nó sử dụng HTTP đơn giản để tạo cho giao tiếp giữa các máy. Vì vậy, thay vì sử dụng một URL cho việc xử lý một số thông tin người dùng, REST gửi một yêu cầu HTTP như GET, POST, DELETE, vv đến một URL để xử lý dữ liệu.

- REST API là một ứng dụng chuyển đổi cấu trúc dữ liệu có các phương thức để kết nối với các thư viện và ứng dụng khác.

**RESTful**

- RESTful API là một tiêu chuẩn dùng trong việc thết kế các thiết kế API cho các ứng dụng web để quản lý các resource. RESTful là một trong những kiểu thiết kế API được sử dụng phổ biến nhất ngày nay.

- Trọng tâm của REST quy định cách sử dụng các HTTP method (như GET, POST, PUT, DELETE...) và cách định dạng các URL cho ứng dụng web để quản các resource.

- Ví dụ với một trang blog để quản lý các bài viết chúng ta có các URL đi với HTTP method như sau:

    - URL tạo bài viết: http://my-blog.xyz/posts. Tương ứng với HTTP method là POST

    - URL đọc bài viết với ID là 123: http://my-blog.xyz/posts/123. Tương ứng với HTTP method là GET

    - URL cập nhật bài viết với ID là 123: http://my-blog.xyz/posts/123. Tương ứng với HTTP method là PUT

    - URL xoá bài viết với ID là 123: http://my-blog.xyz/posts/123. Tương ứng với HTTP method là DELETE

- Với các ứng dụng web được thiết kế sử dụng RESTful, lập trình viên có thể dễ dàng biết được URL và HTTP method để quản lý một resource.

- Bạn cũng cần lưu ý bản thân RESTful không quy định logic code ứng dụng và RESTful cũng không giới hạn bởi ngôn ngữ lập trình ứng dụng. Bất kỳ ngôn ngữ lập trình (hoặc framework) nào cũng có thể áp dụng RESTful trong việc thiết kế API cho ứng dụng web.

# 3. JSON, XML:<a name="JSON_XML"></a>

**JSON**

- JSON viết tắt JavaScript Object Notation. JSON được sử dụng để lưu trữ và trao đổi dữ liệu. JSON là ngôn ngữ “tự mô tả” và dễ hiểu.

- JSON là một kiểu định dạng dữ liệu trong đó sử dụng văn bản thuần tuý, định dạng JSON sử dụng các cặp key - value để dữ liệu sử dụng.

- Một ví dụ một tập tin có tên application_info.json với nội dung như ở dưới đây sử dụng format kiểu JSON để lưu trữ thông tin của một ứng dụng phần mềm:

    ```
    {
        "name" : "PHPStorm",
        "version" : "16.0.1",
        "license" : "commercial"
    }
    ```

- Tập tin json có thể được lưu với bất kỳ phần mở rộng nào, tuy nhiên thông thường thì nó được lưu dưới phần mở rộng là .json hoặc .js.

- JSON ban đầu được phát triển để dành phục vụ cho ứng dụng viết bằng JavaScript. Bản thân thuật ngữ JSON là viết tắt của cụm từ JavaScript Object Notation . Tuy nhiên vì JSON là một định dạng dữ liệu nên nó có thể được sử dụng bởi bất cứ ngôn ngữ nào mà không giới hạn với JavaScript.

- **Sử Dụng JSON**:

    - Một trường hợp khá phổ biến trong JavaScript mà dữ liệu được định dạng theo format JSON xuất hiện đó là trong các AJAX request.

    - Ví dụ bạn lưu tập tin `application_info.json` ở thư mục gốc của server (để khi truy cập vào URL `http://localhost/application_info.json` thì server trả về nội dung của tập tin này) và sau đó bạn tạo một tập tin json_ajax.html với nội dung như sau:

        ```
        <html>
        <head>
            <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
        </head>
        <body>
        <script type="text/javascript">
            $.ajax(
                type: 'GET',
                url: "http://localhost/application_info.json",
                success: function(response) {
                    console.log("Data type: " + (typeof response));
                    console.log("Application name: " + response.name);
                },
            );
        </script>
        </body>
        </html>
        ```

    - Đoạn code trên sử dụng `$.ajax()` để gửi AJAX request lên server lấy về nội dung tập tin `application_info.json`. Sau khi lấy về nội dung tập tin này thành công, dữ liệu sẽ được chuyển vào biến response.

    - **Sử Dụng JSON Với PHP**

        - Giống như JavaSCript, PHP cũng hỗ trợ dữ liệu định dạng JSON.

        ```
        <?php
        $json_string = <<<DOC
        {
            "name" : "PHPStorm",
            "version" : "16.0.1",
            "license" : "commercial"
        }
        DOC;
        $arr = json_decode($json_string, true);
        print_r($arr);
        ```

        - Đoạn code trên sử dụng hàm json_decode để decode dữ liệu được lưu trong biến $json_string. Biến $json_string lúc này có kiểu dữ liệu là String của PHP nhưng đồng thời chuỗi này cũng hỗ trợ định dạng JSON.

        - Kết quả trả về của đoạn code trên sẽ như sau:

        ```
        Array
        (
            [name] => PHPStorm
            [version] => 16.0.1
            [license] => commercial
        )
        ```

**XML**

- XML (viết tắt của từ EXtensible Markup Language) là một ngôn ngữ đánh dấu mở rộng được dùng để mô tả cấu trúc dữ liệu của các văn bản theo một định dạng mà cả con người và máy tính đều có thể hiểu được.

- **XML Là Ngôn Ngữ Đánh Dấu Mở Rộng**: XML sử dụng các thẻ để đánh dấu văn bản giống với HTML. Tuy nhiên khác với HTML, XML cho phép chúng ta có thể tự do đặt tên các thẻ.

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <bookstore>
    <book category="programming">
        <title lang="en">XML Cơ Bản</title>
        <author>Khang Nguyễn</author>
        <year>2015</year>
        <price>0</price>
    </book>
    </bookstore>
    ```

- **XML Dùng Để Mô Tả Cấu Trúc Dữ Liệu**: XML được sử dụng để mô tả cấu trúc của dữ liệu các văn bản theo một cấu trúc giúp máy tính có thể dựa trên cấu trúc này để dễ dàng gọi ra các thông tin cần thiết.

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <group name="student">
        <user>
            <id>123</id>
            <firstname>John</firstname>
            <lastName>Doe</lastName>
        </user>
    <group>
    ```

- **XML Dùng Làm Gì**: XML được dùng để lưu trữ và trao đổi dữ liệu giữa các máy tính một cách dễ dàng. Bản thân XML không làm bất cứ công việc gì, thay vào đó các tập tin XML chứa dữ liệu (với cấu trúc nhất định).

    ```
    <?xml version="1.0" encoding="UTF-8"?>
    <group name="spiderman">
        <user>
            <id>1</id>
            <firstname>Mary</firstname>
            <lastName>Jane</lastName>
            <gender>Female</gender>
        </user>
        <user>
            <id>2</id>
            <firstname>Peter</firstname>
            <lastName>Parker</lastName>
            <gender>Male</gender>
        </user>
    <group>
    ```

- Việc sử dụng (xử lý, hiển thị...) dữ liệu này như thế nào phụ thuộc vào ứng dụng. Với văn bản XML như trên chúng ta có thể viết một ứng dụng (bằng JavaScript hoặc PHP) để hiện thị thông tin người dùng đặt trong hai khung như sau:

```
Marry Jane
ID: 1
Gender: Female
```
```
Peter Packer
ID: 2
Gender: Male
```
- Hầu hết các ngôn ngữ lập trình đều hỗ trợ API (hàm) để có thể đọc dữ liệu từ tập tin XML.
