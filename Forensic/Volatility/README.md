> The true forenSeek
>> Giữ nguyên hiện trường là việc cần thiết trong quá trình điều tra số. Một trong những file lưu trữ hình ảnh của RAM trong quá trình làm đề thi được leak ra cho các chiến binh. Cho mình thấy các cậu tìm được gì nào :)
https://drive.google.com/file/d/1PMbu0KbORvRD7Sp2-V-2e-97YIJUY86p/view?usp=sharing
* Mình không biết bài này do vấn đề gì nhưng chỉ cần sử dụng commad `strings`:



`strings DESKTOP-K5GNI06-20211028-104628.raw | grep Flag{`





![image](https://user-images.githubusercontent.com/68783065/140452925-ef17a2d8-94f8-4ea2-afe2-ab834206473a.png)
![image](https://user-images.githubusercontent.com/68783065/140452929-a19a42ea-8ebe-48ae-a458-5cb1c92018d9.png)
* Flag is: `Flag{7ef31e58bd4086e294b4d700c721f35f}`
