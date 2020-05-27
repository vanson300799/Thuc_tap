# Các lệnh linux cơ bản:
-Dòng lệnh **sell** có dạng tổng quát như sau:
**<center> command   [option]    arguments</center>**
- Trong đó:

    - **command** là tên lệnh.

    - **option** - Các tùy chọn, thường bắt đầu bằng `-` hoặc `--`. Nhiều tùy chọn có thể kết hợp bằng 1 ký hiệu `-`.

    **VD**: `ls -l -a` <=> `ls -la`
    - **argument** - tham số lệnh.
> **chú ý**: dòng lệnh shell có phân biệt chữ thường và chữ hoa

>## Thủ thuật khi gõ lệnh:
- Dùng phím "↑" , "↓" để xem lại các lệnh vừa gõ.
- Dùng tổ hợp `Ctrl` + `C` để hủy lệnh gõ lệnh
- Gõ `clear` để làm mới màn hình Terminal ( hoặc sử dụng tổ hợp `Ctrl` + `L`)
- Dùng phím `Tab` để gõ nhanh tên file hoặc lệnh

# 1) Lệnh trợ giúp : `man` ( manual )

- Dùng để xem hướng dẫn dùng 1 lệnh cụ thể trong Linux .

    ```
    # man <ten lenh>
    ```

- Sử dụng "↑" , "↓" hoặc PgUp , PgDn để di chuyển trong các trang manual .

- Gõ `Shilf` + `G` để đi đến cuối trang manual .

- Gõ `/` + `Từ khóa` để tìm kiếm trong manual , sau đó gõ `n` để đi đến từng kết quả tìm kiếm , gõ `Shift` + `n` để đến kết quả tìm kiếm trước đó .

- Gõ `q` để thoát trợ giúp lệnh .

# 2) Các lệnh file system thiết yếu.

## 2.1) `pwd` ( print name of current/working directory )
- Cho biết thư mục hiện hành đang làm việc .

<img src="../images/02/pwd.png">

## 2.2) `cd` ( change directory ).

- Dùng để chuyển vị trí làm việc sang thư mục khác .

    ``` 
    # cd [path]
    ```
    - `cd /etc` : Chuyển đến thư mục `etc` (thư mục bất kỳ - đường dẫn tuyệt đối).

    - `cd usr` : Chuyển đến thư mục `usr` là thư mục con của thư mục hiện hành - đường dẫn tương đối ).

    - `cd ..` : Chuyển đến thư mục cha.

    - `cd` : Chuyển đến thư mục home của user hiện tại.

    - `cd ~` : Chuyển đến thư mục home của user hiện tại.

    - `cd -` - Chuyển đến thư mục mình vừa rời đi trước đó.

    ```
    [root@localhost ~]# cd /root/file_1/file_1.1
    [root@localhost file_1.1]# cd ..
    [root@localhost file_1]# cd file_1.1
    [root@localhost file_1.1]# cd
    [root@localhost ~]# cd -
    /root/file_1/file_1.1
    [root@localhost file_1.1]# cd ~
    ```

    ## 2.3) `ls` ( list directory contents ).

