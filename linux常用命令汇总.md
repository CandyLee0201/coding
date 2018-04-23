## Linux命令大全  
### 第1章 文件管理  
#### 1.1 cat  
用于连接文件并打印到标准输出设备上。  
cat [-AbeEnstTuv] [--help] [--version] filename  
-n/--number：由1开始对所有输出的行数编号；  
-b/--number-nonblank：和-n类似，但是对于空白行不编号；  
-s/--squeeze-blank：当遇到有连续两行以上的空白行，就代换为一行空白行；  
-v/--show-nonprinting：使用 ^ 和M-符号，除了LFD和TAB之外；  
-E/e/--show-ends：在每行结束处显示$；  
-T/t/--show-tabs：将TAB字符显示为^ I；  
#### 1.2 chattr  
用于改变文件或目录属性。属性共有如下8种模式：  
a：让文件或目录仅供附加用途；  
b：不更新文件或目录的最后存取时间；  
c：将文件或目录压缩后存放；  
d：将文件或目录排除在倾倒操作之外；  
i：不得任意更动文件或目录；  
s：保密性删除文件或目录；  
S：即时更新文件或目录；  
u：预防意外删除；  
chattr [-RV] [-v<版本编号>] [+/-/=<属性>][文件或目录]  
-R：递归处理，将指定目录下的所有文件及子目录一并处理；  
-v：版本编号，设置文件或目录版本；  
-V：显示指令执行过程；  
-<属性>：指定文件或目录的该项属性
#### 1.3 chgrp  
用于变更文件或目录的所属群组。  
chgrp [-cfhRv][--help][--version][所属群组][文件或目录...]  
chgrp [-cfhRv][--help][--reference=<参考文件或目录>][--version][文件或目录...]  
-c/--changes：效果类似‘-v’参数，但仅回报更改的部分；  
-f/--quite/--slient：不显示错误信息；  
-h/--no-dereference：只对符号连接的文件作修改，而不更动其他任何相关文件；  
-R/--recursive：递归处理，将制定目录下的所有文件及子目录一并处理；  
-v/--verbose：显示指令执行过程；  
--help：在线帮助；  
--reference<参考文件或目录>：把制定文件或目录的所属群组全部设成和参考文件或目录的所属群组相同；  
--version：显示版本信息；  
#### 1.4 chmod  
chmod可以来控制文件如何被他人所调用。  
Linux/Unix的文件调用权限分为三级：文件拥有者、群组、其他。  
chmod [-cfvR][--help][--version] mode file...  



