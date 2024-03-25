---
title: "treasury_effr"
description: "This documentation page provides information about Treasury Bill data,  including the selected Treasury Bill rate minus Federal Funds Rate. It explains  the concept of constant maturity and the Treasury yield curve. The page also covers  the parameters, returns, and data associated with the `obb.fixedincome.spreads.treasury_effr`  function."
keywords:
- Treasury Bill
- Selected Treasury Bill
- Federal Funds Rate
- Constant Maturity
- Treasury yield curve
- bid-yields
- US Treasuries
- obb.fixedincome.spreads.treasury_effr
- start_date
- end_date
- maturity
- provider
- results
- warnings
- chart
- metadata
- rate
- data
---

import HeadTitle from '@site/src/components/General/HeadTitle.tsx';

<HeadTitle title="fixedincome/spreads/treasury_effr - Reference | OpenBB Platform Docs" />

<!-- markdownlint-disable MD012 MD031 MD033 -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

Select Treasury Bill.

Get Selected Treasury Bill Minus Federal Funds Rate.
Constant maturity is the theoretical value of a U.S. Treasury that is based on recent values of
auctioned U.S. Treasuries.
The value is obtained by the U.S. Treasury on a daily basis through interpolation of the Treasury
yield curve which, in turn, is based on closing bid-yields of actively-traded Treasury securities.


Examples
--------

```python
from openbb import obb
obb.fixedincome.spreads.treasury_effr(provider='fred')
obb.fixedincome.spreads.treasury_effr(maturity='6m', provider='fred')
```

---

## Parameters

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | End date of the data, in YYYY-MM-DD format. | None | True |
| maturity | Literal['3m', '6m'] | The maturity | 3m | True |
| provider | Literal['fred'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fred' if there is no default. | fred | True |
</TabItem>

<TabItem value='fred' label='fred'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | End date of the data, in YYYY-MM-DD format. | None | True |
| maturity | Literal['3m', '6m'] | The maturity | 3m | True |
| provider | Literal['fred'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fred' if there is no default. | fred | True |
</TabItem>

</Tabs>

---

## Returns

```python wordwrap
OBBject
    results : SelectedTreasuryBill
        Serializable results.
    provider : Literal['fred']
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
| date | date | The date of the data. |
| rate | float | SelectedTreasuryBill Rate. |
</TabItem>

<TabItem value='fred' label='fred'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | date | The date of the data. |
| rate | float | SelectedTreasuryBill Rate. |
</TabItem>

</Tabs>