- ls ( list directory contents )

    ```
    # ls [options] [path]
    ```

    - Options:

        - `-l` :liệt kê chi tiết.
        ```
        [root@localhost ~]# ls -l
        total 4
        -rw-------. 1 root root 1244 May 26 14:26 anaconda-ks.cfg
        drwxr-xr-x. 5 root root   54 May 26 14:34 file_1
        drwxr-xr-x. 3 root root   74 May 26 16:38 file_2
        drwxr-xr-x. 2 root root    6 May 26 15:36 file_3
        ```

        - `-a` :liệt kê tất cả các file ẩn.

        ```
        [root@localhost ~]# ls -a
        .  ..  anaconda-ks.cfg  .bash_history  .bash_logout  .bash_profile  .bashrc  .cshrc  file_1  file_2  file_3  .tcshrc
        ```

        - `-tr` : liệt kê các file theo thứ tự thời gian mới nhất dưới cùng.
         ```
        [root@localhost ~]# ls -trl
        total 4
        -rw-------. 1 root root 1244 May 26 14:26 anaconda-ks.cfg
        drwxr-xr-x. 5 root root   54 May 26 14:34 file_1
        drwxr-xr-x. 2 root root    6 May 26 15:36 file_3
        drwxr-xr-x. 3 root root   74 May 26 16:38 file_2
        ```

        - `-h` : liệt kê file size theo định dạng quen thuộc.

        ```
        [root@localhost ~]# ls -hl
        total 4.0K
        -rw-------. 1 root root 1.3K May 26 14:26 anaconda-ks.cfg
        drwxr-xr-x. 5 root root   54 May 26 14:34 file_1
        drwxr-xr-x. 3 root root   74 May 26 16:38 file_2
        drwxr-xr-x. 2 root root    6 May 26 15:36 file_3
        ```
        
        - `-s` : sắp xêp kích cõ file từ cao xuống thấp.

        ```
        [root@localhost ~]# ls -sl
        total 4
        4 -rw-------. 1 root root 1244 May 26 14:26 anaconda-ks.cfg
        0 drwxr-xr-x. 5 root root   54 May 26 14:34 file_1
        0 drwxr-xr-x. 3 root root   74 May 26 16:38 file_2
        0 drwxr-xr-x. 2 root root    6 May 26 15:36 file_3
        ```

        - `-t` : tìm file được chỉnh sửa gần nhất.
        
        ```
        [root@localhost ~]# ls -tl
        total 4
        drwxr-xr-x. 3 root root   74 May 26 16:38 file_2
        drwxr-xr-x. 2 root root    6 May 26 15:36 file_3
        drwxr-xr-x. 5 root root   54 May 26 14:34 file_1
        -rw-------. 1 root root 1244 May 26 14:26 anaconda-ks.cfg
        ```

## 2.4) `cp` (copy)

- Dùng để copy file / thư mục

    ```
    # cp [options] source destination
    ```

    - options:

        - -r , -R : sao chép toàn bộ thư mục.

        - -v : hiển thị quá trình copy.

        - -v : hiển thị quá trình copy.

        - -p : copy file lẻ và giữ lại thuộc tính của file.

        - -n : ép buộc lệnh copy không được ghi đè nếu file nguồn và file đích cùng tên.

        - -f : ép buộc lệnh copy ghi đè nếu file nguồn và file đích cùng tên.

- Copy file `A` thành file `B`:

    ```
    # touch A.txt       ( tạo file A rỗng )
    # cp A.txt B.txt
    ```

- Copy nhiều file cùng lúc vào thư mục:

    ```
    # touch ./{A,B,C}.txt     ( tạo file rỗng )
    # mkdir -p ./lab/         ( tạo thư mục rỗng )
    # cp A.txt B.txt C.txt ./lab/
    ```

- Copy thư mục `mydir_1` và đổi tên thành `mydir_2` tại thư mục hiện hành :

    ```
    # cp -R mydir_1 mydir_2
    ```

## 2.5) mv ( move )

- Dùng để đổi tên / di chuyển thư mục hoặc file từ nơi này sang nơi khác.

    ```
    # mv [options] source destination
    ```

    - options:

        - `-i` : cảnh báo trước khi di chuyển với tập tin / thư mục mà đích đã có rồi.

        - `-f` : ghi đè khi di chuyển với tập tin / thư mục đích đã có rồi.

        - `-v` : hiển thị quá trình di chuyển , đổi tên.

- Đổi tên file và thư mục :

    ```
    # mv dir1 dir2
    ```

    ```
    [root@localhost file_2]# mv -v bai_1 bai_4
    mv: overwrite ‘bai_4’? yes
    ‘bai_1’ -> ‘bai_4’
    ```
- Di chuyển file vào thư mục :

    ```
    # mv file5 /tmp
    ```
    ```
    [root@localhost ~]# mv -v file_1 file_2
    ‘file_1’ -> ‘file_2/file_1’
    ```
