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
print(model.predict([[9183]]))
```
