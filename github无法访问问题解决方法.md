# github无法访问问题解决方法

问题描述:

直接使用gtihub.com网址访问github浏览器无响应。

解决办法：

1、登录https://github.com.ipaddress.com/去查询github.com、github.global.ssl.fastly.net对应的IP地址；

2、在网站的Domain Summary下查询到Github的IP地址；

&#x20;![](<.gitbook/assets/image (2).png>)

3、直接在浏览器中输入IP地址访问Github，网页正常响应。

4、编辑C:\Windows\System32\drivers\etc下的hosts文件，将github的IP地址保持到hosts文件。

&#x20;![](<.gitbook/assets/image (4).png>)

5、如果遇到无法保存hosts文件的问题，由于hosts文件权限导致，可以右键点击hosts文件，选择“属性”->“安全”->给user用户勾选写入权限。

![](<.gitbook/assets/image (5).png>)

&#x20;

&#x20;6、在cmd中运行ipconfig /flushdns ，刷新dns，此时浏览器中直接输入github.com即可成功访问。
