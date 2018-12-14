# Python-study
Python study notes
4种类型的数：整数、长整数、浮点数、复数

字符串：单引号‘’，双引号“”，三引号''' a'''
转义字符：'what'\s your name?'
自然字符串：给字符串加上前缀r或R， r"Hi ,how are you\n"
Unicode字符串:给字符串加上前缀u或U， u"This is a Unicode string."

控制流：if..else, if...elif..else, while , for...in (for i in range(1,5)); 
break:终止循环语句，如果你从for或while循环中 终止 ，任何对应的循环else块将不执行。
continue语句：被用来告诉Python跳过当前循环块中的剩余语句，然后 继续 进行下一轮循环。
return语句：用来从一个函数 返回 即跳出函数

文档字符串DocStrings:  __doc__
文档字符串的惯例是:
    一个多行字符串，它的首行以大写字母开始，句号结尾。
    第二行是空行，
    从第三行开始是详细的描述。

模块： 引用模块import sys;
from..import语句 from sys import argv

模块的__name__属性：if __name__ == '__main__':

dir()函数：使用内建的dir函数来列出模块定义的标识符。标识符有函数、类和变量。
当你为dir()提供一个模块名的时候，它返回模块定义的名称列表。如果不提供参数，它返回当 前模块中定义的名称列表。

数据结构：列表 list[] 
         元组 ('a','b')
         字典dict  d = {key1:value1, key2:value2}  
 
 
 元组中的定制可以是%s表示字符串或%d表示整数
 # Filename: print_tuple.py
age = 22 
name = 'Swaroop'
print '%s is %d years old' % (name, age) 
print 'Why is %s playing with that python?' % name 
（源文件：code/print_tuple.py）
输出
$ python print_tuple.py 
Swaroop is 22 years old
Why is Swaroop playing with that python? 
 
 软件开发过程：1，什么（what）-——分析
              2，如何（how）-——设计
              3，编写（do）-——实施
              4，测试（test）-——测试与调试
              5，使用（use）-——实施或开发
              6，维护（maintain）-——优化
         
__init__方法：__init__方法在类的一个对象被建立时，马上运行。这个方法可以用来对你的对象做一些你希 望的 初始化 。注意，这个名称的开始和结尾都是双下划线
没有专门调用__init__方法，只是在创建一个类的新实例的时候，把参数包 括在圆括号内跟在类名后面，从而传递给__init__方法
# Filename: class_init.py
class Person:   
      def __init__(self, name):        
           self.name = name    
      def sayHi(self):       
           print 'Hello, my name is', self.name
p = Person('Swaroop') 
p.sayHi()

存储器：pickle、json、shelve
      pickle:使用它你可以在一个文件中储存任何Python对象，之 后你又可以把它完整无缺地取出来。这被称为 持久地 储存对象。
              以二进制来操作，pickle.dump(a,f)
      json:列表和字典的自由组合形式；json数据需要双引号，不能用单引号；json写入文件不能显示中文；在将json对象转化为字符串时需用unicode来编码json中文。（json.dump(data,f,ensure__ascii=False)确保中文中文正常显示）
      json.dumps() #将json对象转化为文本字符串
      json.loads() #将文本字符串转化为json对象
      shelve ：支持多个数据的读写
      写文件 shelve.open('shelve_text')
             f["name"]=name
      读文件 shelve.open('shelve_text')
            print(f1.get();;name)
 #读写文件函数    
• close – 关闭文件。跟你编辑器的 文件->保存.. 一个意思。
• read – 读取文件内容。你可以把结果赋给一个变量。 
• readline – 读取文本文件中的一行。 
• truncate – 清空文件，请小心使用该命令。
• write(stuff) – 将stuff写入文件

# Python格式化字符 %s %d %f
原文：http://blog.csdn.net/huangfu77/article/details/54807835

格式 描述
%% 百分号标记 #就是输出一个%
%c 字符及其ASCII码
%s 字符串
%d 有符号整数(十进制)
%u 无符号整数(十进制)
%o 无符号整数(八进制)
%x 无符号整数(十六进制)
%X 无符号整数(十六进制大写字符)
%e 浮点数字(科学计数法)
%E 浮点数字(科学计数法，用E代替e)
%f 浮点数字(用小数点符号)
%g 浮点数字(根据值的大小采用%e或%f)
%G 浮点数字(类似于%g)
%p 指针(用十六进制打印值的内存地址)
%n 存储输出字符的数量放进参数列表的下一个变量中
        
%格式化符也可用于字典，可用%(name)引用字典中的元素进行格式化输出。
        
负号指时数字应该是左对齐的，“0”告诉Python用前导0填充数字，正号指时数字总是显示它的正负(+，-)符号，即使数字是正数也不例外。
        
可指定最小的字段宽度，如："%5d" % 2。也可用句点符指定附加的精度，如："%.3d" % 3。


   
