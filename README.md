# Python-27-
Python学习笔记(27)
# p86 字符串的编码与解码
s='天涯共此时'
#编码
print(s.encode(encoding='GBK'))  #在GBk这种编码格式中，一个汉字占两个字节
print(s.encode(encoding='UTF-8'))  #在UTF-8编码格式中，一个汉字3个字节

#解码
#byte代表的就是一个二进制数据(字节类型的数据)
byte=s.encode(encoding='GBK')  #编码
print(byte.decode(encoding='UTF-8'))  #解码这里会爆警告 用什么编码方式就用什么解码方式

byte=s.encode(encoding='UTF-8')
print(byte.decode(encoding='UTF-8')



# p87 函数的定义和调用
def calc(a,b):
    c=a+b
    return c

result=calc(10,20)
print(result)



# p88 函数调用的参数传递_位置实参_关键字实参
def calc(a,b):  #a,b称为形参，形参的位置是在函数的定义处
    c=a+b
    return c

result=calc(10,20)  #10，20称为实参，实参的位置是函数的调用处
print(result)
#第一个值给第一个...这种按位置来的是位置实参

res=calc(b=10,a=20)  #  =左侧的名称称为关键字参数
print(res)
#这种是关键字传参,传的值不按位置，按关键字
