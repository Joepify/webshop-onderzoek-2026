# Staat van de Nederlandse webshop 2026 (State of the Dutch webshop 2026)

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23561392.svg)](https://doi.org/10.5281/zenodo.23561392)

Open dataset by [Joepify](https://www.joepify.nl) (Rotterdam, NL): an automated, outside-in check of **220 Dutch webshops** on e-mail security, HTTPS and security headers, legally required information and cookie banners. Measured on **15 October 2026**.

Full report (Dutch): https://www.joepify.nl/onderzoek-webshops-2026

## Key figures (all 220 shops)

| Metric | Share |
|---|---|
| SPF record present | 94.1% |
| DMARC record present | 65.9% |
| DMARC set to quarantine or reject | 23.2% |
| Valid HTTPS | 96.4% |
| HSTS header | 44.5% |
| Content-Security-Policy header | 24.5% |
| KvK (Chamber of Commerce) number shown | 38.6% |
| VAT number shown | 28.6% |
| Withdrawal (herroeping) information or button found | 48.6% |
| Accessibility statement found | 0.9% |
| Cookie banner on first page load | 38.2% |
| PHP version below 8.2 visible from outside | 7.3% |

Per-platform breakdowns (Shopify, WooCommerce, Lightspeed, unknown) are in the CSV. Small groups: differences of a few percentage points are noise.

## Files

- `onderzoek-webshops-2026-data.csv`: aggregated results (100 rows: 20 metrics x platform groups). Columns are described in [CODEBOOK.md](CODEBOOK.md).
- `CITATION.cff`: how to cite this dataset.

## Method (summary)

- **Sample:** webshops taken from OpenStreetMap (businesses with a website tagged as shop/webshop) with a .nl website; 220 included.
- **Checks:** home page and standard pages (terms, privacy) fetched automatically; DNS records (SPF, DMARC) queried; HTTPS connection and response headers checked; cookie banner detected on the first page load without clicking.
- **Anonymous:** no names, domains or addresses of shops are published, only totals.

## Limitations

- **Not a random sample.** OpenStreetMap mostly contains shops someone entered, more often shops with a physical address. Pure online shops and large chains are probably under-represented. Results apply to this group, not to all Dutch webshops.
- **Automated signals.** A "no" means *not found*, not *proven absent*: a withdrawal button or accessibility statement can exist on a page the script did not find.
- **Missing is not a violation.** Not every rule applies to every shop (e.g. the micro-enterprise exemption for accessibility). No individual shop is assessed legally.
- **Snapshot:** one day (15 Oct 2026); shops may have changed since.

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). You may share and adapt, also commercially, as long as you credit **Joepify** with a link to https://www.joepify.nl/onderzoek-webshops-2026 .

## Citation

Assaidi, A. (2026). *Staat van de Nederlandse webshop 2026* [Data set]. Joepify. https://doi.org/10.5281/zenodo.23561392

## Contact

Ayoub Assaidi, Joepify, Metaalhof 27, 3067 GM Rotterdam. info@joepify.nl, +31 6 87 19 50 43.
Check your own webshop on the same points: https://www.joepify.nl/website-apk
