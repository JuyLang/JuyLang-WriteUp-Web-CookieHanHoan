> Sau nhiều đêm suy nghĩ về việc làm thế nào để bảo vệ mã nguồn. Cố gắng thoát khỏi ánh mắt soi mói của Mèo Yang Hồ.

> Gà chẹp miệng rồi nói: "Đã tới lúc phải cho nó phải thốt lên rằng! WTF!!!"



> http://chal4.web.letspentest.org/ 


* `Ctrl + U` phân tích 4 file `js`:

![image](https://user-images.githubusercontent.com/68783065/140503880-19feaef5-a724-4a84-ae0c-77e919e113a4.png)



  * File đầu tiên:

![image](https://user-images.githubusercontent.com/68783065/140504099-01a0f917-2702-45ac-b916-f553fc66a520.png)

   * `Decode JSFuck` trên https://enkhee-osiris.github.io/Decoder-JSFuck/ nhận được:

```js
function verifyUsername(username) {
    if (username != "cookiehanhoan") {
        return false
    }
    return true
}
```
  * lấy ra `username` `cookiehanhoan`

  * Tương tự với file thứ 2 lấy ra hàm `reverseString`:
  
```js
function reverseString(str) {
    if (str === "") {
        return ""
    } else {
        return reverseString(str.substr(1)) + str.charAt(0)
    }
}
```
  * File 3 lấy ra `password` `dr0Wss@p3rucreSr3pus`:

```js
function verifyPassword(password) {
    if (reverseString(password) != "dr0Wss@p3rucreSr3pus") {
        return false
    }
    return true
}
```

  * Đảo ngược chuỗi lại nhận được `password` là `sup3rSercur3p@ssW0rd`: `echo 'dr0Wss@p3rucreSr3pus' | rev`




![image](https://user-images.githubusercontent.com/68783065/140505823-2006798b-293c-4182-96f5-5c25701f1114.png)



  * File 4 lấy ra `role` `@dmiN`:


```js
function verifyRole(role) {
    if (role.charCodeAt(0) != 64) {
        return false;
    }
    if ((role.charCodeAt(1) + role.charCodeAt(2) != 209) && (role.charCodeAt(2) - role.charCodeAt(1) != 9)) {
        return false
    }
    if ((role.charCodeAt(3).toString() + role.charCodeAt(4).toString() != "10578") && (role.charCodeAt(3) - role.charCodeAt(4) != 27)) {
        return false
    }
    return true
}
```


* Nhập tất cả vào trang đăng nhập:



![image](https://user-images.githubusercontent.com/68783065/140506318-e9bf9fd5-8905-4f49-a031-2d80c20b9b32.png)


![image](https://user-images.githubusercontent.com/68783065/140506342-2b33c21d-7f68-4aa1-b621-cabfbe4b292e.png)


* Flag is: `Flag{JAV-ascript_F*ck}`





