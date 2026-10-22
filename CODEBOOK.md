# Codebook

Each row is one aggregated measurement. No individual webshops, domains or addresses are published.

| Column | Meaning |
|---|---|
| groep | Category: mail, tls (HTTPS and security headers), legal, cookies, overig (other) |
| platform | `alle` (all 220 shops) or a platform (e.g. shopify, woocommerce, lightspeed) |
| metric | Machine-readable metric id |
| omschrijving | Dutch description of the metric |
| n_gecontroleerd | Number of shops checked for this metric in this group |
| aantal | Number of shops where the signal was found |
| percentage | aantal / n_gecontroleerd x 100, one decimal |

## Metrics

| groep | metric | omschrijving (NL) |
|---|---|---|
| mail | spf | heeft een SPF-record |
| mail | dmarc | heeft een DMARC-record |
| mail | dmarc_enforced | DMARC staat op quarantine of reject |
| tls | https | bereikbaar via geldig HTTPS |
| tls | http_redirect | stuurt http door naar https |
| tls | hsts | stuurt een HSTS-header |
| tls | hdr_csp | stuurt een Content-Security-Policy |
| tls | hdr_xcto | stuurt X-Content-Type-Options |
| tls | hdr_frame | beschermt tegen framing (X-Frame-Options/CSP) |
| tls | hdr_referrer | stuurt een Referrer-Policy |
| legal | kvk | toont een KvK-nummer |
| legal | btw | toont een btw-nummer |
| legal | herroeping | toont herroepingsinformatie of -knop |
| overig | herroepingsknop | herroepingsknop |
| legal | toegankelijkheid | heeft een toegankelijkheidsverklaring |
| cookies | cookie_banner | toont een cookiebanner |
| overig | viewport | viewport |
| overig | php_eol | php_eol |
| overig | wp_version_exposed | wp_version_exposed |
| overig | tls_expiry_30d | tls_expiry_30d |
