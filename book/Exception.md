# 异常记录
#### 1.文件名、目录名或卷标语不正确
DeBug: 因为IE上传文件的时候，后台（以下都表示C#）通过IFormFile files.FileName 获取到的是完整路径。<br />
如：D:\ConsignAPI\Content\File\（后面是FileName获取的）C:\Users\yingchunchen\Desktop\test.pdf <br />
这会导致后面处理文件时，路径是不合法的，产生异常。
     
