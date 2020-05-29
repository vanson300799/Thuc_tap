# ** USER & GROUP**

# 1) `USER`:
## 1.1) `User` là gì?

- Là một thuật ngữ chuyên dụng được sử dụng trong ngành công nghệ thông tin.

- User được dùng để thể hiện tài khoản của người dùng trong máy tính.

- User giúp bạn bảo mật thông tin máy tính của bạn.

-  User được sử dụng để login, gán quyền, v.v..

## 1.2) Phân loại `User`:

- Có 2 loại user:

    - user người dùng: là những tài khoản để login sử dụng hệ điều hành .

    - user hệ thống: dùng để thực thi các module , script cần thiết phục vụ cho hệ điều hành .

- Trong các tài khoản người dùng thì tài khoản user **root ( super user )** là tài khoản quan trọng nhất :

    - Tài khoản này được tự động tạo ra khi cài đặt Linux .

    - Tài khoản này không thể đổi tên hoặc xóa bỏ .

    - User root còn gọi là super user vì nó có full quyền trên hệ thống .

    - Chỉ làm việc với user root khi muốn thực hiện công tác quản trị hệ thống , trong các trường hợp khác , chỉ nên làm việc với user thường .

## 1.3) Các đặc điểm của user:

- Tên tài khoản user là duy nhất, có thể dùng chữ thường hoặc in hoa.

- Mỗi user có 1 mã định danh duy nhất (UID).

- Mỗi user có thể thuộc về group.

- Tài khoản super user có uid=gid=0.

# 2) Các file dữ liệu.

## 2.1) /etc/password: Lưu thông tin người dùng.

- Mọi user đều có thể xem thông tin này, chỉ có root mới có quyền thay đổi.

