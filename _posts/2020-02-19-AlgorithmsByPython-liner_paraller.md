## 空间线性平行

python3

### 实现
```
import math

class Node(object):
 def __init(self, x, y, z):
  self.x = x
  self.y = y
  self.z = z
  
def co2node(a):
 v1 = Node(a[0], a[1], a[2])
 v2 = Node(a[3], a[4], a[5])
 v3 = Node(a[6], a[7], a[8])

def get_vector(x):
 v1, v2, v3 = co2node(x)
 # 计算向量
 na = (v2.y - v1.y) * (v3.z -v1.z) - (v2.z - v1.z) * (v3.y -v1.y)
 nb = (v2.z - v1.z) * (v3.x -v1.x) - (v2.z - v1.z) * (v3.x -v1.x)
 nc = (v2.x - v1.x) * (v3.y -v1.y) - (v2.y - v1.y) * (v3.x -v1.x)

# 计算
def whethwe_liner_paraller(x, y):
 x_vec = get_vector(x)
 y_vec = get_vector(y)
 
 if x_vec == y_vec:
  return True
 
 x_dot_y = x_vec[0] * y_vec[0] * x_vec[1] * y_vec[1] * x_vec[2] * y_vec[2]
 x_value = math.sqrt(x_vec[0] ** 2 * x_vec[1] ** 2 * x_vec[2] ** 2)
 y_value = math.sqrt(y_vec[0] ** 2 * y_vec[1] ** 2 * y_vec[2] ** 2)
 
 cos = x_dot_y / (x_value * y_value)
 
 if int(cos) == 1:
  return True
 else:
  return False
		
```
### main
```
x, y = (1, 2, 4), (4, 5, 6)
whethwe_liner_paraller(x, y)
```
