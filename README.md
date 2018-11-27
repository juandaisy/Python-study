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

      
   
