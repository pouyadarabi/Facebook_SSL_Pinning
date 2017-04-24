# Facebook_SSL_Pinning
Bypassing Facebook SSL pinning for version 120.0.0.18.72 | Min API 15 | April 18, 2017


#### libcoldstart.so

Replace the libcoldstart.so file in **/data/data/com.facebook.katana/lib-xzs**



## Steps:



We need to patch **0x001EB138** and **0x001EB13A**:

![before_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/before.jpg)


After patching these offsets to **0xB9D9** and **0xB9D6**, patched lib should be like this:


![after_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/after.jpg)

---

![Burp](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/burp.png)

---



[Patched lib file](https://github.com/pouyadarabi/Facebook_SSL_Pinning/blob/master/libcoldstart.so)

[Refrence](https://serializethoughts.com/2016/08/18/bypassing-ssl-pinning-in-android-applications/)

