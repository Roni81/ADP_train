## ADP_train<br/>
### 빅분기 예상문제 링크 <br/>

#### 데이터 전처리 100문제
https://www.datamanim.com/dataset/99_pandas/pandasMain.html </br>

## 01 Getting & Knowing Data
### Attention
롤 랭킹 데이터 : https://www.kaggle.com/datasnaek/league-of-legends </br>
DataUrl = ‘https://raw.githubusercontent.com/Datamanim/pandas/main/lol.csv’
```python
import pandas as pd
# import pandas module
```

### Question 1
데이터를 로드하라, 데이터는 \t를 기준으로 구분되어 있다
```python
DataUrl = 'https://raw.githubusercontent.com/Datamanim/pandas/main/lol.csv'
df = pd.read_csv(DataUrl,sep = '\t')   # \t로 나누어진 데이터
```
<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>gameId</th>
      <th>creationTime</th>
      <th>gameDuration</th>
      <th>seasonId</th>
      <th>winner</th>
      <th>firstBlood</th>
      <th>firstTower</th>
      <th>firstInhibitor</th>
      <th>firstBaron</th>
      <th>firstDragon</th>
      <th>...</th>
      <th>t2_towerKills</th>
      <th>t2_inhibitorKills</th>
      <th>t2_baronKills</th>
      <th>t2_dragonKills</th>
      <th>t2_riftHeraldKills</th>
      <th>t2_ban1</th>
      <th>t2_ban2</th>
      <th>t2_ban3</th>
      <th>t2_ban4</th>
      <th>t2_ban5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>3326086514</td>
      <td>1504279457970</td>
      <td>1949</td>
      <td>9</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>...</td>
      <td>5</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>114</td>
      <td>67</td>
      <td>43</td>
      <td>16</td>
      <td>51</td>
    </tr>
    <tr>
      <th>1</th>
      <td>3229566029</td>
      <td>1497848803862</td>
      <td>1851</td>
      <td>9</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>...</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>11</td>
      <td>67</td>
      <td>238</td>
      <td>51</td>
      <td>420</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3327363504</td>
      <td>1504360103310</td>
      <td>1493</td>
      <td>9</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>...</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>157</td>
      <td>238</td>
      <td>121</td>
      <td>57</td>
      <td>28</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3326856598</td>
      <td>1504348503996</td>
      <td>1758</td>
      <td>9</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>164</td>
      <td>18</td>
      <td>141</td>
      <td>40</td>
      <td>51</td>
    </tr>
    <tr>
      <th>4</th>
      <td>3330080762</td>
      <td>1504554410899</td>
      <td>2094</td>
      <td>9</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>...</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>86</td>
      <td>11</td>
      <td>201</td>
      <td>122</td>
      <td>18</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>51485</th>
      <td>3308904636</td>
      <td>1503076540231</td>
      <td>1944</td>
      <td>9</td>
      <td>2</td>
      <td>1</td>
      <td>2</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>...</td>
      <td>10</td>
      <td>2</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>55</td>
      <td>-1</td>
      <td>90</td>
      <td>238</td>
      <td>157</td>
    </tr>
    <tr>
      <th>51486</th>
      <td>3215685759</td>
      <td>1496957179355</td>
      <td>3304</td>
      <td>9</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>...</td>
      <td>11</td>
      <td>7</td>
      <td>4</td>
      <td>4</td>
      <td>1</td>
      <td>157</td>
      <td>55</td>
      <td>119</td>
      <td>154</td>
      <td>105</td>
    </tr>
    <tr>
      <th>51487</th>
      <td>3322765040</td>
      <td>1504029863961</td>
      <td>2156</td>
      <td>9</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>0</td>
      <td>1</td>
      <td>...</td>
      <td>10</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>113</td>
      <td>122</td>
      <td>53</td>
      <td>11</td>
      <td>157</td>
    </tr>
    <tr>
      <th>51488</th>
      <td>3256675373</td>
      <td>1499562036246</td>
      <td>1475</td>
      <td>9</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>...</td>
      <td>11</td>
      <td>3</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>154</td>
      <td>39</td>
      <td>51</td>
      <td>90</td>
      <td>114</td>
    </tr>
    <tr>
      <th>51489</th>
      <td>3317333020</td>
      <td>1503612754059</td>
      <td>1445</td>
      <td>9</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>...</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>11</td>
      <td>157</td>
      <td>141</td>
      <td>31</td>
      <td>18</td>
    </tr>
  </tbody>
</table>
<p>51490 rows × 61 columns</p>
</div>

### Question 2
데이터 상위 5개 행을 출력하라

