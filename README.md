# AIDL_Demo
首先AIDL传对象<br>
1.创建bean，实现Parcelable<br>
2.app/main/aidl相同目录下创建同名aidl文件<br>
例如：<br>
package com.zyh.aidl;<br>
//下面这段很重要<br>
parcelable Person;<br>
//interface Person {<br>
//<br>
//}<br>
<br>
Process 'command 'D:\Studio\SDK\build-tools\27.0.3\aidl.exe'' finished with non-zero exit value 1<br>
出现此错误是由于AIDL自定义方法参数是（序列化）对象。<br>
检查<br>
1.（序列化）对象的包是否相同（app/main/aidl下与app/main/自定义目录）<br>
2.aidl文件导包路径是否正确
