---
title: "Sếp nhớ trả lương em gấp 10 nha (phần 4) - IDE"
date: 2020-03-20T21:11:05+07:00
tags:
    - 10x-engineer
    - soft-skill
categories:
    - Sếp nhớ trả lương em gấp 10 nha
    - Thiết lập môi trường dev
draft: false
---

# Các loại IDE dành cho lập trình viên

IDE là chương trình dành để viết các dòng lệnh ấy các bạn, IDE nếu chọn và cài đặt đúng không thể nghi ngờ gì có thể boost performance của bạn lên cả trăm lần.

Trong bài này, mình sẽ chia sẻ một số IDE phổ biến và cách thiết lập tối ưu cho môi trường code.

Bạn có thể xem lại các phần trước tại đây:
>[Sếp nhớ trả lương em gấp 10 nha (phần 1)]({{< ref "10x-engineer-part-1.md" >}})

>[Sếp nhớ trả lương em gấp 10 nha (phần 2)]({{< ref "10x-engineer-part-2.md" >}})

>[Sếp nhớ trả lương em gấp 10 nha (phần 3)]({{< ref "10x-engineer-part-3.md" >}})


### 1. vim

Phần này thực sự là hardcore nè các bạn.

Mình có cơ duyên làm việc chung với một anh bạn tên là Minh Phạm, và môi trường làm việc của anh ấy chỉ có ```terminal``` và ```vim``` thôi, kèm một đến hai cửa sổ Chrome, mọi giao tiếp chat, email để qua giao diện web. Ấy thế mà performance khi làm việc phải nói là siêu tốc.

Bài viết này mình sẽ nhờ sự cộng tác của anh bạn Minh Phạm để có thể mô tả được toàn bộ tinh túy của ```vim```. Các bạn nghe không nhầm đâu, dùng vim làm IDE cho lập trình.

Tuy nhiên trước hết, mình khuyến cáo bài viết này có thể hơi extreme, trong thực tế, các IDE như Visual Studio Code hay WebStorm đều có nhiều tiện ích mở rộng siêu hay, mặc dù không phủ nhận ```vim``` rất flexible và cũng có vô vàn tiện ích mở rộng nhưng xét về nhiều mặt khi code và debug thì có lẽ cần phân tích kỹ hơn. Sẽ có không ít ngữ cảnh / mục đích sử dụng ```vim``` sẽ tỏa sáng nhưng ngược lại vẫn không ít trường hợp Visual Studio Code / Webstorm là lựa chọn tuyệt vời hơn.

...

### 2. Visual Studio Code

Từ khi ông Satya Nadella lên CEO của Microsoft chúng ta thấy Microsoft chuyển dịch rất mạnh về mảng cloud software, đồng thời rất tích cực trong việc đóng góp cho cộng đồng mã nguồn mở, với các động thái như mua lại github, hay hỗ trợ tích hợp môi trường Linux vào ngay trong HĐH Windows, và Visual Studio Code là một trong những động thái rất đáng hoan nghênh đó.

Hiện nay có thể nói là IDE này là IDE yêu thích nhất của mình cho khá nhiều công việc, bao gồm cả coding website, chỉnh sửa các loại config, ghi chú, hay cả viết blog (blog này mình viết bằng Visual Studio Code trên cú pháp markdown đấy).

Dưới đây là một số tổng hợp các plugin rất tuyệt vời cho Visual Studio Code mà có thể boost performance của bạn lên gấp nhiều lần.

* https://ehkoo.com/bai-viet/vscode-must-have-plugins
* https://techtalk.vn/20-bo-visual-studio-code-mo-rong-tot-nhat-cho-cac-nha-phat-trien-front-end.html
* https://viblo.asia/p/nhung-plugin-can-thiet-cho-visual-studio-code-Ljy5VMRMlra
* https://quantrimang.com/extension-visual-studio-code-cho-lap-trinh-de-dang-hon-163456
(rất thích plugin Rest Client được đề xuất ở đây để làm việc với API)

