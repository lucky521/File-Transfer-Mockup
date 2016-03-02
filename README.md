# File-Transfer-Mockup
File Transfer on HTML



## 基础模型一

### 文件上传

前端`form`标签内加入`file`标签，发起POST请求。

HTTP报头会指明Content-Type，文件会加入到HTTP的`MIME Multipart Media Encapsulation`字段中。

后端cgi处理POST请求，将HTTP报文中的文件对象存储成文件。

### 文件下载

前端对文件url发起GET请求。

后端处理GET请求，将文件放在HTTP报文的Content-type标明文件类型，正文中返回给前端。