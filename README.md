# debug
1. 我爱你
- 第一
- 第二
## 代码引用
、
import random as r
class Fish:
    def __init__(self):
        self.x = r.randint(0,10)
        self.y = r.randint(0,10)
    def move(self):
        self.x -=1
        print('我的位置是：',self.x,self.y)

class Goldfish(Fish):
    pass
class Carp(Fish):
    pass
class Salmon(Fish):
    pass
class Shark(Fish):
    def __init__(self):  #此处重新写了def，所以不能运行shark.move()
        #如果要运行shark.move()有两种方法：
        #1。为绑定的父类方法(self为子类的)
        Fish.__init__(self)
        #2.super函数     优点：不用参数
        #super().__init__()
        self.hungry = True
        
    def eat(self):
        if self.hungry:
            print('吃货的梦想是天天有的吃^_^')
            self.hungry = False
        else:
            print("太撑了吃不下了^_^")
        
、
