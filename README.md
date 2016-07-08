# Dow命令收集
### 1.查看命令所在的路径
where adb
### 2.给文件重命名
ren dir newName
#### 解释：dir为全路径，后面不能写路径，只能是新名字
#### 例子：ren  F:\test\\*.txt    *.png 把dir目录下的所有以.txt结尾的文件改扩展名为 .png

### 3.查看已签名的apk的签名信息
#### 例子：keytool -list -printcert -v -jarfile F:\打包\ceshi.apk

### 4.删除手机上文件
#### 例子 删除手机data/data/com.baidu
<pre>
<code>
adb shell             //切换到shell命令
su                    //切换到用户
cd data               //切换到data目录
chmod 777 data        //修改此data目录下面的data文件权限为rwb
cd data
chmod 777 com.baidu
rm -rR com.baidu      //删除文件夹
rm -f a.txt           //删除文件
</code>
<pre>
### 5.查看手机某个应用占用内存情况
<pre>
<code>
adb shell dumpsys meminfo packagename -d
</code>
<pre>
