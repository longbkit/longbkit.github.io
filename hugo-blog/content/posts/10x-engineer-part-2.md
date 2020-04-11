---
title: "Sếp nhớ trả lương em gấp 10 nha (phần 2) - HĐH Ubuntu"
date: 2020-03-10T21:11:05+07:00
tags:
    - 10x-engineer
    - soft-skill
categories:
    - Sếp nhớ trả lương em gấp 10 nha
    - Thiết lập môi trường dev
draft: false
---

Phần trước tôi đã nhắc đến tất cả công việc nếu bạn dùng một công cụ đúng thì hiệu quả sẽ tăng lên đáng kể. 


Bạn có thể xem lại phần 1 tại đây:
>[Sếp nhớ trả lương em gấp 10 nha (phần 1)]({{< ref "10x-engineer-part-1.md" >}})


Hình ảnh máy gặt đập liên hợp ở dưới là một ví dụ rất rõ minh chứng cho điều này.

![Tool](/img/rice-field.jpg "Với chiếc máy gặt đập liên hợp này không còn cảnh một dàn các bác nông dân cầm liềm để gặt lúa, rồi vác từng bao về nhà để xay nữa.")

Hôm nay với tư cách là một người dùng Windows lâu năm, đã từng cảm giác không thể thiếu Windows nhưng sau khoảng một tháng dùng Ubuntu 18.04 với một số kỹ thuật tweak lại một cách thích hợp nhất cho developer giờ đây tôi lại cảm giác không thể thiếu Ubuntu. Đoạn dưới đây sẽ hướng dẫn các bạn cách setup Ubuntu làm sao để có thể tận dụng tối đa hiệu suất lập trình, vd cài đặt phím tắt, cài terminal số một zsh kèm các plugins thiết yếu.


### 1. Cài ibus-unikey để hỗ trợ đánh tiếng Việt

Lưu ý: trình đánh tiếng Việt này sẽ không tương thích với các ứng dụng cài bằng snap, do đó để đánh được tiếng Việt trong ứng dụng luôn cài đặt ứng dụng từ đuôi .deb (Debian). Ví dụ bạn có thể vào website chính hãng skype / chrome / slack để tải .deb về cài đặt, sẽ có thể đánh tiếng Việt phà phà.

### 2. Tuyệt chiêu 10x nằm phần lớn ở đây với các bạn hay dùng câu lệnh 

Bạn có muốn khi làm việc với các dòng lệnh bash, vd cài đặt npm, cài đặt chương trình, test api bằng curl, watch, chạy docker, ... hiệu suất sẽ tăng lên đáng kể không?

Vậy hãy theo các bước hướng dẫn bên dưới, thì bạn sẽ có thể biến terminal của bạn thành như sau:

![zsh terminal](/img/zsh-terminal.gif "Termninal nâng cấp lần 1")

Cài zsh + oh-my-zsh và zsh plugins, đặc biệt là zsh-autosuggestions
https://github.com/robbyrussell/oh-my-zsh

* Tham khảo thêm thông tin của plugins zsh-autosuggestions ở đây https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md

