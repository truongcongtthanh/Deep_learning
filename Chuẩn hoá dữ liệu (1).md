# Chuẩn hoá dữ liệu
## 1. Dữ liệu cơ bản
![](https://i.imgur.com/UE3UQzo.png)

=> Làm cho species thành dạng số được phân loại

``` python=
# aivietnam.ai
# Đọc file IRIS.csv
import numpy as np
import numpy.core.defchararray as np_f
# lấy các đặc trưng và lưu vào biến X
X = np.genfromtxt('IRIS.csv', delimiter=',', dtype='float', usecols=[0,1,2,3], skip_header=1)
print(X.shape)
# lấy species và lưu vào biến y
y = np.genfromtxt('IRIS.csv', delimiter=',', dtype='str', usecols=4, skip_header=1)
# thay chuỗi bằng số
categories = np.unique(y)
for i in range(categories.size):
    y = np_f.replace(y, categories[i], str(i))    
# đưa về kiểu float    
y = y.astype('float')
print(y)
```

- Ở đoạn code trên:
    - dữ liệu số cần dùng được đưa vào X
    - Dữ liệu nhãn phân loại được chuẩn hoá về dạng số
    
- Ta có kết quả trả về như sau:
![](https://i.imgur.com/O1hqEp0.png)

- Download data = code, 
    - tuple(0): link cần down
    - tuple(1): nơi cần để lưu
![](https://i.imgur.com/SbrdUlY.png)

