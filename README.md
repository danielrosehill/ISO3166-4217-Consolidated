## ISO-3166 & ISO-4217 "Consolidated" Lookup Dataset

This dataset contains a mapping between ISO-3166 (countries) and ISO-4217 (currencies).

The objective was to create a single dataset to support everyday workloads in international financial analysis undertaken by "casual" / non-official actors and analysts. 

## Version

V1

Compiled by: Daniel Rosehill
Date: 03-09 (September) - 2025

Note: geopolitics and the global financial system are clearly dynamic concepts. 

Much as this dataset is totally unofficial (and should be used accordingly) it also reflects a mapping based upon a static copy of the data sourced on September 03, 2025. 

ISO-4217 provides a separate sub-standard for historic currencies. Countries change name from time to time, secede, join monetary alliances, etc. These changes are reflected in the ongoing revision process of the ISO standards which also (ISO-4217) provides a lookup for former/deprecated currencies. 

### Provenance / Edits

To reflect the intended 

- Several currencies provided in ISO-4217 and which are not the permament formal/national currency of current soverign entities were excludedc from the matching logic. 

- See `changelog.md` for a list of these. These include multilateral mechanisms like Special Drawing Rights. 

## Enriched Data

A few Booleans were added to help quickly identify outliers in the international currency system such as the (relatively few) countries in which there are multiple legaly units of tender, as captured in ISO-4217.

---

# Repository Organisation 

## Original Data Sources

- `source/edited/iso-3166.csv`: ISO 3166 territory list (edited copy).
- `source/edited/iso-4217-edited.csv`: ISO 4217 currency list (edited to remove special instruments and historical entries).

## Consolidated / Mapped Data

### As CSV

- `consolidated.csv`: Base consolidated table with ISO identifiers and up to two currencies per territory.
- `consolidated_enriched.csv`: Same as base plus derived flags for common analyses.

### As JSON

- `consolidatd.json`: JSON array version of the base consolidated table.
- `consolidated_enriched.json`: JSON array version of the enriched table (flags as booleans).

---

## Data Dictionary

- `country_common_name`: Territory name from ISO 3166.
- `iso_3166_alpha-2`: Two-letter country code.
- `iso_3166_alpha-3`: Three-letter country code.
- `iso_3166_code`: Numeric country code.
- `iso_4217_currency_name_currency_1`: Primary currency name.
- `iso_4217_alphabetic_code_currency_1`: Primary 4217 alphabetic currency code.
- `iso_4217_numeric_code_currency_1`: Primary 4217 numeric currency code.
- `iso_4217_currency_name_currency_2`: Secondary currency name (if applicable).
- `iso_4217_alphabetic_code_currency_2`: Secondary 4217 alphabetic code (if applicable).
- `iso_4217_numeric_code_currency_2`: Secondary 4217 numeric code (if applicable).
- `has_multiple_currencies` (enriched): 1 if two currencies listed for the territory, else 0.
- `shared_currency` (enriched): 1 if any listed currency code is used by multiple territories, else 0.
- `is_usd` (enriched): 1 if USD is one of the listed currencies, else 0.
- `is_euro` (enriched): 1 if EUR is one of the listed currencies, else 0.
- `dollar_in_name` (enriched): 1 if any listed currency name contains the word “Dollar,” else 0.
