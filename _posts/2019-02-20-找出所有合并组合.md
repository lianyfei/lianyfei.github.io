## 找出列表中元素的所有组合

python3
macOS

### 思路
Python操作符：

	i << j 
	
	%
### 实现
```
def find_all_combinations(item_list):
	n = len(item_list)
	for i in range(2*n):
		rts = []
		for j in range(n):
		if (i << j) % 2:
			rts.append(item_list[j])
```
### main
```
find_all_combinations()
```
