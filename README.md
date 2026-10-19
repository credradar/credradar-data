# Thailand International School Fee History (2020/21–2024/25)

Annual tuition fee history for international schools in Thailand — 455 school-year records for 99 schools, recovered from archived published sources. Every record is a figure that was actually published; nothing is interpolated, estimated, or modelled.

Published by [CredRadar](https://credradar.org) — Thailand international schools, every fee verified. The canonical report built on this dataset, with charts and methodology, is at **https://credradar.org/reports/thailand-international-school-fees/**

## What this is

One row per school per academic year, giving the lowest and highest published annual tuition figures (in Thai baht) for that year, the basis on which the figure was published, and a link to the archived source it was read from. The records span the 2017/18 to 2025/26 academic years and are concentrated in 2019/20–2024/25:

| Academic year | Records |
|---|---|
| 2017/18 | 1 |
| 2018/19 | 6 |
| 2019/20 | 54 |
| 2020/21 | 67 |
| 2021/22 | 79 |
| 2022/23 | 81 |
| 2023/24 | 82 |
| 2024/25 | 78 |
| 2025/26 | 7 |

Headline finding from the canonical report: on a like-for-like basis (the same 42 Bangkok schools with published fees in both 2020/21 and 2024/25), the median fee rose **+13.7%** over the four years — about **+3.3% per year**. Cross-sectional medians across different school sets should not be read as a trend; school composition changes between years.

## Files

- `fee-history-thailand-international-schools.csv` — the dataset (455 data rows + header).
- `LICENSE` — CC BY-NC 4.0 licence text.
- `dataset-metadata.json` — metadata for mirror uploads (e.g. Kaggle).

## Field dictionary

| Column | Meaning |
|---|---|
| `school_slug` | CredRadar's stable identifier for the school. It matches the slug in the school's page URL on credradar.org (e.g. `https://credradar.org/schools/<school_slug>/`). |
| `school_name` | The school's name as listed on CredRadar. |
| `academic_year` | The academic year the figure applies to, as labelled by the source (e.g. `2024/25`). |
| `fee_min_thb` | The lowest published annual tuition figure for that school-year, in Thai baht (THB, nominal — no inflation or currency adjustment). |
| `fee_max_thb` | The highest published annual tuition figure for that school-year, in Thai baht (THB, nominal). |
| `basis` | How the published figure is structured: `range` (a published low–high span), `single figure` (one figure was published; it is stored as min = max and is **not** a range), or `per-grade table` (the span of the school's published per-grade fee table). Some values carry a parenthetical qualification where the basis needs one — the qualification is part of the record and travels with it. |
| `source_type` | Provenance of the archived source — see the source labels below. `wayback-official` = **[O]**, `wayback-isd` = **[A]**. |
| `source_url` | The archived (Internet Archive Wayback Machine) snapshot the figure was read from. |
| `snapshot_date` | The date of that archived snapshot (YYYY-MM-DD). |

## How the figures were compiled

Each figure was read from an archived copy of a published source — either the school's own published fee document or fee page, or a third-party aggregator listing — retrieved via the Wayback Machine. CredRadar labels every fee figure with its provenance, and the same labels apply to this dataset:

- **[O] Official fees** (`source_type = wayback-official`, 42 records) — fee taken from the school's own published fee document.
- **[A] Aggregator figure** (`source_type = wayback-isd`, 413 records) — fee as listed by a third-party aggregator (e.g. ISD, Edarabia). Not the school's own published figure — confirm with the school.

Compilation rules:

- Only figures actually published in an archived source are included. No interpolation, no estimated years, no smoothing.
- Where an official per-grade table and an aggregator figure both existed for the same school-year, the official figure replaces the aggregator figure.
- Figures are the published annual tuition span as it appeared. Any qualification — for example, a figure that includes residential trips, or an annual total summed from term instalments — is recorded in the `basis` column rather than silently adjusted.
- 2019/20 caveat: the aggregator published a single fee figure per school that year (`basis = single figure`, stored as min = max). Do not plot those rows as ranges or mix them into range-based statistics.
- All amounts are nominal Thai baht as published. No inflation adjustment and no currency conversion has been applied.

## Coverage caveat

This dataset covers the **international-school segment only** — schools offering an international curriculum — not all Thai private K–12 education. Thailand's bilingual, English Programme and Thai-programme private schools number in the thousands and are outside the scope of this dataset. Not every international school publishes historical fees, and not every published fee page survives in the archive: the 99 schools here are those for whom at least one historical figure could be recovered and verified. Absence of a school or a year means no figure could be verified — not that the fee was zero or unchanged.

## Cite as

> CredRadar. *Thailand International School Fee History (2020/21–2024/25)* [dataset]. Canonical report: https://credradar.org/reports/thailand-international-school-fees/

## Licence

This dataset is released under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** licence — see `LICENSE`. Attribution is required (link to https://credradar.org/reports/thailand-international-school-fees/); commercial use is not permitted under this licence.
