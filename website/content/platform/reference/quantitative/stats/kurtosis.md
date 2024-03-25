---
title: "kurtosis"
description: "Calculate the rolling kurtosis of a target column"
keywords:
- quantitative
- stats
- kurtosis
---

import HeadTitle from '@site/src/components/General/HeadTitle.tsx';

<HeadTitle title="quantitative/stats/kurtosis - Reference | OpenBB Platform Docs" />

<!-- markdownlint-disable MD012 MD031 MD033 -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

Calculate the rolling kurtosis of a target column.

 Kurtosis measures the "tailedness" of the probability distribution of a real-valued random variable.
 High kurtosis indicates a distribution with heavy tails (outliers), suggesting a higher risk of extreme outcomes.
 Low kurtosis indicates a distribution with lighter tails (less outliers), suggesting less risk of extreme outcomes.
 This function helps in assessing the risk of outliers in financial returns or other time series data.


Examples
--------

```python
from openbb import obb
# Get Kurtosis.
stock_data = obb.equity.price.historical(symbol="TSLA", start_date="2023-01-01", provider="fmp").to_df()
returns = stock_data["close"].pct_change().dropna()
obb.quantitative.stats.kurtosis(data=returns, target="close")
obb.quantitative.stats.kurtosis(target='close', data=[{'date': '2023-01-02', 'close': 0.05}, {'date': '2023-01-03', 'close': 0.08}, {'date': '2023-01-04', 'close': 0.07}, {'date': '2023-01-05', 'close': 0.06}, {'date': '2023-01-06', 'close': 0.06}])
```

---

## Parameters

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| data | List[Data] | The time series data as a list of data points. |  | False |
| target | str | The name of the column for which to calculate kurtosis. |  | False |
</TabItem>

</Tabs>

---

## Returns

```python wordwrap
OBBject
    results : List[Data]
        An object containing the kurtosis value
```
