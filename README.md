## 빅데이터 분석기사 시험 준비
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

### importing Pandas library
```python
import pandas as pd
```



### 데이터 불러오기
```python
pd.read_csv(데이터 경로, sep = '\t', encoding=엔코더 이름)

```
parameter_URL : https://pandas.pydata.org/docs/reference/api/pandas.read_csv.html#pandas-read-csv

### 위쪽부터 n개 행을 출력하라 head 함수
```python
df.head(n)
# head 함수 사용 default값은 10
```
parameter_URL : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.head.html#pandas.DataFrame.head
### 데이터의 모양을 확인하자 shape
```python
df.shape
```
(51490, 61)</br>

parameter_URL : https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.shape.html#pandas.DataFrame.shape
