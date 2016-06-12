# Dow命令收集
### 1.查看命令所在的路径
where adb
### 2.给文件重命名
ren dir newName
#### 解释：dir为全路径，后面不能写路径，只能是新名字
#### 例子：ren  F:\test\\*.txt    *.png 把dir目录下的所有以.txt结尾的文件改扩展名为 .png

### 3.查看已签名的apk的签名信息
#### 例子：keytool -list -printcert -v -jarfile F:\打包\ceshi.apk