Rất tiếc, mình chưa thấy một trang blog nào thực sự tổng hợp hết tinh tùy của Visual Studio Code, tuy nhiên nếu bạn theo các link ở trên sẽ thu lượm được kha khá plugin bổ ích. Hẹn các bạn trong một series bài viết khác chuyên sâu hơn về Visual Studio Code, hy vọng sẽ giúp ích.

À, bạn nhớ skill hotkey thần thánh mình đã viết ở bài đầu tiên nhé. Đặt câu hỏi là VS Code có những hotkeys nào hay, và tự mình đi tìm nha.

### 3. Webstorm

IDE này cũng rất chất, chỉ tội là có phí.

Dưới đây là tổng hợp một vài plugins chất cho WebStorm, rất tiếc ít có bài viết tiếng Việt nào chất lượng nói về WebStorm hiện tại nên mình share tạm link tiếng Anh:
* https://medium.com/@jughosta/25-productivity-tips-and-tricks-for-webstorm-and-other-intellij-idea-based-ides-d7430ee32a61
* https://blog.codota.com/top-25-javascript-plugins-for-webstorm-intellij/
* https://www.sitepoint.com/productivity-tips-for-webstorm-and-angular-part-1/
* https://www.sitepoint.com/productivity-tips-for-webstorm-and-angular-part-2/
* Dành cho lập trình viên php: https://github.com/WyriHaximus/awesome-phpstorm

### 4. Các trình IDE khác 

Ngoài các IDE trên, có rât nhiều IDE khác tùy vào ngôn ngữ / framework các bạn đang sử dụng, vd bạn có thể dùng Android Studio để code app Android, XCode để code app iOS / macOS, Eclipse IDE (Android Studio là mở rộng của Eclipse IDE, thường hay được dùng để code C/C++ hay Java, hỗ trợ customize mạnh). Ngoài ra, mình biết không ít bạn đang dùng nhiều trình soạn thảo text khác để code như Sublime Text, Atom, Notepad++, mỗi phần mềm đều có ưu nhược riêng, và đều là lựa chọn tốt cho một số mục đích khác nhau. Các bạn có thể chia sẻ thêm về trải nghiệm của bạn với từng IDE ở bên dưới phần comment cho mọi người cùng học hỏi nhé!

### Phần hay nhất của IDE

Bạn có biết, điều gì hay nhất của IDE mà bạn có thể chưa tận dụng được?
Theo mình, code snippet (trong VSCode) hay Live Templates (trong webstorm) chính là điều đó.
Nếu bạn là lập trình viên, bạn sẽ rất hay làm việc với vòng for, có thể là thế này

```for (i = 0; i++; i<n) { console.log("i", i); }```

Vậy, tại sao bạn cứ lặp đi lặp lại chính mình làm gì, chỉ cần cài sẵn code snippet, chỉ cần tạo code snippet mẫu và gán lệnh tắt cho nó, bạn sẽ tiết kiệm được vô vàn công sức và thời gian.

![code snippet](/img/10x-code-snippets.gif "VS Code")

![code snippet](/img/10x-live-templates.gif "Webstorm")

Phần này có rất nhiều thủ thuật hay đi kèm, mình sẽ share thêm một bài chuyên sâu về code snippet sau bạn nhé.

* Code snippets cho Visual Studio Code https://code.visualstudio.com/docs/editor/userdefinedsnippets
* Live templates cho Webstorm https://www.jetbrains.com/help/webstorm/using-live-templates.html
* Gần như tất cả IDE đều có tính năng tương tự, nếu bạn dùng IDE khác, hãy thử tìm hiểu và comment ở bên dưới để chia sẻ thêm với bạn đọc nhé.

Bạn có thể xem tiếp phần 5 tại đây:
>[Sếp nhớ trả lương em gấp 10 nha (phần 5)]({{< ref "10x-engineer-part-5.md" >}})
