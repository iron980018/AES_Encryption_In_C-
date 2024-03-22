# AES_Encryption

# 資訊安全課程實作

2024/3/20:
16字元內成功加解密

2024/3/21:
需加密訊息在32字元內目前能加解密
超過前面會有亂碼

2024/3/22:
加密訊息分段加密，解決只能加密<=32字元的訊息
加密金鑰前8字元必須跟後8字元一樣
不然會在InvMixColumns()時解密出與加密時不一樣的加密字串

2024/3/23:
修正加密金鑰前8字元必須跟後8字元一樣的問題
原因為解密時使用了錯誤的流程:  
![image](https://github.com/iron980018/AES_Encryption/blob/main/incorrect.jpg)  
正確的如下:  
![image](https://github.com/iron980018/AES_Encryption/blob/main/correct.png)  

此版本加密訊息是透過將原始訊息切割成每16字元進行一次加解密  
之後有時間或需求再去研究免切割和python版本
