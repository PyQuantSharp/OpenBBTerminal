---
title: "World News"
description: "World News"
---

<!-- markdownlint-disable MD012 MD031 MD033 -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

---

## Implementation details

### Class names

| Model name | Parameters class | Data class |
| ---------- | ---------------- | ---------- |
| `WorldNews` | `WorldNewsQueryParams` | `WorldNewsData` |

### Import Statement

```python
from openbb_core.provider.standard_models.world_news import (
WorldNewsData,
WorldNewsQueryParams,
)
```

---

## Parameters

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| limit | int | The number of data entries to return. The number of articles to return. | 2500 | True |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | End date of the data, in YYYY-MM-DD format. | None | True |
| provider | Literal['benzinga', 'biztoc', 'fmp', 'intrinio', 'tiingo'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'benzinga' if there is no default. | benzinga | True |
</TabItem>

<TabItem value='benzinga' label='benzinga'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| limit | int | The number of data entries to return. The number of articles to return. | 2500 | True |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | End date of the data, in YYYY-MM-DD format. | None | True |
| provider | Literal['benzinga', 'biztoc', 'fmp', 'intrinio', 'tiingo'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'benzinga' if there is no default. | benzinga | True |
| date | Union[date, str] | A specific date to get data for. | None | True |
| display | Literal['headline', 'abstract', 'full'] | Specify headline only (headline), headline + teaser (abstract), or headline + full body (full). | full | True |
| updated_since | int | Number of seconds since the news was updated. | None | True |
| published_since | int | Number of seconds since the news was published. | None | True |
| sort | Literal['id', 'created', 'updated'] | Key to sort the news by. | created | True |
| order | Literal['asc', 'desc'] | Order to sort the news by. | desc | True |
| isin | str | The ISIN of the news to retrieve. | None | True |
| cusip | str | The CUSIP of the news to retrieve. | None | True |
| channels | str | Channels of the news to retrieve. | None | True |
| topics | str | Topics of the news to retrieve. | None | True |
| authors | str | Authors of the news to retrieve. | None | True |
| content_types | str | Content types of the news to retrieve. | None | True |
</TabItem>

<TabItem value='biztoc' label='biztoc'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| limit | int | The number of data entries to return. The number of articles to return. | 2500 | True |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | End date of the data, in YYYY-MM-DD format. | None | True |
| provider | Literal['benzinga', 'biztoc', 'fmp', 'intrinio', 'tiingo'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'benzinga' if there is no default. | benzinga | True |
| filter | Literal['crypto', 'hot', 'latest', 'main', 'media', 'source', 'tag'] | Filter by type of news. | latest | True |
| source | str | Filter by a specific publisher. Only valid when filter is set to source. | bloomberg | True |
| tag | str | Tag, topic, to filter articles by. Only valid when filter is set to tag. | None | True |
| term | str | Search term to filter articles by. This overrides all other filters. | None | True |
</TabItem>

<TabItem value='fmp' label='fmp'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| limit | int | The number of data entries to return. The number of articles to return. | 2500 | True |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | End date of the data, in YYYY-MM-DD format. | None | True |
| provider | Literal['benzinga', 'biztoc', 'fmp', 'intrinio', 'tiingo'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'benzinga' if there is no default. | benzinga | True |
</TabItem>

<TabItem value='intrinio' label='intrinio'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| limit | int | The number of data entries to return. The number of articles to return. | 2500 | True |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | End date of the data, in YYYY-MM-DD format. | None | True |
| provider | Literal['benzinga', 'biztoc', 'fmp', 'intrinio', 'tiingo'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'benzinga' if there is no default. | benzinga | True |
</TabItem>

<TabItem value='tiingo' label='tiingo'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| limit | int | The number of data entries to return. The number of articles to return. | 2500 | True |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | End date of the data, in YYYY-MM-DD format. | None | True |
| provider | Literal['benzinga', 'biztoc', 'fmp', 'intrinio', 'tiingo'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'benzinga' if there is no default. | benzinga | True |
| offset | int | Page offset, used in conjunction with limit. | 0 | True |
| source | str | A comma-separated list of the domains requested. | None | True |
</TabItem>

</Tabs>

---

## Data

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | datetime | The date of the data. The published date of the article. |
| title | str | Title of the article. |
| images | List[Dict[str, str]] | Images associated with the article. |
| text | str | Text/body of the article. |
| url | str | URL to the article. |
</TabItem>

<TabItem value='benzinga' label='benzinga'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | datetime | The date of the data. The published date of the article. |
| title | str | Title of the article. |
| images | List[Dict[str, str]] | Images associated with the article. |
| text | str | Text/body of the article. |
| url | str | URL to the article. |
| id | str | Article ID. |
| author | str | Author of the news. |
| teaser | str | Teaser of the news. |
| channels | str | Channels associated with the news. |
| stocks | str | Stocks associated with the news. |
| tags | str | Tags associated with the news. |
| updated | datetime | Updated date of the news. |
</TabItem>

<TabItem value='biztoc' label='biztoc'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | datetime | The date of the data. The published date of the article. |
| title | str | Title of the article. |
| images | List[Dict[str, str]] | Images associated with the article. |
| text | str | Text/body of the article. |
| url | str | URL to the article. |
| favicon | str | Icon image for the source of the article. |
| tags | List[str] | Tags for the article. |
| id | str | Unique Article ID. |
| score | float | Search relevance score for the article. |
</TabItem>

<TabItem value='fmp' label='fmp'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | datetime | The date of the data. The published date of the article. |
| title | str | Title of the article. |
| images | List[Dict[str, str]] | Images associated with the article. |
| text | str | Text/body of the article. |
| url | str | URL to the article. |
| site | str | News source. |
</TabItem>

<TabItem value='intrinio' label='intrinio'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | datetime | The date of the data. The published date of the article. |
| title | str | Title of the article. |
| images | List[Dict[str, str]] | Images associated with the article. |
| text | str | Text/body of the article. |
| url | str | URL to the article. |
| id | str | Article ID. |
| company | Dict[str, Any] | Company details related to the news article. |
</TabItem>

<TabItem value='tiingo' label='tiingo'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| date | datetime | The date of the data. The published date of the article. |
| title | str | Title of the article. |
| images | List[Dict[str, str]] | Images associated with the article. |
| text | str | Text/body of the article. |
| url | str | URL to the article. |
| symbols | str | Ticker tagged in the fetched news. |
| article_id | int | Unique ID of the news article. |
| site | str | News source. |
| tags | str | Tags associated with the news article. |
| crawl_date | datetime | Date the news article was crawled. |
</TabItem>

</Tabs>
