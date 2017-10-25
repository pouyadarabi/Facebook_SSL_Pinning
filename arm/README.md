# Facebook_SSL_Pinning
Bypassing Facebook SSL pinning for version 146.0.0.53.92 | Min API 15 | arm | October 22, 2017
[Download Link](https://www.apkmirror.com/apk/facebook-2/facebook/facebook-146-0-0-53-92-release/facebook-146-0-0-53-92-2-android-apk-download/)


#### libcoldstart.so

Replace the libcoldstart.so file in **/data/data/com.facebook.katana/lib-xzs**



## Steps:



We need to patch **0x00264BF8** and **0x00264BFA**:

![before_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/arm/before.jpg?1234)


After patching these offsets to **0xB1D9** and **0xB9D6**, patched lib should be like this:


![after_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/arm/after.jpg?1234)

---

![Burp](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/arm/burp.jpg?123)

---



[Patched lib file](https://github.com/pouyadarabi/Facebook_SSL_Pinning/blob/master/arm/libcoldstart.so)

[Refrence](https://serializethoughts.com/2016/08/18/bypassing-ssl-pinning-in-android-applications/)

