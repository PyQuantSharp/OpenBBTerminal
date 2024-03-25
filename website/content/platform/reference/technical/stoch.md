---
title: "stoch"
description: "Learn about the Stochastic Oscillator and its calculation. Understand  the parameters, returns, and see examples of how to use it with OpenBB. Improve  your page's SEO with this well-researched content."
keywords:
- stochastic oscillator
- close
- trading range
- '%D values'
- overbought condition
- oversold condition
- buy signal
- sell signal
- raw %K
- crossover signals
- parameters
- data
- index
- fast %K period
- slow %D period
- slow %K period
- returns
- stochastic oscillator data
- examples
- openbb
- equity
- price
- historical
- symbol
- start date
- provider
- stock data
- stoch data
- well-researched
- improve page's SEO
---

import HeadTitle from '@site/src/components/General/HeadTitle.tsx';

<HeadTitle title="technical/stoch - Reference | OpenBB Platform Docs" />

<!-- markdownlint-disable MD012 MD031 MD033 -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

Calculate the Stochastic Oscillator.

 The Stochastic Oscillator measures where the close is in relation
 to the recent trading range. The values range from zero to 100. %D values over 75
 indicate an overbought condition; values under 25 indicate an oversold condition.
 When the Fast %D crosses above the Slow %D, it is a buy signal; when it crosses
 below, it is a sell signal. The Raw %K is generally considered too erratic to use
 for crossover signals.


Examples
--------

```python
from openbb import obb
# Get the Stochastic Oscillator.
stock_data = obb.equity.price.historical(symbol='TSLA', start_date='2023-01-01', provider='fmp')
stoch_data = obb.technical.stoch(data=stock_data.results, fast_k_period=14, slow_d_period=3, slow_k_period=3)
```

---

## Parameters

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| data | List[Data] | The data to use for the Stochastic Oscillator calculation. |  | False |
| index | str, optional | Index column name to use with `data`, by default "date". |  | False |
| fast_k_period | NonNegativeInt, optional | The fast %K period, by default 14. |  | False |
| slow_d_period | NonNegativeInt, optional | The slow %D period, by default 3. |  | False |
| slow_k_period | NonNegativeInt, optional | The slow %K period, by default 3. |  | False |
</TabItem>

</Tabs>

---

## Returns

```python wordwrap
OBBject
    results : List[Data]
        The Stochastic Oscillator data.
```
