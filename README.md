# Wines Export Observatory (open data)

Which Italian wine denominations foreign buyers carry, country by country, and where each denomination is listed
worldwide. Published monthly by Wines Export (Servizi Digitali 24 S.R.L., Rome, Italy).
Live, updated version: https://www.wines-export.com/en/observatory

- Snapshot month: 2026-11
- Computed on: 2026-11-23 (UTC)
- Publisher: Wines Export — https://www.wines-export.com
- Contact: info@wines-export.com
- License: Creative Commons Attribution 4.0 International (CC BY 4.0)

## Files

### `data/2026-11/wines-export-observatory-2026-11-buyers.csv`
The Italian denominations most carried by foreign wine buyers.

| column | meaning |
|---|---|
| `snapshot_month` | first day of the snapshot month (YYYY-MM-DD) |
| `scope` | `world` = all foreign buyers together; `country` = buyers of one country |
| `country_iso2` | ISO 3166-1 alpha-2 country code, or `WORLD` |
| `rank` | position of the denomination within that scope (1 = most carried) |
| `denomination` | Italian denomination or grape name as declared by buyers |
| `share_of_buyers_pct` | share (%) of buyers carrying the denomination, among the buyers of that scope whose Italian range is known |

A buyer usually carries several denominations, so shares do not add up to 100.
For each country the file lists the ten most carried denominations; the world scope lists all 33 denominations tracked by the Observatory.

### `data/2026-11/wines-export-observatory-2026-11-listings.csv`
Where each denomination is listed by retailers and online stores.

| column | meaning |
|---|---|
| `snapshot_month` | first day of the snapshot month (YYYY-MM-DD) |
| `denomination` | Italian denomination or grape name |
| `rank` | position of the country for that denomination (1 = largest share) |
| `country_iso2` | ISO 3166-1 alpha-2 country code |
| `share_of_listings_pct` | each country's share (%) of the observed listings of that denomination |

Only the eight largest countries per denomination are listed, so shares do not add up to 100.

## Method

- **Buyers:** companies that buy wine to resell it (importers, distributors, wholesalers, wine shops, online stores),
  identified from company registers, customs data, trade fairs and company websites. Companies outside the wine trade
  and those that asked not to appear are excluded.
- **Share of buyers:** among a country's buyers whose Italian range is known, the percentage carrying a given
  denomination. Only countries with a broad base are published.
- **Listings:** the Italian wine bottles read on the lists of retailers and online stores, country by country. The share
  is each country's weight on the observed listings of that denomination.
- The dataset contains only shares and rankings: no company names, contacts or absolute counts.

## How to cite

Wines Export (2026). *Wines Export Observatory — November 2026 snapshot* [Data set]. https://www.wines-export.com/en/observatory

## Snapshots

| month | folder |
|---|---|
| 2026-11 | `data/2026-11/` |

Each monthly snapshot is published as a GitHub release.