* Chuyển đổi qua theme agnoster để hiển thị tốt hơn (https://github.com/agnoster/agnoster-zsh-theme), lưu ý có thể custom cách hiển thị cho theme agnoster để command prompt hiển thị ngắn gọn và súc tích hơn, bạn có thể tham khảo thêm trong link. 
* Cài font powerline-fonts https://github.com/Lokaltog/powerline-fonts
* Thêm dòng sau DEFAULT_USER=$USER vào file ~/.zshrc
* Và có thể enable rất nhiều plugins tuyệt vời cho oh-my-zsh. Ví dụ một số plugins tiêu biểu

plugins=(git command-not-found extract git-extras history-substring-search zsh-autosuggestions)

* Bạn có thể thấy
> plugin ```git``` sẽ bổ sung tên git branch khi ở trong 1 folder có dùng git.

> plugin ```command-not-found``` sẽ hỗ trợ suggest package để cài đặt nếu chưa có

> plugin ```history-substring-search``` sẽ hỗ trợ nhập 1 đoạn text trong câu, bấm nút lên (Up) và terminal sẽ show câu lệnh gần nhất có chứa đoạn text đó. Đặc biệt tiện trong trường hợp chạy các câu lệnh dài như docker, trong hình là tác giả chỉ nhớ là có chạy docker neo4j nhưng không nhớ chính xác câu lệnh.

![zsh plugins](/img/zsh-plugins.png "Plugins và ý nghĩa")

> plugin ```autosuggestions``` là khi đánh câu lênh, termnial sẽ gợi nhắc câu lệnh gần đây nhất khớp với câu lệnh đang đánh, vd trước đó nếu đã đánh ```git checkout master```, lúc đánh ```git``` thì termninal tự hiện ra dấu nhắc full câu lệnh ```git checkout master``` với phần gợi nhắc được làm mờ đi, nếu đúng là câu lệnh bạn muốn dùng, chỉ cần nhấp nút qua phải (Right) là được.

![zsh plugins](/img/zsh-substring-plugin.png)


### 3. Alias - tiết kiệm thêm vài giây cuộc đời

bash script của Linux có hỗ trợ đặt alias hay có thể hiểu là lệnh viết tắt rất tiện. Ví dụ bạn hình dung một số trường hợp sau:

* git checkout: ```git checkout master```, nếu có alias ```gco``` thì chỉ cần đánh ```gco master```
* Siêu cấp hơn: khi cần add files, commit, push lên remote origin, chúng ta thường đánh 3 câu lệnh

```git add .```
```git commit -m 'message'```
```git push origin master```

Nay nếu setup alias, chúng ta có thể chỉ cần đánh lệnh ```gacp 'message'```, a gợi nhắc ta chữ add, c gợi nhắc chữ commit and p gợi nhắc chữ push, vẫn rất dễ nhớ và mình không nói ngoa, bạn có thể thử kiểm nghiệm xem tiết kiệm được bao nhiêu giây cuộc đời nào?

Bạn có thể setup lệnh ```gacp``` bằng cách chèn các câu lệnh bên dưới vào file ~/.zshrc hoặc ~/.bashrc:

```git config --global alias.acp '!f() { git add -A && git commit -m "$@" && git push; }; f'```

```git config --global alias.cp '!f() { git commit -m "$@" && git push; }; f'```

```alias gacp="git acp"```

* TODO: chỗ này mình sẽ publish cho các bạn một git repo tổng hợp các alias xịn sò nha. Nhớ nhắc mình nếu chờ hoài chưa thấy, và mình nhắc lại quan trọng là tư duy tối ưu, nếu bạn luôn tự đặt câu hỏi làm sao để tối ưu bằng alias, bạn sẽ tự sáng tạo và tìm ra vô số cách, hoặc đã có rất nhiều git repo làm sẵn điều này cho bạn.

### 4. Hỗ trợ chia tách cửa sổ câu lệnh

Cài terminator để hỗ trợ chia cửa sổ termninal thành nhiều ô nhỏ, rất tiện trong các trường hợp cần chạy nhiều câu lệnh hoặc theo dõi nhiều kết quả termninal đồng thời.

![](/img/10x-terminator.png "Multi-tasking như thế này")

Cách cài đặt: ```sudo apt install terminator```

https://linux.die.net/man/1/terminator

Các phím tắt:

> ```Ctrl+Shift+O``` chia terminal theo chiều ngang
> ```Ctrl+Shift+E``` chia terminal theo chiều dọc 
> ```Ctrl+Shift+Right``` di chuyển qua cửa sổ bên phải
> ```Ctrl+Shift+S``` Ẩn / hiện thanh cuộn
> ```Ctrl+Shift+N``` hoặc ```Ctrl+Tab``` chuyển cửa sổ theo thứ tự từ trái qua phải từ trên xuống dưới
> ```Ctrl+Shift+P``` hoặc ```Ctrl+Shift+Tab``` chuyển cửa sổ theo tứ tự từ phải qua trái từ dưới lên trên
> ```Alt+UpMove``` chuyển qua khung lệnh phía trên khung cửa sổ hiện tại

### 5. Cài brew để tiện cài đặt nhiều chương trình khác 
http://linuxbrew.sh/

### 6. Cài đặt docker & docker-compose để dễ dàng chạy các service bên thứ ba cũng như deploy phần mềm

Ví dụ bạn muốn vọc wordpress để tự tạo website cho mình, mà để cài wordpress phải cài đặt nào là database, nào là apache web server, nào là php, rồi wordpress? Với docker & docker-compose chỉ một nốt nhạc thôi bạn à. Điều này làm cho việc vọc vạch của bạn trở nên dễ hơn gấp nhiều lần, từ đó động lực để vọc cái mới của bạn cũng tăng nhiều, dẫn tới bạn biết nhiều hơn, giỏi nhanh hơn. Khi biết thêm gì nhớ nhắn nhỏ sếp bạn một câu để sếp biết nhé.

Thử ngay nào: nếu chưa biết cách cài đặt docker & docker-compose, bạn có thể theo hướng dẫn ở đây 
* Tiếng Anh: https://docs.docker.com/compose/install/
* Tiếng Việt: https://www.thegioimaychu.vn/blog/ao-hoa/huong-dan-cai-dat-docker-community-edition-va-docker-compose-tren-ubuntu-windows-va-macos-p4441/

Sau khi cài đặt xong, tải file này xuống [link tải](/src-ref/docker-compose-wordpress.yml)

Tiếp đến, bạn vào thư mục chứa file vừa tải, đánh lệnh ```docker-compose -f docker-compose-wordpress.yml up```

Và oh la la, wordpress đã lên và sẵn sàng cho bạn tại địa chỉ [http://localhost:8000](http://localhost:8000)

### 7. Phần mềm chụp ảnh màn hình và ghi chú, minh họa siêu cấp

https://github.com/lupoDharkael/flameshot#install

Để tiện sử dụng, sửa lại nút Print Screen để map với chương trình này. Sau đó mỗi lần bấm Print Screen sẽ qua mode chụp hình với flameshot.

Cách chỉnh hotkey lại:

* Bỏ mapping nút PrtScr the PrtScr binding by this command

```gsettings set org.gnome.settings-daemon.plugins.media-keys screenshot ''```
* Đến mục Settings -> Devices -> Keyboard và cuộn xuống dưới, bấm nút + để tạo shortcut tùy chỉnh

Nhập: ```flameshot```, command: ```/usr/bin/flameshot gui```

![](/img/screenshot-flameshot.png)

* Một số hotkey của flameshot: nhấn nút space để chỉnh màu sắc khi vẽ, cuộn chuột lên / xuống để tăng kích thước chữ hoặc độ dày viền.


### 8. Nếu bạn cần dùng vpn, hãy cài openvpn

### 9. Cài hot corners để khi đưa chuột vào các góc sẽ có hiệu ứng chuyển qua màn hình chọn cửa sổ rất ảo diệu

https://www.fosslinux.com/4184/how-to-enable-hot-corners-in-ubuntu-18-04.htm/


### 10. Phần mềm ghi chú evernote

 https://github.com/klaussinani/tusk/releases/tag/v0.11.0


### 11. Cài đặt để giao diện đẹp lung linh như máy Mac (bao gồm cả tweek font chữ, nhìn rất xịn sò)

https://vitux.com/how-to-change-login-lock-screen-background-in-ubuntu/


## Troubleshooting

Một số  lưu ý khi cài đặt dual book Ubuntu & Windows:

* Kiểm tra windows đang boot ở mode nào (Legacy vs UEFI), nếu là mode UEFI thì ubuntu cũng cần cài ở mode đó

* Một số máy ko cho chọn boot USB Ubuntu ở mode Legacy thì sẽ bị lỗi vì ubuntu cài ở mode UEFI trong khi win chạy ở mode legacy => vào https://help.ubuntu.com/community/Boot-Repair xem hướng dẫn để convert về mode legacy

* Có 2 loại format ổ cứng, MBR hoặc GPT, MBR thì hỗ trợ tối đa 3 primary partition và 1 extended partition.

* Chỉ có partition primary mới boot được

* Xử lỗi ko boot đc sau khi cài ubuntu, tool boot-repair: https://help.ubuntu.com/community/Boot-Repair

## Video

TODO: đã qua hai bài rồi, để các bạn có thể hình dung rõ hơn 10x engineer như thế nào, mình sẽ up video mình dùng máy tính như thế nào. Một lần nữa, nhớ nhắc nếu mình lỡ quên nghen các bạn :-D

Bạn có thể xem tiếp phần 3 tại đây:
>[Sếp nhớ trả lương em gấp 10 nha (phần 3) - trình duyệt web]({{< ref "10x-engineer-part-3.md" >}})
