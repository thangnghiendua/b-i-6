LẬP TRÌNH GAME DÒ MÌN
Lịch sử về game:
-Lịch sử của trò chơi dò mìn có thể được truy nguyên từ những năm 1970, khi một trò chơi có tên Cube được phát triển bởi Robert Donner. Trò chơi này có các ô vuông có thể chứa mìn, và người chơi phải sử dụng logic để xác định vị trí của mìn mà không chạm vào chúng.
-Năm 1989, một trò chơi có tên Sweep được phát triển bởi Bruce Shifflett. Trò chơi này tương tự như Cube, nhưng nó có giao diện người dùng đồ họa.
-Năm 1990, trò chơi dò mìn chính thức được phát hành như một phần của hệ điều hành Windows 3.0. Trò chơi này nhanh chóng trở nên phổ biến và được nhiều người yêu thích.

Tổng quan về cách hoạt động của trò chơi:
-Trò chơi Minesweeper bắt đầu với một bảng 10x10 ô. Trong số các ô này, có 10 ô chứa quả mìn. Các ô còn lại không chứa mìn.
-Mục tiêu của trò chơi là mở tất cả các ô không chứa mìn mà không mở bất kỳ ô nào chứa mìn.
-Người chơi thực hiện điều này bằng cách nhập các ký tự. Ký tự o được sử dụng để mở một ô. Ký tự f được sử dụng để đặt hoặc xóa cờ trên một ô.
-Nếu người chơi mở một ô chứa mìn, trò chơi kết thúc và người chơi thua.
-Nếu người chơi mở tất cả các ô không chứa mìn, trò chơi kết thúc và người chơi thắng.



PHẦN CODE
- thư viện cần thiết:
 
-Cung cấp các hàm đầu vào và đầu ra cần thiết trong C++. Cho phép bạn nhận đầu vào từ người dùng thông qua bàn phím và hiển thị đầu ra trên màn hình.
Một số mẹo chơi trò chơi:
-Sử dụng các số trên các ô để suy ra vị trí của các quả mìn. Ví dụ, nếu một ô có số 3, thì có ba quả mìn nằm gần đó.
-Dùng cờ để đánh dấu các ô có khả năng chứa mìn. Điều này sẽ giúp bạn tránh mở các ô đó.
-Hàm cell_number():
 
-Hàm này được sử dụng để gán số cho các ô trên bảng. Số này cho biết có bao nhiêu quả mìn nằm gần ô đó.
-Hàm này lặp qua tất cả các ô trên bảng. Đối với mỗi ô, hàm kiểm tra xem ô có chứa quả mìn hay không. Nếu ô có chứa quả mìn, hàm sẽ tăng số của ô đó lên 1.
-Sau khi lặp qua tất cả các ô, hàm sẽ trả về mảng chứa các số của các ô.
-Hàm create_mine_positions():
 
-Hàm này được sử dụng để tạo vị trí của các quả mìn trên bảng. Nó sử dụng hàm rand() để tạo các số ngẫu nhiên trong khoảng từ 0 đến 9.
-Hàm này lặp lại 10 lần, mỗi lần tạo một số ngẫu nhiên. Nếu số ngẫu nhiên đó chưa được sử dụng, hàm sẽ lưu trữ số đó vào một mảng.
-Sau khi lặp 10 lần, hàm sẽ trả về mảng chứa các vị trí của các quả mìn.
-Hàm create_table():
 
-Hàm này được sử dụng để tạo bảng trò chơi. Nó sử dụng hàm cell_number() để gán số cho các ô.
-Hàm này lặp qua tất cả các ô trên bảng. Đối với mỗi ô, hàm sẽ sử dụng hàm cell_number() để lấy số của ô đó.
-Sau khi lặp qua tất cả các ô, hàm sẽ trả về mảng chứa các ký tự của các ô
-Hàm print_table():
 
-Hàm này được sử dụng để in bảng trò chơi ra màn hình. Nó sử dụng các ký tự * để biểu thị các ô chưa được mở, 1 đến 9 để biểu thị các ô đã được mở có chứa số mìn gần đó, và B để biểu thị các ô đã được mở có chứa quả mìn.
-Hàm này lặp qua tất cả các ô trên bảng. Đối với mỗi ô, hàm sẽ sử dụng ký tự thích hợp để in ra màn hình.
-Hàm open_cell():
 
-Hàm này được sử dụng để mở ra một ô trên bảng. Nó sử dụng hàm reveal() để thực hiện việc này.
-Hàm này yêu cầu người chơi nhập chỉ số hàng và chỉ số cột của ô cần mở. Sau khi nhận được đầu vào từ người chơi, hàm sẽ sử dụng hàm reveal() để mở ô đó.





-Hàm place_or_remove_flag():
 
-Hàm này được sử dụng để đặt hoặc xóa cờ trên một ô trên bảng. Nó sử dụng các ký tự * và F để biểu thị các ô không có cờ và ô có cờ, tương ứng.
-Hàm này yêu cầu người chơi nhập chỉ số hàng và chỉ số cột của ô cần đặt hoặc xóa cờ. Sau khi nhận được đầu vào từ người chơi, hàm sẽ sử dụng ký tự thích hợp để cập nhật ô đó.




