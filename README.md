# imagettftext

这是关于php GD库的应用，这个源码将使您可以自定义的打印一些内容在图片上

get表单：

image=本地图像（与imageurl不能同时出现），默认=white.png（./images/white.png），可选

imageurl=远程图像（与image不能同时出现）默认=，可选

r=&g=&b=颜色r,g,b，默认r=0&g=0&b=0（范围0-255），可选

size=字体大小，默认=30（根据版本决定单位），可选

i=字体倾斜的角度，默认=0，可选

x=&y=起始文字的x、y坐标，默认x=10y=40，可选

font=字体文件，默认=./fonts/arialuni.ttf（Unicode标准），可选

text=文本（强烈建议字符串先进行url(utf-8)编码再提交get表单），默认=（空白则等效直接输出背景图），可选


使用举例：

http://106.52.30.88/imagettftext/?text=%E8%BF%99%E6%98%AF%E4%B8%80%E6%9D%A1%E6%B5%8B%E8%AF%95%E6%96%87%E6%9C%AC&image=blackboard.jpeg&x=100&y=120&r=255&g=255&b=255&i=2&size=40&font=fonts/msyh.ttf

http://api.xiwangly.xyz/imagettftext/?text=%E8%BF%99%E6%98%AF%E4%B8%80%E6%9D%A1%E6%B5%8B%E8%AF%95%E6%96%87%E6%9C%AC&image=blackboard.jpeg&x=100&y=120&r=255&g=255&b=255&i=2&size=40&font=fonts/msyh.ttf

在QRSpeed中的应用举例：

白板 [\s\S]*(.*)[\s\S]*<br>
e:$URLEncoder %参数1%$<br>
绘制白板结果：【±img=http://106.52.30.88/img.php?url=http\%3A\%2F\%2F106.52.30.88\%2Fimagettftext\%2F\%3Ftext\%3D%e%±】

下载后最好把文件夹.\*-master（其它分支同理）重命名为.\*，并且推荐解析到该文件夹，或者直接把下载后文件夹内的文件（选择性）拖放到wwwroot（一般指网站根目录）
