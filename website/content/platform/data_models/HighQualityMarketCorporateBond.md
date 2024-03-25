---
title: "High Quality Market Corporate Bond"
description: "High Quality Market Corporate Bond"
---

<!-- markdownlint-disable MD012 MD031 MD033 -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

---

## Implementation details

### Class names

| Model name | Parameters class | Data class |
| ---------- | ---------------- | ---------- |
| `HighQualityMarketCorporateBond` | `HighQualityMarketCorporateBondQueryParams` | `HighQualityMarketCorporateBondData` |

### Import Statement

```python
from openbb_core.provider.standard_models.hqm import (
HighQualityMarketCorporateBondData,
HighQualityMarketCorporateBondQueryParams,
)
```

---

## Parameters

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| date | Union[date, str] | A specific date to get data for. | None | True |
| yield_curve | Literal['spot', 'par'] | The yield curve type. | spot | True |
| provider | Literal['fred'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fred' if there is no default. | fred | True |
</TabItem>

<TabItem value='fred' label='fred'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| date | Union[date, str] | A specific date to get data for. | None | True |
| yield_curve | Literal['spot', 'par'] | The yield curve type. | spot | True |
| provider | Literal['fred'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fred' if there is no default. | fred | True |
</TabItem>

</Tabs>

---

## Data

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | date | The date of the data. |
| rate | float | HighQualityMarketCorporateBond Rate. |
| maturity | str | Maturity. |
| yield_curve | Literal['spot', 'par'] | The yield curve type. |
</TabItem>

<TabItem value='fred' label='fred'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | date | The date of the data. |
| rate | float | HighQualityMarketCorporateBond Rate. |
| maturity | str | Maturity. |
| yield_curve | Literal['spot', 'par'] | The yield curve type. |
| series_id | str | FRED series id. |
</TabItem>

</Tabs>