- Di chuyển file `my_file` vào thư mục dir1 đồng thời đổi thành `new_file` :

    ```
    # mv my_file dir1/new_file
    ```
    
    ```
    [root@localhost file_2]# mv -v bai_2 file_1/bai_1
    ‘bai_2’ -> ‘file_1/bai_1’
    ```

## 2.6) `mkdir` ( make directory )

- Dùng để tạo thư mục .
    ```
    # mkdir [options] directory_name
    ```
    - options:

        - `-p` : cho phép tạo cả thư mục con khi chưa có thư mục cha.

            ```
            [root@localhost file_2]# mkdir -pv file_1.4/bai_1 
            mkdir: created directory ‘file_1.4’
            mkdir: created directory ‘file_1.4/bai_1’
            [root@localhost file_2]# mkdir -v file_1.5/bai_2
            mkdir: cannot create directory ‘file_1.5/bai_2’: No such file or directory

            ```

        - `-v` : hiển thị quá trình tạo thư mục.

            ```
            [root@localhost file_2]# mkdir -v bai_2
            mkdir: created directory ‘bai_2’
            ```

        - `-m` : tạo thư mục với phân quyền cụ thể. *

- Tạo nhiều thư mục cùng lúc :

    ```
    # mkdir thu1 thu2 thu3
    = # mkdir /root/thu{1,2,3}
    = # mkdir /root/{thu1,thu2,thu3}
    ```

    ```
    [root@localhost file_2]# mkdir -v test_1,test_2,test_3
    mkdir: created directory ‘test_1,test_2,test_3’
    ```

## 2.7) touch.

- Dùng để tạo file mới ( file rỗng ).

    ```
    # touch <file_name>
    ```
- Tạo nhiều file :

    ```
    # touch file1 file2 file3
    = # touch file{1,2,3}
    = # touch {file1,file2,file3}
    ```

## 2.8) rm ( remove ).

- Dùng để xóa file / thư mục.

    ```
    # rm [options] [file/dir]
    ```

- Lệnh này được coi là 1 lệnh nguy hiểm của Linux .

    - options:

        - `-f` : xóa không cần hỏi.

        - `-i` : hỏi trước khi xóa

        Mặc định , tùy chọn -i được sử dụng .

        - `-R , -r` : xóa toàn bộ thư mục , kể cả thư mục con.

        - `-d` : xóa 1 thư mục rỗng ( = rmdir )

>Chú ý : Lệnh rm -rf / sẽ xóa toàn bộ file system ( nguy hiểm )

        ```
        [root@localhost bai_2]# rm bai_1
        rm: remove regular empty file ‘bai_1’? yes

        [root@localhost file_2]# rm -r bai_2
        rm: remove directory ‘bai_2’? yes
        ```
## 2.9) du ( disk usage ).

- Dùng để xem dung lượng của thư mục .

    ```
    du [option] [path]
    ```

    - Options :

        - `-s` : xuất kết quả theo summarize ( tổng dung lượng ).

        ```
        [root@localhost file_2]# du -ks
        24
        ```

        - `-h` : in kích thước mà người dùng có thể đọc.

        ```
        [root@localhost file_2]# du -kh
        8.0K    ./file_1.1
        8.0K    ./file_1/file_1.1
        0       ./file_1/file_1.2
        0       ./file_1/file_1.3
        8.0K    ./file_1
        0       ./file_1.4/bai_1
        0       ./file_1.4
        0       ./test_1,test_2,test_3
        24K 
        ```

        - `-k` : hiển thị thông tin theo kylobyte.

        ```
        [root@localhost file_2]# du -kh
        8.0K    ./file_1.1
        8.0K    ./file_1/file_1.1
        0       ./file_1/file_1.2
        0       ./file_1/file_1.3
        8.0K    ./file_1
        0       ./file_1.4/bai_1
        0       ./file_1.4
        0       ./test_1,test_2,test_3
        24K 
        ```
        - `-m` : hiển thị thông tin theo megabyte
    
        ```
        [root@localhost file_2]# du -m
        1       ./file_1.1
        1       ./file_1/file_1.1
        0       ./file_1/file_1.2
        0       ./file_1/file_1.3
        1       ./file_1
        0       ./file_1.4/bai_1
        0       ./file_1.4
        0       ./test_1,test_2,test_3
        1       .

        ```

