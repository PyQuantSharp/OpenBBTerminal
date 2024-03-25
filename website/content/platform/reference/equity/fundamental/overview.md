---
title: "overview"
description: "Learn about the company overview and get essential information, including  symbol, price, beta, volume average, market capitalization, last dividend, industry,  website, CEO, sector, country, and more."
keywords:
- company overview
- overview symbol
- equity fundamental overview
- parameters
- returns
- data
- symbol
- price
- beta
- vol_avg
- mkt_cap
- last_div
- range
- changes
- company_name
- currency
- cik
- isin
- cusip
- exchange
- exchange_short_name
- industry
- website
- description
- ceo
- sector
- country
- full_time_employees
- phone
- address
- city
- state
- zip
- dcf_diff
- dcf
- image
- ipo_date
- default_image
- is_etf
- is_actively_trading
- is_adr
- is_fund
---

import HeadTitle from '@site/src/components/General/HeadTitle.tsx';

<HeadTitle title="equity/fundamental/overview - Reference | OpenBB Platform Docs" />

:::caution Deprecated
This endpoint is deprecated; use `/equity/profile` instead. Deprecated in OpenBB Platform V4.1 to be removed in V4.3.
:::

<!-- markdownlint-disable MD012 MD031 MD033 -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

Get company general business and stock data for a given company.


Examples
--------

```python
from openbb import obb
obb.equity.fundamental.overview(symbol='AAPL', provider='fmp')
```

---

## Parameters

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| symbol | str | Symbol to get data for. |  | False |
| provider | Literal['fmp'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fmp' if there is no default. | fmp | True |
</TabItem>

<TabItem value='fmp' label='fmp'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| symbol | str | Symbol to get data for. |  | False |
| provider | Literal['fmp'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fmp' if there is no default. | fmp | True |
</TabItem>

</Tabs>

---

## Returns

```python wordwrap
OBBject
    results : CompanyOverview
        Serializable results.
    provider : Literal['fmp']
        Provider name.
    warnings : Optional[List[Warning_]]
        List of warnings.
    chart : Optional[Chart]
        Chart object.
    extra : Dict[str, Any]
        Extra info.

```

---

## Data

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| symbol | str | Symbol representing the entity requested in the data. |
| price | float | Price of the company. |
| beta | float | Beta of the company. |
| vol_avg | int | Volume average of the company. |
| mkt_cap | int | Market capitalization of the company. |
| last_div | float | Last dividend of the company. |
| range | str | Range of the company. |
| changes | float | Changes of the company. |
| company_name | str | Company name of the company. |
| currency | str | Currency of the company. |
| cik | str | Central Index Key (CIK) for the requested entity. |
| isin | str | ISIN of the company. |
| cusip | str | CUSIP of the company. |
| exchange | str | Exchange of the company. |
| exchange_short_name | str | Exchange short name of the company. |
| industry | str | Industry of the company. |
| website | str | Website of the company. |
| description | str | Description of the company. |
| ceo | str | CEO of the company. |
| sector | str | Sector of the company. |
| country | str | Country of the company. |
| full_time_employees | str | Full time employees of the company. |
| phone | str | Phone of the company. |
| address | str | Address of the company. |
| city | str | City of the company. |
| state | str | State of the company. |
| zip | str | Zip of the company. |
| dcf_diff | float | Discounted cash flow difference of the company. |
| dcf | float | Discounted cash flow of the company. |
| image | str | Image of the company. |
| ipo_date | date | IPO date of the company. |
| default_image | bool | If the image is the default image. |
| is_etf | bool | If the company is an ETF. |
| is_actively_trading | bool | If the company is actively trading. |
| is_adr | bool | If the company is an ADR. |
| is_fund | bool | If the company is a fund. |
</TabItem>

<TabItem value='fmp' label='fmp'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| symbol | str | Symbol representing the entity requested in the data. |
| price | float | Price of the company. |
| beta | float | Beta of the company. |
| vol_avg | int | Volume average of the company. |
| mkt_cap | int | Market capitalization of the company. |
| last_div | float | Last dividend of the company. |
| range | str | Range of the company. |
| changes | float | Changes of the company. |
| company_name | str | Company name of the company. |
| currency | str | Currency of the company. |
| cik | str | Central Index Key (CIK) for the requested entity. |
| isin | str | ISIN of the company. |
| cusip | str | CUSIP of the company. |
| exchange | str | Exchange of the company. |
| exchange_short_name | str | Exchange short name of the company. |
| industry | str | Industry of the company. |
| website | str | Website of the company. |
| description | str | Description of the company. |
| ceo | str | CEO of the company. |
| sector | str | Sector of the company. |
| country | str | Country of the company. |
| full_time_employees | str | Full time employees of the company. |
| phone | str | Phone of the company. |
| address | str | Address of the company. |
| city | str | City of the company. |
| state | str | State of the company. |
| zip | str | Zip of the company. |
| dcf_diff | float | Discounted cash flow difference of the company. |
| dcf | float | Discounted cash flow of the company. |
| image | str | Image of the company. |
| ipo_date | date | IPO date of the company. |
| default_image | bool | If the image is the default image. |
| is_etf | bool | If the company is an ETF. |
| is_actively_trading | bool | If the company is actively trading. |
| is_adr | bool | If the company is an ADR. |
| is_fund | bool | If the company is a fund. |
</TabItem>

</Tabs>
