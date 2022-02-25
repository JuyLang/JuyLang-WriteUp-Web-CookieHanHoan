> Để nhiều loại Trình duyệt và Web Server có thể nói chuyện và hiểu được nhau thì họ phải sử dụng chung một giao thức có tên gọi là HTTP Protocol. Khi người dùng bắt đầu truy cập Web, trình duyệt sẽ chuyển những hành động của họ thành yêu cầu (Request) tới Web Server. Còn Web Server sẽ trả lời (Response) xem có thể đáp ứng hay từ chối cung cấp thông tin cho trình duyệt.

> Ví dụ, bạn Gà muốn LẤY danh sách các thử thách trong cookiearena<chấm>org, ở đường dẫn /challenges bằng TRÌNH DUYỆT Chrome. Trình duyệt của Gà sẽ phải điền vào một cái form mẫu có tên gọi là HTTP Header và gửi đi. Mỗi yêu cầu sẽ được viết trên một dòng, và nội dung của mỗi yêu cầu sẽ phải viết đằng sau dấu hai chấm.

> Hãy đoán xem trong thử thách này có những Header thú vị nào nha.




>http://chal3.web.letspentest.org/ 



* Use `curl` nhưng cần `credential`: `curl --request POST http://chal3.web.letspentest.org/`


![image](https://user-images.githubusercontent.com/68783065/140493495-67be8d6a-39fd-4915-900a-b1926d201020.png)



* `curl -G http://chal3.web.letspentest.org/` nhận được `Credential`:



![image](https://user-images.githubusercontent.com/68783065/140493849-40a327f6-31da-402f-a975-cd371f0817a6.png)


* `curl --request POST http://chal3.web.letspentest.org/ --user gaconlonton:cookiehanhoan` và get Flag thôi:


![image](https://user-images.githubusercontent.com/68783065/140493909-165e14fa-7384-467b-8dba-8411b9a38314.png)


* Flag is: `Flag{m4g1c@l_h34d3r_xD}`




