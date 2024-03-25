---
title: "SP500 Multiples"
description: "Historical S&P 500 multiples and Shiller PE ratios"
---

<!-- markdownlint-disable MD012 MD031 MD033 -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

---

## Implementation details

### Class names

| Model name | Parameters class | Data class |
| ---------- | ---------------- | ---------- |
| `SP500Multiples` | `SP500MultiplesQueryParams` | `SP500MultiplesData` |

### Import Statement

```python
from openbb_core.provider.standard_models.sp500_multiples import (
SP500MultiplesData,
SP500MultiplesQueryParams,
)
```

---

## Parameters

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| series_name | Literal['shiller_pe_month', 'shiller_pe_year', 'pe_year', 'pe_month', 'dividend_year', 'dividend_month', 'dividend_growth_quarter', 'dividend_growth_year', 'dividend_yield_year', 'dividend_yield_month', 'earnings_year', 'earnings_month', 'earnings_growth_year', 'earnings_growth_quarter', 'real_earnings_growth_year', 'real_earnings_growth_quarter', 'earnings_yield_year', 'earnings_yield_month', 'real_price_year', 'real_price_month', 'inflation_adjusted_price_year', 'inflation_adjusted_price_month', 'sales_year', 'sales_quarter', 'sales_growth_year', 'sales_growth_quarter', 'real_sales_year', 'real_sales_quarter', 'real_sales_growth_year', 'real_sales_growth_quarter', 'price_to_sales_year', 'price_to_sales_quarter', 'price_to_book_value_year', 'price_to_book_value_quarter', 'book_value_year', 'book_value_quarter'] | The name of the series. Defaults to 'pe_month'. | pe_month | True |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| transform | Literal['diff', 'rdiff', 'cumul', 'normalize'] | Transform the data as difference, percent change, cumulative, or normalize. | None | True |
| collapse | Literal['daily', 'weekly', 'monthly', 'quarterly', 'annual'] | Collapse the frequency of the time series. | None | True |
| provider | Literal['nasdaq'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'nasdaq' if there is no default. | nasdaq | True |
</TabItem>

<TabItem value='nasdaq' label='nasdaq'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| series_name | Literal['shiller_pe_month', 'shiller_pe_year', 'pe_year', 'pe_month', 'dividend_year', 'dividend_month', 'dividend_growth_quarter', 'dividend_growth_year', 'dividend_yield_year', 'dividend_yield_month', 'earnings_year', 'earnings_month', 'earnings_growth_year', 'earnings_growth_quarter', 'real_earnings_growth_year', 'real_earnings_growth_quarter', 'earnings_yield_year', 'earnings_yield_month', 'real_price_year', 'real_price_month', 'inflation_adjusted_price_year', 'inflation_adjusted_price_month', 'sales_year', 'sales_quarter', 'sales_growth_year', 'sales_growth_quarter', 'real_sales_year', 'real_sales_quarter', 'real_sales_growth_year', 'real_sales_growth_quarter', 'price_to_sales_year', 'price_to_sales_quarter', 'price_to_book_value_year', 'price_to_book_value_quarter', 'book_value_year', 'book_value_quarter'] | The name of the series. Defaults to 'pe_month'. | pe_month | True |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| transform | Literal['diff', 'rdiff', 'cumul', 'normalize'] | Transform the data as difference, percent change, cumulative, or normalize. | None | True |
| collapse | Literal['daily', 'weekly', 'monthly', 'quarterly', 'annual'] | Collapse the frequency of the time series. | None | True |
| provider | Literal['nasdaq'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'nasdaq' if there is no default. | nasdaq | True |
</TabItem>

</Tabs>

---

## Data

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | date | The date of the data. |
</TabItem>

<TabItem value='nasdaq' label='nasdaq'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | date | The date of the data. |
</TabItem>

</Tabs>
