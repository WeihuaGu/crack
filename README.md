# crack
自己的破解脚本(破阵)

## zipcrack目录
#### zip 密码暴力破解
使用伪线程（通过&把前台命令改成后台）加快跑字典

注意：

1.使用7z命令检验zip文件，所以你要先安装p7zip-full,之所以不用unzip是因为可能会遇到讨厌的`need PK compat. v5.1 (can do v4.6)` 

ubuntu安装p7zip-full

`sudo apt-get install p7zip-full`


2.zippo依赖于同目录下的zipcrack。使用zippo必须将zipcrack放在同一目录。zippo可以处理较大的字典，而zipcrack只能跑很小的字典。

用法:
 
    sh zippo <zip文件名> <密码字典> <分割密码字典的行数>
    sh zipcrack <zip文件名> <小型密码字典（最好不超过1000行)>

例如：
    sh zippo test.zip dic 100000
    
判断是否破解成功：

    zippo如果失败，退出码为-1,并且显示pass not found
    
    zippo如果成功，echo $? 退出码为0,并会把密码写入 zip文件名.pass文件中。例如例子中是test.zip,则成功后密码写入test.zip.pass文件。
    
## passwddic目录
这个目录用来存储收集到的用来破解的字典
#### wifiweak.txt(破解wifi的弱密码字典)

###对于zip等猜测比较简单的密码，推荐使用crunch命令生成字典
ubuntu安装crunch sudo apt-get install crunch

生成4位纯数字字典 `crunch 4 4 0123456789 -o num4.txt`

生成6位数字加特定字母字典（a,b,c,d,e,f) `crunch 6 6 0123456789abcdef -o numabcdef6.txt`