-Hàm input_symbol():
 
-Hàm này được sử dụng để đọc đầu vào từ người chơi. Nó sử dụng biến symbol để lưu trữ ký tự đầu vào.
-Hàm này sẽ lặp lại cho đến khi người chơi nhập một ký tự hợp lệ.

-Hàm reveal():
 
-Hàm này được sử dụng để mở ra một ô trên bảng. Nó có hai tham số đầu vào là chỉ số hàng và chỉ số cột của ô cần mở.
-Đầu tiên, hàm kiểm tra xem ô đã được mở hay chưa. Nếu ô đã được mở, hàm sẽ không làm gì cả.
-Nếu ô chưa được mở, hàm sẽ kiểm tra xem ô có chứa quả mìn hay không. Nếu ô chứa quả mìn, hàm sẽ in ra màn hình ký tự B và kết thúc trò chơi.
-Nếu ô không chứa quả mìn, hàm sẽ in ra màn hình số mìn nằm gần ô đó. Nếu không có quả mìn nào nằm gần ô đó, hàm sẽ in ra màn hình ký tự ..
-Hàm end_game_win_check():
 
-Hàm này được sử dụng để kiểm tra xem trò chơi đã kết thúc chưa. Nó trả về true nếu trò chơi đã kết thúc với chiến thắng và false nếu trò chơi đã kết thúc với thất bại.
-Hàm này kiểm tra xem tất cả các ô không chứa mìn đã được mở chưa. Nếu tất cả các ô không chứa mìn đã được mở, hàm sẽ trả về true. Nếu không, hàm sẽ trả về false.
-Cụ thể, hàm này lặp qua tất cả các ô trên bảng. Đối với mỗi ô, hàm kiểm tra xem ô đó có chứa quả mìn hay không. Nếu ô đó không chứa quả mìn và ô đó chưa được mở, hàm sẽ trả về false.
-Nếu hàm này lặp qua tất cả các ô mà không tìm thấy bất kỳ ô nào không chứa mìn chưa được mở, hàm sẽ trả về true.





-Hàm game():
 
-Hàm này là hàm chính của trò chơi. Nó thực hiện vòng lặp chơi trò chơi.
-Vòng lặp này sẽ lặp lại cho đến khi trò chơi kết thúc. Trong mỗi vòng lặp, hàm sẽ thực hiện các bước sau:
1.	In bảng trò chơi ra màn hình.
2.	Yêu cầu người chơi nhập một ký tự.
3.	Dựa trên ký tự đầu vào, thực hiện hành động thích hợp.
-Các hành động thích hợp bao gồm mở một ô, đặt hoặc xóa cờ, hoặc thoát khỏi trò chơi.
-Vòng lặp sẽ kết thúc khi trò chơi kết thúc. Nếu trò chơi kết thúc với chiến thắng, hàm sẽ in ra màn hình thông báo "YOU WIN!". Nếu trò chơi kết thúc với thất bại, hàm sẽ in ra màn hình thông báo "GAME OVER!".
Hàm main():
 
-là hàm chính của chương trình. Nó sẽ khởi chạy trò chơi.

-Kết luận
-Trò chơi dò mìn là một trò chơi trí tuệ đơn giản nhưng thú vị. Nó đòi hỏi người chơi phải suy luận logic để tìm ra vị trí của các quả mìn. Trò chơi có thể chơi một mình hoặc nhiều người.
-Trò chơi dò mìn có nhiều lợi ích cho người chơi. Nó giúp người chơi rèn luyện khả năng suy luận logic, khả năng tập trung và khả năng giải quyết vấn đề. Trò chơi cũng giúp người chơi thư giãn và giải trí.

-Một số tính năng mà nhóm mình sẽ cải tiến trong tương lai:
-Thêm các cấp độ khó khác nhau. Điều này sẽ khiến trò chơi trở nên thú vị hơn đối với những người chơi có kinh nghiệm.
-Tạo một giao diện đồ họa. Điều này sẽ làm cho trò chơi trở nên hấp dẫn hơn đối với người chơi.


MỤC LỤC
Lịch sử về game……………………………………………………… 1
Tổng quan về cách hoạt động của trò chơi………………….…….... 1
Phần Code…………………………………………………………… 2
-Thư viện cần thiết………………………………………….……….. 2
-Hàm cell_number…………………………………………………... 2
-Hàm create_mine_positions………………………………………... 3
-Hàm create_table…………………………………………………… 4
-Hàm print_table…………………………………………………….. 4
-Hàm open_cell…………………………………………..………….. 5
-Hàm place_or_remove_flag………………………………………... 6
-Hàm input_symbol………………………………………………….. 7
-Hàm reveal………………………………………………………….. 7
-Hàm end_game_win_check………………………………………... 8
-Hàm game……………………………………………………...…… 9
-Hàm main…………………………………………….…………… 10
-Kết luận……………………………………………………………. 10
*Một số tính năng mà nhóm mình sẽ cải tiến trong tương lai….... 10








