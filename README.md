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

### 전체 컬럼을 출력하라
```python
df.columns
df.columns[n-1]   #n번째 컬럼의 데이터 타입을 확인하라
```
Index(['gameId', 'creationTime', 'gameDuration', 'seasonId', 'winner',
       'firstBlood', 'firstTower', 'firstInhibitor', 'firstBaron',
       'firstDragon', 'firstRiftHerald', 't1_champ1id', 't1_champ1_sum1'],
      dtype='object')
### 데이터셋의 인덱스를 출력하라
```python
df.index
```
RangeIndex(start=0, stop=51490, step=1)(시작 : 0, 끝 : 51490, 단계 = 1)

### 6번째 컬럼의 3번째 값은 무엇인가?
```python
df.iloc[2,5]  #df.iloc[row , column]
```

