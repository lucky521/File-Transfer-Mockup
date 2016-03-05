# File-Transfer-Mockup
File Transfer on HTML

File Transfer is a typical feature that could appears in kinds of scenario for web applications. HTTP is simple and practical, so we use it to transfer files intead of FTP. 

At front end, we need to pack file binary into HTTP packet with help of JS script and HTML FORM tag. At end front, we can use various methods and language to handle HTTP request. 



## 基础模型

### 文件上传

前端`form`标签内加入`file`标签，发起POST请求。

HTTP报头会指明Content-Type，文件会加入到HTTP的`MIME Multipart Media Encapsulation`字段中。

后端cgi处理POST请求，将HTTP报文中的文件对象存储成文件。

### 文件下载

前端对文件url发起GET请求。

后端处理GET请求，HTTP报文的Content-type标明文件类型，将文件体放在正文中返回给前端。