- Để xem nội dung file ta dùng lệnh: `#cat /etc/passwd`

    ```
    [root@localhost file_2]# cat /etc/passwd
    root:x:0:0:root:/root:/bin/bash
    bin:x:1:1:bin:/bin:/sbin/nologin
    daemon:x:2:2:daemon:/sbin:/sbin/nologin
    adm:x:3:4:adm:/var/adm:/sbin/nologin
    lp:x:4:7:lp:/var/spool/lpd:/sbin/nologin
    sync:x:5:0:sync:/sbin:/bin/sync
    shutdown:x:6:0:shutdown:/sbin:/sbin/shutdown
    halt:x:7:0:halt:/sbin:/sbin/halt
    mail:x:8:12:mail:/var/spool/mail:/sbin/nologin
    operator:x:11:0:operator:/root:/sbin/nologin
    games:x:12:100:games:/usr/games:/sbin/nologin
    ftp:x:14:50:FTP User:/var/ftp:/sbin/nologin
    nobody:x:99:99:Nobody:/:/sbin/nologin
    systemd-network:x:192:192:systemd Network Management:/:/sbin/nologin
    dbus:x:81:81:System message bus:/:/sbin/nologin
    polkitd:x:999:998:User for polkitd:/:/sbin/nologin
    sshd:x:74:74:Privilege-separated SSH:/var/empty/sshd:/sbin/nologin
    postfix:x:89:89::/var/spool/postfix:/sbin/nologin
    chrony:x:998:996::/var/lib/chrony:/sbin/nologin
    ````

- Mỗi user tạo ra  được lưu trên 1 dòng.

- Ý nghĩa của thành phần trong dòng: (Dòng 1)

    - root: Tên user(login name).

    - X mật khẩu được mã hóa. 

    - 0: UID.

    - 0: GID.

    - root: Tên mô tả người sử dụng.

    - root: thư mục home của của user.

    - /bin/bash: Loại sell sẽ hoạt động khi user login

## 2.2) /etc/shadow:

- Lưu thông tin password của user.

- Chỉ có user root mới có quyền truy cập file này.

- User root có quyền reset mật khẩu của bất cứ user nào trên máy .

- Mỗi dòng trong tập tin chứa thông tin về mật khẩu của user , định dạng của dòng gồm nhiều cột , giá trị , dấu : được sử dụng để phân cách các cột .

        ```
        root:$6$HC5fRt9bvocUEvkT$vFglGMafQXsou8.F5bf.BCRTOV.Uj2a2gqvz8bbqcyubjFP2pJfRpFP2sdsoKdPonfddK1CINfv7Pe.pbvlx3.::0:99999:7:::
        bin:*:18353:0:99999:7:::
        daemon:*:18353:0:99999:7:::
        adm:*:18353:0:99999:7:::
        lp:*:18353:0:99999:7:::
        sync:*:18353:0:99999:7:::
        shutdown:*:18353:0:99999:7:::
        halt:*:18353:0:99999:7:::
        mail:*:18353:0:99999:7:::
        operator:*:18353:0:99999:7:::
        games:*:18353:0:99999:7:::
        ftp:*:18353:0:99999:7:::
        nobody:*:18353:0:99999:7:::
        systemd-network:!!:18408::::::
        dbus:!!:18408::::::
        polkitd:!!:18408::::::
        sshd:!!:18408::::::
        postfix:!!:18408::::::
        chrony:!!:18408::::::
        ```
        
- Ý nghĩa: (dòng 2)

    - Bin: tên thư mục.

    - *: Mật khẩu được mã hóa.

    - 18353: số ngày kể từ lần cuối thay đổi mật khẩu.

    - 0: Số ngày trước khi có thể thay đổi mật khẩu.

    - 99999: Số ngày mật khẩu có giá trị.

    - 7: Số ngày cảnh báo user trước khi mật khẩu hết hạn.

    - Số ngày sau khi mật khẩu hết hạn tài khoản sẽ bị khóa .

    - Số ngày kể từ khi tài khoản bị khóa ( tính từ 1/1/1970 )

# 3) Các lệnh quản lý user:

## 3.1) Useradd:

- là lệnh tạo tài khoản user.

    ```
    # useradd [options] [login_name]
    ```
    
    - Options:

        - `-c`: comment: Tạo bí danh.

        - `-u`: set userID: mặc định sẽ lấy số ID tiếp theo để gắn cho user ( bắt đầu từ 1000 ).

        - `-d`: Chỉ định thư mục home cho user.

        - `-g`: Chỉ định group chính.

        - `-G`: Chỉ định group phụ.

        - `-s`: Chỉ định sell cho user chỉ định.

- VD1: Tạo user với tên son và tên đầy đủ là vanson
    
    ```
     [root@localhost file_2]# useradd -c "vanson" son
    ```

    => User được tạo sẽ thuộc về group will và thư mục home của user là /home/will được tạo ra tự động .

- VD2: Tạo user với tên justice và tên đầy đủ là Justice Smiths , user thuộc nhóm users và các nhóm wheel , sales

    ```
    # useradd -g users -G wheel,sales -c "Justice Smiths" justice
    ```

## 3.2) Passwd;

- Là lệnh đổi password cho user.

    ```
    # passwd [login name]
    ```

    ```
    [root@localhost file_2]# passwd son
    Changing password for user son.
    New password:
    BAD PASSWORD: The password is shorter than 8 characters
    Retype new password:
    Sorry, passwords do not match.
    New password:
    Retype new password:
    passwd: all authentication tokens updated successfully
    ```

## 3.3) Usermod:

- Là lệnh sửa thông tin tài khoản:

    ```
    # usermod [options] [login_name]
    ```

    - options:

        - `-c`: comment: tạo bí danh    

        - `-d`: thay đổi thư mục home cho user

        - `-m`: di chuyển nội dung từ thư mục home cũ sang thư mục home mới ( chỉ dùng với -d )

        - `-g`: chỉ định group chính

        - `-G`: chỉ định group phụ ( group mở rộng )

        - `-s`: chỉ định shell cho user sử dụng

        - `-l`: đổi tên tài khoản

        - `-L`: Khóa tài khoản

-VD: đổi tên tài khoản son thành tài khoản a với thư mục home của user là home/a

    ```
    # usermod -l a -c "vana" -m -d /home/a
    ```

## 3.4) userdel

- Là lệnh xóa tài khoản user.

    ```
    # userdel [options] [login_name]
    ```

    - options:
        
        - `-r` : xóa cả thư mục home của user

## 3.5) chage:

- Dùng để thiết lập chính sách (policy) cho user

    ```
    # chage [options] [login_name]
    ```

    - options: 

        - `-l`: Xem danh sách của 1 user.

        - `-E`: Thiết lập ngày hết hạn cho account

        - `-I`: thiết lập ngày bị khóa sau khi hết hạn mật khẩu.

        - `-m`: Thiết lập số ngày tối thiểu được phép thay đổi password.

        - `-M`: thiết lập số ngày tối đa được thay đổi  password

        - `-W`: thiết lập số ngày cảnh báo trước khi hết hạn mật khẩu

## 3.6) ID.

- Xem thông tin ID hiện hành.

    ```
    [root@localhost file_2]# id
    uid=0(root) gid=0(root) groups=0(root) context=unconfined_u:unconfined_r:unconfined_t:s0-s0:c0.c1023
    ```

## 3.7) su

- Chuyển đổi user làm việc từ terminal .

- User root chuyển qua các user khác thì không cần nhập mật khẩu .

- User root chuyển qua các user khác thì không cần nhập mật khẩu .

    ```
    # su -l [login_name]
    ```

- Chuyển đổi từ user thường sang user root :

    ```
    [son@localhost ~]$ su -l root
    Password:
    Last login: Fri May 29 11:41:31 +07 2020 on pts/0
    ```