```python
ans = df.head(5)  #상위 5개 행을 출력 
display(ans)
```
<div>

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>gameId</th>
      <th>creationTime</th>
      <th>gameDuration</th>
      <th>seasonId</th>
      <th>winner</th>
      <th>firstBlood</th>
      <th>firstTower</th>
      <th>firstInhibitor</th>
      <th>firstBaron</th>
      <th>firstDragon</th>
      <th>...</th>
      <th>t2_towerKills</th>
      <th>t2_inhibitorKills</th>
      <th>t2_baronKills</th>
      <th>t2_dragonKills</th>
      <th>t2_riftHeraldKills</th>
      <th>t2_ban1</th>
      <th>t2_ban2</th>
      <th>t2_ban3</th>
      <th>t2_ban4</th>
      <th>t2_ban5</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>3326086514</td>
      <td>1504279457970</td>
      <td>1949</td>
      <td>9</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>...</td>
      <td>5</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>114</td>
      <td>67</td>
      <td>43</td>
      <td>16</td>
      <td>51</td>
    </tr>
    <tr>
      <th>1</th>
      <td>3229566029</td>
      <td>1497848803862</td>
      <td>1851</td>
      <td>9</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>...</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>11</td>
      <td>67</td>
      <td>238</td>
      <td>51</td>
      <td>420</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3327363504</td>
      <td>1504360103310</td>
      <td>1493</td>
      <td>9</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>2</td>
      <td>...</td>
      <td>2</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>157</td>
      <td>238</td>
      <td>121</td>
      <td>57</td>
      <td>28</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3326856598</td>
      <td>1504348503996</td>
      <td>1758</td>
      <td>9</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>...</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>164</td>
      <td>18</td>
      <td>141</td>
      <td>40</td>
      <td>51</td>
    </tr>
    <tr>
      <th>4</th>
      <td>3330080762</td>
      <td>1504554410899</td>
      <td>2094</td>
      <td>9</td>
      <td>1</td>
      <td>2</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>...</td>
      <td>3</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>86</td>
      <td>11</td>
      <td>201</td>
      <td>122</td>
      <td>18</td>
    </tr>
  </tbody>
</table>
<p>5 rows × 61 columns</p>
</div>

### Question 3
데이터의 행과 열의 갯수를 파악하라

```python
print(df.shape)
print('행 :', df.shape[0])   # df.shape의 첫번째 숫자
print('열 :', df.shape[1])   # df.shape의 첫번째 숫자
```
(51490, 61)</br>
행 : 51490 </br>
열 : 61

### Question 4
전체 컬럼을 출력하라

```python
res = df.columns
res
```
Index(['gameId', 'creationTime', 'gameDuration', 'seasonId', 'winner',
       'firstBlood', 'firstTower', 'firstInhibitor', 'firstBaron',
       'firstDragon', 'firstRiftHerald', 't1_champ1id', 't1_champ1_sum1',
       't1_champ1_sum2', 't1_champ2id', 't1_champ2_sum1', 't1_champ2_sum2',
       't1_champ3id', 't1_champ3_sum1', 't1_champ3_sum2', 't1_champ4id',
       't1_champ4_sum1', 't1_champ4_sum2', 't1_champ5id', 't1_champ5_sum1',
       't1_champ5_sum2', 't1_towerKills', 't1_inhibitorKills', 't1_baronKills',
       't1_dragonKills', 't1_riftHeraldKills', 't1_ban1', 't1_ban2', 't1_ban3',
       't1_ban4', 't1_ban5', 't2_champ1id', 't2_champ1_sum1', 't2_champ1_sum2',
       't2_champ2id', 't2_champ2_sum1', 't2_champ2_sum2', 't2_champ3id',
       't2_champ3_sum1', 't2_champ3_sum2', 't2_champ4id', 't2_champ4_sum1',
       't2_champ4_sum2', 't2_champ5id', 't2_champ5_sum1', 't2_champ5_sum2',
       't2_towerKills', 't2_inhibitorKills', 't2_baronKills', 't2_dragonKills',
       't2_riftHeraldKills', 't2_ban1', 't2_ban2', 't2_ban3', 't2_ban4',
       't2_ban5'],
      dtype='object')

### Question 5
6번째 컬럼명을 출력하라

```python
res = df.columns[5]
res
```
'firstBlood'

### Question 6
6번째 컬럼의 데이터 타입을 확인하라
```python
res = df.iloc[:,5].dtypes
print(res)
```
### Question 7
데이터셋 인덱스의 구성은 어떤가?
```pyhton
res = df.index
print(res)
```
RangeIndex(start=0, stop=51490, step=1)








https://www.datamanim.com/dataset/03_dataq/typeone.html
