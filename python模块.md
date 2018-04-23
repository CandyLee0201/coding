### Python模块总结  
#### 时间处理  
##### 概述  
1.在python中，通常用以下几种方式来表示时间：  
① 时间戳  
② 格式化的时间字符串  
③ 元组（struct_time）  
2.UTC（Coordinate Universal Time）世界协调时  
DST（Daylight Saving Time）夏令时  
3.时间戳的方式：时间戳表示的是从1970年1月1日的00:00:00开始按秒计算的偏移量。  
4.元组（struct_time）方式：struct_time元组共有九个元素，分别是年、月、日、时、分、秒、周、一年中的第几天、是否是夏令时。  
##### time
time.localtime([secs])  
将一个时间戳转换为当前时区的strut_time；若不提供secs参数，则以当前时间为准；  
time.gmtime()  
和localtime()方法类似，将一个时间戳转换为UTC时区的struct_time  
time.time()  
返回当前时间的时间戳  
time.mktime(t)  
将一个struct_time转化为时间戳  
time.sleep(secs)  
线程推迟指定的时间运行，单位为秒  
time.clock()  
在不同的系统上，含义不同；在UNIX系统上，它返回的是“进程时间”，用秒表示的浮点数---时间戳；在Windows中，第一次调用，返回的是进程运行的实际时间，第二次之后的调用是自第一次调用以后到现在的运行时间。  
time.asctime([t])  
把一个表示时间的元组或者struct_time表示为Sun June 20 23:21:05 2018；如果没有参数，将会将time.localtime()作为参数传入  
time.ctime([secs])  
把一个时间戳转化为time.asctime()的形式；如果参数未给的时候，会默认time.time()为参数；作用同time.asctime(time.localtime(secs))  
time.strftime(format[,t])  
把一个代表时间的元组或者struct_time转化为格式化的时间字符串；如果t未指定，将传入time.localtime()。  
time.strptime(string[,string])  
##### date  

##### datetime  
datetime是用于date和time的模块的合集，datetime的两个常量是MAXYEAR和MINYEAR，分别是9999和1。  
datetime.time  
表示日期的类，有三个参数，datetime.date(year,month,day)，返回值为year-month-day；  

#### 文件名及文件路径  
##### os  
os模块为我们提供了文件操作的各类函数。  
os.getcwd()  
获得当前路径；  
os.listdir()  
获得当前文件夹下的所有文件和文件夹；  
os.removedir()  
删除单个目录和多个目录；  
os.path.isfile/isdir()  
检查是否是文件/文件夹；  
os.path.exits()  
检查文件路径是否存在；  
os.path.split()  
分离文件名/扩展名；  
os.path.dirname()  
获得文件路径；  
os.path.basename()  
获得文件名；  
os.path.join()  
把两个路径拼接成一个时，可用此方法
os.walk('路径')  
os.walk输入一个路径名称，以yield的方式返回一个三元组：dirpath、dirnames、filenames；  
dirpath：为目录的路径，是一个字符串；  
dirnames：列出了目录路径下的所有存在的目录的名称；  
filenames：列出了目录路径下的所有文件的名称  
##### 文件读写(I/O)  
在磁盘上读写文件的功能都是由操作系统提供的，现代的操作系统不允许普通的程序直接操作磁盘，所以读写文件就是请求操作系统打开一个文件对象（通常称之为文件描述符），然后通过操作系统提供的接口从这个文件对象中读取数据(读文件)，或者把数据写入这个文件对象(写文件)。  
###### 读文件  
要以读文件的模式打开一个文件对象，使用Python内置的open()函数，传入文件名和标示符；  
如果文件打开成功，接下来调用read()方法可以一次读取文件的全部内容，Python把内容读到内存，用str对象标示；  
最后一步调用用close()方法关闭文件  
###### 写文件  
在打开文件时，模式选为wb即可  
##### JSON  
如果我们要在不同的编程语言之间传递对象，就必须把对象序列化为标准格式。最好的格式是JSON。  
Python内置的json模块提供了非常完善的Python对象到JSON格式的转换。  
json.dump()  
可以直接把JSON写入一个file-like object，该方法返回一个字符串；  
json.load()  
将JSON反序列化为Python对象。


