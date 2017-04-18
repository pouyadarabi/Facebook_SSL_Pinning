# Facebook_SSL_Pinning
Bypassing Facebook SSL pinning for version 118.0.0.22.79 | Min API 15 | April 4, 2017


#### libcoldstart.so

Replace the libcoldstart.so file in **/data/data/com.facebook.orca/lib-xzs**



## Steps:



We need to patch **0x001DF870** and **0x001DF872**:

![before_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/before.jpg)


After patching these offsets to **0xB9D6** and **0xB9D9**, patched lib should be like this:


![after_patching](https://raw.githubusercontent.com/pouyadarabi/Facebook_SSL_Pinning/master/after.jpg)



---


[Patched source code](https://github.com/pouyadarabi/Facebook_SSL_Pinning/blob/master/libcoldstart.c)

[Patched lib file](https://github.com/pouyadarabi/Facebook_SSL_Pinning/blob/master/libcoldstart.so)

[Refrence](https://serializethoughts.com/2016/08/18/bypassing-ssl-pinning-in-android-applications/)

