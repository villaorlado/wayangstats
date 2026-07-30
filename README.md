# Wayang occurrences in Singapore Malay newspapers

This dataset tracks occurrences of the word *wayang* ("وايڠ") in two Jawi-script
Malay-language newspapers published in Singapore: **Warta Malaya** (1930s) and
**Utusan Melayu** (1950s).

The 100 occurrences were identified from a random sample using a Gemma-based
model from AI Singapore, then manually verified.

## Why this matters

*Wayang* is a highly polysemous word. It can refer to puppetry (*wayang
kulit*, *wayang golek*), to stage performances such as Chinese opera,
*bangsawan*, or *kethoprak*, and to film — often as *wayang gambar*, or
simply implied from context. Because a single term spans such a wide
semantic range, tracking how its usage is distributed across these senses
over time offers a window into semantic narrowing: as cinema became more
prominent in Singapore, *wayang* increasingly came to mean "film," at the
expense of its older theatrical and puppetry senses. Comparing Warta Malaya
(1930s) against Utusan Melayu (1950s) lets us observe this shift
quantitatively rather than anecdotally.

## Files

### `wayang_dataset.csv`

100 rows, one per occurrence, with the following columns:

- `date` — publication date of the issue (range: 1933-04-25 to 1956-07-24)
- `newspaper` — `WM` (Warta Malaya) or `UM` (Utusan Melayu)
- `page_number` — page number within the issue
- `page_url` — link to the scanned page image
- `full_segment` — the Jawi text surrounding the occurrence
- `type` — sense in which *wayang* is used: `film`, `theatre/opera`, `puppetry`, or `metaphor`

### `per_type.png`

![Wayang occurrences per type](per_type.png)

Total count of occurrences by type across both newspapers.

### `per_type_newspaper.png`

![Wayang occurrences per type per newspaper](per_type_newspaper.png)

Same breakdown by type, split by newspaper (WM vs UM).
