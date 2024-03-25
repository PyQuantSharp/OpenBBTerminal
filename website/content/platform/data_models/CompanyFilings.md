---
title: "Company Filings"
description: "Get the URLs to SEC filings reported to EDGAR database, such as 10-K, 10-Q, 8-K, and more"
---

<!-- markdownlint-disable MD012 MD031 MD033 -->

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';

---

## Implementation details

### Class names

| Model name | Parameters class | Data class |
| ---------- | ---------------- | ---------- |
| `CompanyFilings` | `CompanyFilingsQueryParams` | `CompanyFilingsData` |

### Import Statement

```python
from openbb_core.provider.standard_models.company_filings import (
CompanyFilingsData,
CompanyFilingsQueryParams,
)
```

---

## Parameters

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| symbol | str | Symbol to get data for. | None | True |
| form_type | str | Filter by form type. Check the data provider for available types. | None | True |
| limit | int | The number of data entries to return. | 100 | True |
| provider | Literal['fmp', 'intrinio', 'sec', 'tmx'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fmp' if there is no default. | fmp | True |
</TabItem>

<TabItem value='fmp' label='fmp'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| symbol | str | Symbol to get data for. | None | True |
| form_type | str | Filter by form type. Check the data provider for available types. | None | True |
| limit | int | The number of data entries to return. | 100 | True |
| provider | Literal['fmp', 'intrinio', 'sec', 'tmx'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fmp' if there is no default. | fmp | True |
</TabItem>

<TabItem value='intrinio' label='intrinio'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| symbol | str | Symbol to get data for. | None | True |
| form_type | str | Filter by form type. Check the data provider for available types. | None | True |
| limit | int | The number of data entries to return. | 100 | True |
| provider | Literal['fmp', 'intrinio', 'sec', 'tmx'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fmp' if there is no default. | fmp | True |
| start_date | Union[date, str] | Start date of the data, in YYYY-MM-DD format. | None | True |
| end_date | Union[date, str] | End date of the data, in YYYY-MM-DD format. | None | True |
| thea_enabled | bool | Return filings that have been read by Intrinio's Thea NLP. | None | True |
</TabItem>

<TabItem value='sec' label='sec'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| symbol | str | Symbol to get data for. | None | True |
| form_type | str | Filter by form type. Check the data provider for available types. | None | True |
| limit | int | The number of data entries to return. | 100 | True |
| provider | Literal['fmp', 'intrinio', 'sec', 'tmx'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fmp' if there is no default. | fmp | True |
| cik | Union[int, str] | Lookup filings by Central Index Key (CIK) instead of by symbol. | None | True |
| type | Literal['1', '1-A', '1-A POS', '1-A-W', '1-E', '1-E AD', '1-K', '1-SA', '1-U', '1-Z', '1-Z-W', '10-12B', '10-12G', '10-D', '10-K', '10-KT', '10-Q', '10-QT', '11-K', '11-KT', '13F-HR', '13F-NT', '13FCONP', '144', '15-12B', '15-12G', '15-15D', '15F-12B', '15F-12G', '15F-15D', '18-12B', '18-K', '19B-4E', '2-A', '2-AF', '2-E', '20-F', '20FR12B', '20FR12G', '24F-2NT', '25', '25-NSE', '253G1', '253G2', '253G3', '253G4', '3', '305B2', '34-12H', '4', '40-17F1', '40-17F2', '40-17G', '40-17GCS', '40-202A', '40-203A', '40-206A', '40-24B2', '40-33', '40-6B', '40-8B25', '40-8F-2', '40-APP', '40-F', '40-OIP', '40FR12B', '40FR12G', '424A', '424B1', '424B2', '424B3', '424B4', '424B5', '424B7', '424B8', '424H', '425', '485APOS', '485BPOS', '485BXT', '486APOS', '486BPOS', '486BXT', '487', '497', '497AD', '497H2', '497J', '497K', '497VPI', '497VPU', '5', '6-K', '6B NTC', '6B ORDR', '8-A12B', '8-A12G', '8-K', '8-K12B', '8-K12G3', '8-K15D5', '8-M', '8F-2 NTC', '8F-2 ORDR', '9-M', 'ABS-15G', 'ABS-EE', 'ADN-MTL', 'ADV-E', 'ADV-H-C', 'ADV-H-T', 'ADV-NR', 'ANNLRPT', 'APP NTC', 'APP ORDR', 'APP WD', 'APP WDG', 'ARS', 'ATS-N', 'ATS-N-C', 'ATS-N/UA', 'AW', 'AW WD', 'C', 'C-AR', 'C-AR-W', 'C-TR', 'C-TR-W', 'C-U', 'C-U-W', 'C-W', 'CB', 'CERT', 'CERTARCA', 'CERTBATS', 'CERTCBO', 'CERTNAS', 'CERTNYS', 'CERTPAC', 'CFPORTAL', 'CFPORTAL-W', 'CORRESP', 'CT ORDER', 'D', 'DEF 14A', 'DEF 14C', 'DEFA14A', 'DEFA14C', 'DEFC14A', 'DEFC14C', 'DEFM14A', 'DEFM14C', 'DEFN14A', 'DEFR14A', 'DEFR14C', 'DEL AM', 'DFAN14A', 'DFRN14A', 'DOS', 'DOSLTR', 'DRS', 'DRSLTR', 'DSTRBRPT', 'EFFECT', 'F-1', 'F-10', 'F-10EF', 'F-10POS', 'F-1MEF', 'F-3', 'F-3ASR', 'F-3D', 'F-3DPOS', 'F-3MEF', 'F-4', 'F-4 POS', 'F-4MEF', 'F-6', 'F-6 POS', 'F-6EF', 'F-7', 'F-7 POS', 'F-8', 'F-8 POS', 'F-80', 'F-80POS', 'F-9', 'F-9 POS', 'F-N', 'F-X', 'FOCUSN', 'FWP', 'G-405', 'G-405N', 'G-FIN', 'G-FINW', 'IRANNOTICE', 'MA', 'MA-A', 'MA-I', 'MA-W', 'MSD', 'MSDCO', 'MSDW', 'N-1', 'N-14', 'N-14 8C', 'N-14MEF', 'N-18F1', 'N-1A', 'N-2', 'N-2 POSASR', 'N-23C-2', 'N-23C3A', 'N-23C3B', 'N-23C3C', 'N-2ASR', 'N-2MEF', 'N-30B-2', 'N-30D', 'N-4', 'N-5', 'N-54A', 'N-54C', 'N-6', 'N-6F', 'N-8A', 'N-8B-2', 'N-8F', 'N-8F NTC', 'N-8F ORDR', 'N-CEN', 'N-CR', 'N-CSR', 'N-CSRS', 'N-MFP', 'N-MFP1', 'N-MFP2', 'N-PX', 'N-Q', 'N-VP', 'N-VPFS', 'NO ACT', 'NPORT-EX', 'NPORT-NP', 'NPORT-P', 'NRSRO-CE', 'NRSRO-UPD', 'NSAR-A', 'NSAR-AT', 'NSAR-B', 'NSAR-BT', 'NSAR-U', 'NT 10-D', 'NT 10-K', 'NT 10-Q', 'NT 11-K', 'NT 20-F', 'NT N-CEN', 'NT N-MFP', 'NT N-MFP1', 'NT N-MFP2', 'NT NPORT-EX', 'NT NPORT-P', 'NT-NCEN', 'NT-NCSR', 'NT-NSAR', 'NTFNCEN', 'NTFNCSR', 'NTFNSAR', 'NTN 10D', 'NTN 10K', 'NTN 10Q', 'NTN 20F', 'OIP NTC', 'OIP ORDR', 'POS 8C', 'POS AM', 'POS AMI', 'POS EX', 'POS462B', 'POS462C', 'POSASR', 'PRE 14A', 'PRE 14C', 'PREC14A', 'PREC14C', 'PREM14A', 'PREM14C', 'PREN14A', 'PRER14A', 'PRER14C', 'PRRN14A', 'PX14A6G', 'PX14A6N', 'QRTLYRPT', 'QUALIF', 'REG-NR', 'REVOKED', 'RW', 'RW WD', 'S-1', 'S-11', 'S-11MEF', 'S-1MEF', 'S-20', 'S-3', 'S-3ASR', 'S-3D', 'S-3DPOS', 'S-3MEF', 'S-4', 'S-4 POS', 'S-4EF', 'S-4MEF', 'S-6', 'S-8', 'S-8 POS', 'S-B', 'S-BMEF', 'SBSE', 'SBSE-A', 'SBSE-BD', 'SBSE-C', 'SBSE-W', 'SC 13D', 'SC 13E1', 'SC 13E3', 'SC 13G', 'SC 14D9', 'SC 14F1', 'SC 14N', 'SC TO-C', 'SC TO-I', 'SC TO-T', 'SC13E4F', 'SC14D1F', 'SC14D9C', 'SC14D9F', 'SD', 'SDR', 'SE', 'SEC ACTION', 'SEC STAFF ACTION', 'SEC STAFF LETTER', 'SF-1', 'SF-3', 'SL', 'SP 15D2', 'STOP ORDER', 'SUPPL', 'T-3', 'TA-1', 'TA-2', 'TA-W', 'TACO', 'TH', 'TTW', 'UNDER', 'UPLOAD', 'WDL-REQ', 'X-17A-5'] | Type of the SEC filing form. | None | True |
| use_cache | bool | Whether or not to use cache. If True, cache will store for one day. | True | True |
</TabItem>

<TabItem value='tmx' label='tmx'>

| Name | Type | Description | Default | Optional |
| ---- | ---- | ----------- | ------- | -------- |
| symbol | str | Symbol to get data for. | None | True |
| form_type | str | Filter by form type. Check the data provider for available types. | None | True |
| limit | int | The number of data entries to return. | 100 | True |
| provider | Literal['fmp', 'intrinio', 'sec', 'tmx'] | The provider to use for the query, by default None. If None, the provider specified in defaults is selected or 'fmp' if there is no default. | fmp | True |
| start_date | Union[date, str] | The start date to fetch. | None | True |
| end_date | Union[date, str] | The end date to fetch. | None | True |
</TabItem>

</Tabs>

---

## Data

<Tabs>

<TabItem value='standard' label='standard'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| filing_date | date | The date of the filing. |
| accepted_date | datetime | Accepted date of the filing. |
| symbol | str | Symbol representing the entity requested in the data. |
| cik | str | Central Index Key (CIK) for the requested entity. |
| report_type | str | Type of filing. |
| filing_url | str | URL to the filing page. |
| report_url | str | URL to the actual report. |
</TabItem>

<TabItem value='fmp' label='fmp'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| filing_date | date | The date of the filing. |
| accepted_date | datetime | Accepted date of the filing. |
| symbol | str | Symbol representing the entity requested in the data. |
| cik | str | Central Index Key (CIK) for the requested entity. |
| report_type | str | Type of filing. |
| filing_url | str | URL to the filing page. |
| report_url | str | URL to the actual report. |
</TabItem>

<TabItem value='intrinio' label='intrinio'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| filing_date | date | The date of the filing. |
| accepted_date | datetime | Accepted date of the filing. |
| symbol | str | Symbol representing the entity requested in the data. |
| cik | str | Central Index Key (CIK) for the requested entity. |
| report_type | str | Type of filing. |
| filing_url | str | URL to the filing page. |
| report_url | str | URL to the actual report. |
| id | str | Intrinio ID of the filing. |
| period_end_date | date | Ending date of the fiscal period for the filing. |
| sec_unique_id | str | SEC unique ID of the filing. |
| instance_url | str | URL for the XBRL filing for the report. |
| industry_group | str | Industry group of the company. |
| industry_category | str | Industry category of the company. |
</TabItem>

<TabItem value='sec' label='sec'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| filing_date | date | The date of the filing. |
| accepted_date | datetime | Accepted date of the filing. |
| symbol | str | Symbol representing the entity requested in the data. |
| cik | str | Central Index Key (CIK) for the requested entity. |
| report_type | str | Type of filing. |
| filing_url | str | URL to the filing page. |
| report_url | str | URL to the actual report. |
| report_date | date | The date of the filing. |
| act | Union[int, str] | The SEC Act number. |
| items | Union[str, float] | The SEC Item numbers. |
| primary_doc_description | str | The description of the primary document. |
| primary_doc | str | The filename of the primary document. |
| accession_number | Union[int, str] | The accession number. |
| file_number | Union[int, str] | The file number. |
| film_number | Union[int, str] | The film number. |
| is_inline_xbrl | Union[int, str] | Whether the filing is an inline XBRL filing. |
| is_xbrl | Union[int, str] | Whether the filing is an XBRL filing. |
| size | Union[int, str] | The size of the filing. |
| complete_submission_url | str | The URL to the complete filing submission. |
| filing_detail_url | str | The URL to the filing details. |
</TabItem>

<TabItem value='tmx' label='tmx'>

| Name | Type | Description |
| ---- | ---- | ----------- |
| filing_date | date | The date of the filing. |
| accepted_date | datetime | Accepted date of the filing. |
| symbol | str | Symbol representing the entity requested in the data. |
| cik | str | Central Index Key (CIK) for the requested entity. |
| report_type | str | Type of filing. |
| filing_url | str | URL to the filing page. |
| report_url | str | URL to the actual report. |
| description | str | The description of the filing. |
| size | str | The file size of the PDF document. |
</TabItem>

</Tabs>
