#  Multi-Site Biorepository Sample Tracker

An advanced dual-cohort sample management system built in Microsoft Excel,
designed for multi-site biospecimen distribution across clinical research facilities.

##  Overview
Tracks Case and Control participant samples across four storage modalities
and three international sites. Automatically routes samples to the correct
plate position or storage box upon data entry, and generates standardized
sample labels.

##  Workbook Structure

| Sheet | Purpose |
|---|---|
| CASE MASTER | Central case registry — Study Code, sample type, collection/freeze timestamps, auto-routing to 4 locations |
| CONTROL MASTER | Same registry structure for control participants |
| Case/Control CDI Plate | 96-well plate maps for CDI site (SER, PLH, CSF) |
| Case/Control NIH Plate | 96-well plate maps for NIH site |
| Case/Control MAX Planck Plate | 96-well plate maps for Max Planck Institute |
| Cryovial Case/Control Box | 10×10 cryovial box layout with volume-aware label generation |
| Case/Control WB Box | 9×9 whole blood storage box layout |

##  Key Excel Features Used
- Dual-cohort tracking with separate Case (s/i status) and Control registries
- Auto-routing to CDI, NIH, Max Planck, and cryovial locations via `COUNTIFS()`
- Automatic sample label generation with date codes and sample type prefixes
- Multi-range cryovial position parsing using nested `MID`, `SUBSTITUTE`, and `FIND`
- `SUMPRODUCT`-based 2D box position lookup for cryovial and WB storage
- Cross-sheet `INDEX/MATCH` for all plate map population

##  Tools Used
- Microsoft Excel 365 (advanced formula support required)

##  Files
- `Biospecimen-Tracking-System.xlsx` — Full dual-cohort tracking workbook
