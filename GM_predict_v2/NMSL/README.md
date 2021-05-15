```python
import numpy as np

b = np.loadtxt(r"C:\Users\swn\Desktop\电影票房.csv", delimiter=",")
data = b[:,1]
x = data[:]

from GM import GM11
result = GM11.GM11(x,1)#预测结果,一阶差分偏自相关图,一阶差分自相关图
predict = result['predict']['value']
predict = np.round(predict,1)
#print('真实值:',y)
print('预测值:',predict)
#print(result) #打印result
#预测值为predict
```