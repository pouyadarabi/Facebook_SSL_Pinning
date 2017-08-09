# Facebook_SSL_Pinning
Bypassing Facebook SSL pinning for version 136.0.0.22.91 | Min API 15 | x86 | August 8, 2017
[Download Link](http://www.apkmirror.com/apk/facebook-2/facebook/facebook-136-0-0-22-91-release/facebook-136-0-0-22-91-3-android-apk-download/)


#### libcoldstart.so

Replace the libcoldstart.so file in **/data/data/com.facebook.katana/lib-xzs**



## Steps:



We need to patch **0x003E5886** and **0x003E58B3**:

![before_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/x86/before.jpg?123)


After patching these offsets to **0x19EB** and **0x16EB**, patched lib should be like this:


![after_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/x86/after.jpg?123)

---

![Burp](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/x86/burp.jpg?123)

---



[Patched lib file](https://github.com/pouyadarabi/Facebook_SSL_Pinning/blob/master/x86/libcoldstart.so)