## 2.10) tree.

- Hỗ trợ người dùng liệt kê các file và thư mục tại 1 thư mục theo dạng hình cây rất đẹp và dễ nhìn , nó sẽ quét sâu hết tất cả các sub-folder .

- Sau khi liệt kê hết tất cả thì chương trình tree sẽ trả về thông tin tổng số lượng file hoặc thư mục đã được liệt kê .

- Mặc định lệnh tree không được cài đặt trên Linux . Cài đặt như sau :

    ```
    # yum install tree      (RHEL/CentOS)
    # apt-get install tree  (Ubuntu/Debian)
    ```
    ```
    [root@localhost file_2]# yum install tree
    Loaded plugins: fastestmirror
    Loading mirror speeds from cached hostfile
    * base: mirror.tino.org
    * extras: mirror.tino.org
    * updates: mirror.tino.org
    ```
- Cấu trúc lệnh :

    ```
    # tree [option] [path_directory]
    ```

    - options:

        - `-a` : liệt kê cả các file / thư mục ẩn.
            ```
            [root@localhost ~]# tree -a /root/file_2
            /root/file_2
            ├── bai_3
            ├── bai_4
            ├── file_1
            │   ├── bai_1
            │   ├── file_1.1
            │   │   ├── bai_1
            │   │   ├── bai_2
            │   │   └── bai_3
            │   ├── file_1.2
            │   │   ├── bai_1
            │   │   ├── bai_2
            │   │   └── bai_3
            │   └── file_1.3
            ├── file_1.1
            │   ├── bai_1
            │   ├── bai_2
            │   └── bai_3
            ├── file_1.4
            │   └── bai_1
            └── test_1,test_2,test_3

            8 directories, 12 files

            ```

            - `-L + [number]` : giới hạn số lượng sub-directory sẽ được liệt kê.

            ```
            [root@localhost ~]# tree -L 3 /root
            /root
            ├── anaconda-ks.cfg
            ├── file_2
            │   ├── bai_3
            │   ├── bai_4
            │   ├── file_1
            │   │   ├── bai_1
            │   │   ├── file_1.1
            │   │   ├── file_1.2
            │   │   └── file_1.3
            │   ├── file_1.1
            │   │   ├── bai_1
            │   │   ├── bai_2
            │   │   └── bai_3
            │   ├── file_1.4
            │   │   └── bai_1
            │   └── test_1,test_2,test_3
            └── file_3

            10 directories, 7 files
            ``` 

            - `-d` : chỉ liệt kê thư mục , không liệt kê file.

            ```
            [root@localhost ~]# tree -d /root/file_2
            /root/file_2
            ├── file_1
            │   ├── file_1.1
            │   ├── file_1.2
            │   └── file_1.3
            ├── file_1.1
            ├── file_1.4
            │   └── bai_1
            └── test_1,test_2,test_3

            8 directories
            ```

# 3) Các lệnh hệ thống.

## 3.1) shutdown.

- Tắt hệ thống hoặc khởi động lại.

    ```
    # shutdown [options] [time] [wall]
    ```

    - options:

        - `-h` : shutdown

        - `-r` : restart

        - `-c` : cancel pending shutdown

    - Time:

        - `now` : thực hiện ngay lập tức.

        - `hh:mm` : ấn định thời gian ( hẹn giờ ).

        - `+m` : sau `m` phút sẽ thực hiện.

    - `Wall` : Message thông báo.

## 3.2) `reboot`

- Khởi động lại Server :

    ```
    # reboot
    ```

## 3.3) `init`

- ```
  # init [number]
  ```

    - `number` :

        - `3` : restart.

        - `0` : shutdown
## 3.4) `date`

- Xem ngày giờ hệ thống :

    ```
    # date
    ```
    
    ```
    [root@localhost ~]# date
    Wed May 27 15:30:16 +07 2020
    ```