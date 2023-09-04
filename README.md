# Calculation-of-billiard-angle


if you dont speak chinese , you can translate download page's content with chatgpt.

also i will explain the meaning of the talbe of the below link.

the line of the table means  the arc between the two lines . first line is the  link line of the white ball center and the object ball center. the second line is the object ball center and the goal Billiards hole center.

the column of the table means the distance of the two ball's center divided by the diamenter of the ball.

the center data means the arc that you should use . that is the arc between two line . first line is the  link line of the white ball center and the object ball center. the second line is club direction.

if you dont understand ,you can issue the pro.


台球角度计算. https://www.cnblogs.com/zhangbo2008/p/17675783.html



```
# https://www.cnblogs.com/zhangbo2008/p/17675783.html



#=============下面我们用代码来把那里面的公式进行表格化.


#========2个变量. 一个theta是白球距离黑球距离是直径的多少倍
#================一个参数是白球射击到球袋跟直线击打的偏移角.
import math
theta=1
jiaodu=2
hudu=jiaodu/180*math.pi
gognshi=math.atan(math.sin(hudu)/(theta-math.cos(hudu)))

import pandas as pd

import pandas as pd
import numpy as np
dates = pd.date_range('20200315', periods = 5)
hang= list(range(1,90))  # theta
lie=np.arange(1.2,10,0.2)           #   90*90ge

#=======先把数据算完吧.


print(1111111111111111111111)
import math
x = math.sin(90)
print(x)

dataall=[]
for i in hang: #######=======jiaodu是行
    for j in lie: #  lie是距离.

            theta=j
            jiaodu=i
            hudu=math.radians(jiaodu) 
            gognshi=math.atan(math.sin(hudu)/(theta-math.cos(hudu)))
            gognshi=gognshi/math.pi*180
            gognshi=round(gognshi,2)
            dataall.append(gognshi)
dataall=np.array(dataall).reshape(len(hang),-1)
print(1)


aaa=pd.DataFrame(dataall, index = hang, columns = lie)


# for row_index, row in aaa.iterrows():
#     print(row_index,row)


print(1)
print(aaa.head())

aaa.to_excel('台球偏移角.xlsx',sheet_name='台球偏移角')


# theta=2
# jiaodu=30
# hudu=math.radians(jiaodu) 
# gognshi=math.atan(math.sin(hudu)/(theta-math.cos(hudu)))
# gognshi=gognshi/math.pi*180
# print(gognshi)
```
