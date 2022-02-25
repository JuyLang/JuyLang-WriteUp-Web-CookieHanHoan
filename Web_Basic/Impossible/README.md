> Học lỏm được công thức chế tạo lá chắn tàng hình của Hazy. Gà nhanh chóng đem về xây dựng hệ thống phòng thủ của riêng mình. Liệu nó có làm khó được Mèo Yang Hồ không?




> http://chal7.web.letspentest.org/ 



* Phân tích function `checkPass()`:


![image](https://user-images.githubusercontent.com/68783065/140498011-a6494f1a-195d-492b-a301-6ccc6caf6332.png)


  * `Decode` đoạn `base64`: `echo 'Y29va2llaGFuaG9hbg==' | base64 -d `


![image](https://user-images.githubusercontent.com/68783065/140499045-eb76bdef-ff63-41ac-85d1-2af86967806c.png)



  * Password ở đây là `cookiehanhoan` nhưng khi post request sẽ bị mất `cookiehanhoan`
  * Do đó input password sau khi bị thay thế vẫn sẽ phải giữ nguyên là `cookiehanhoan`
  * Suy ra password ở đây sẽ là: `cookiecookiehanhoanhanhoan`


![image](https://user-images.githubusercontent.com/68783065/140498595-e0168af0-53f7-487c-a50b-36126518aefb.png)



![image](https://user-images.githubusercontent.com/68783065/140498640-672c752c-fbed-4bd3-8c40-ba55cef355cf.png)



* Flag is: `Flag{Javascript_is_not_safe???}`
