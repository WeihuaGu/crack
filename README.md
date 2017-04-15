# crack
自己的破解脚本(破阵)

## zipcrack目录
#### zip 密码暴力破解
使用伪线程（通过&把前台命令改成后台）加快跑字典

注意：

1.使用7z命令检验zip文件，所以你要先安装7zip-full,之所以不用unzip是因为可能会遇到讨厌的`need PK compat. v5.1 (can do v4.6)` 

2.zippo依赖于同目录下的zipcrack。使用zippo必须将zipcrack放在同一目录。zippo可以处理较大的字典，而zipcrack只能跑很小的字典。

用法sh zippo <zip文件名> <密码字典> <分割密码字典的行数>

例如：
    sh zippo test.zip dic 100000


## passwddic目录
这个目录用来存储收集到的用来破解的字典
#### wifiweak.txt(破解wifi的弱密码字典)
