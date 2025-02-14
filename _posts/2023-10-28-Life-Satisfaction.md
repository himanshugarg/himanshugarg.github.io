---
categories: learning 
---

Thanks to Aurelien Geron, I figured, the reason for my life satisfaction or the lack of it. 

```python
import pandas as pd
from sklearn.linear_model import LinearRegression

# pull the data
data_root = "https://github.com/ageron/data/raw/main/"
lifesat = pd.read_csv(data_root + "lifesat/lifesat.csv")

# run your model
model = LinearRegression()
model.fit(lifesat[["GDP per capita (USD)"]].values, 
          lifesat[["Life satisfaction"]].values)
print(model.predict([[9183]])) # prints [[4.37155579]]
```

Here is the dataset, just so we know where we stand:
|index|Country|GDP per capita \(USD\)|Life satisfaction|
|---|---|---|---|
|0|Russia|26456\.3879381321|5\.8|
|1|Greece|27287\.0834009302|5\.4|
|2|Turkey|28384\.9877846263|5\.5|
|3|Latvia|29932\.4939100562|5\.9|
|4|Hungary|31007\.7684065437|5\.6|
|5|Portugal|32181\.1545372343|5\.4|
|6|Poland|32238\.157259275|6\.1|
|7|Estonia|35638\.4213511812|5\.7|
|8|Spain|36215\.4475907307|6\.3|
|9|Slovenia|36547\.7389559849|5\.9|
|10|Lithuania|36732\.034744031|5\.9|
|11|Israel|38341\.3075704083|7\.2|
|12|Italy|38992\.1483807498|6\.0|
|13|United Kingdom|41627\.129269425|6\.8|
|14|France|42025\.6173730617|6\.5|
|15|New Zealand|42404\.3937381567|7\.3|
|16|Canada|45856\.6256264804|7\.4|
|17|Finland|47260\.800458441|7\.6|
|18|Belgium|48210\.0331113444|6\.9|
|19|Australia|48697\.8370282475|7\.3|
|20|Sweden|50683\.3235097178|7\.3|
|21|Germany|50922\.3580234484|7\.0|
|22|Austria|51935\.6038618156|7\.1|
|23|Iceland|52279\.7288513646|7\.5|
|24|Netherlands|54209\.5638357302|7\.4|
|25|Denmark|55938\.2128086032|7\.6|
|26|United States|60235\.7284916969|6\.9|
