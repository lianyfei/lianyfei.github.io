## Python-numpy常见操作

python3

### 操作
Python-numpy常见操作：

数据的保存；

载入；

获取坐标的元素；

转换形状；

其他
### 实现
```
import numpy as np
import os


class MatrixToolsObject(object):

	def __init__(self,data, sep=","):
		self.data = data
		self.sep = sep
		
		
	def save(self,save_path):
		if not os.path.exits(save_path):
			os.mkdir(save_path)
		np.savetxt(save_path, self.data, self.sep)
		
	def read(self,read_path):
		# 断言路径是否存在
		self.data = np.loadtxt(read_path, self.sep)
	
	def get(self, row, col):
		row_dim, col_dim = self.data.shape
		# 断言是否越界
		return self.data[row, col]
		
	def transpose(self,):
		# 断言是否None
		self.data = self.data.transpose()
		
```
### main
```
# 声明
matrix_data = np.arange(20).reshape(4,5)
tools_object = MatrixToolsObject(matrix_data) 

# 保存
tools_object.save("path")

# 读取
tools_object.read("path")

# 获取
tools_object.get(1,1)

# 转换
tools_object.transpose()
```
