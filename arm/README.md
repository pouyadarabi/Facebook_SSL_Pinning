# Facebook_SSL_Pinning
Bypassing Facebook SSL pinning for version 136.0.0.22.91 | Min API 15 | arm | August 8, 2017
[Download Link](http://www.apkmirror.com/apk/facebook-2/facebook/facebook-136-0-0-22-91-release/facebook-136-0-0-22-91-2-android-apk-download/)


#### libcoldstart.so

Replace the libcoldstart.so file in **/data/data/com.facebook.katana/lib-xzs**



## Steps:



We need to patch **0x0018C4D0** and **0x0018C4D2**:

![before_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/arm/before.jpg?123)


After patching these offsets to **0xB9D9** and **0xB9D6**, patched lib should be like this:


![after_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/arm/after.jpg?123)

---

![Burp](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/arm/burp.jpg?123)

---



[Patched lib file](https://github.com/pouyadarabi/Facebook_SSL_Pinning/blob/master/arm/libcoldstart.so)

[Refrence](https://serializethoughts.com/2016/08/18/bypassing-ssl-pinning-in-android-applications/)

