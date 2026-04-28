# Draft
## Data Preparation

### 1. Data Source

The empirical material is drawn from a corpus of scanned annual account volumes from **Exeter College, Oxford University**, covering the period `1700-1900`. The research corpus consists of page-image PDFs derived from handwritten account books rather than born-digital text files.

At the raw-source level, the corpus contains `193` PDF volumes and `1,581` total pages. The raw total of `1,581` pages matches the repository's repeated reference to `1,581` enriched pages, indicating that the processed corpus is close to the full raw page universe.

The archive is best understood as a sequence of annual or fiscal-year account volumes rather than as a uniform panel of calendar-year text. Coverage is broad but not perfectly continuous: a small number of years are missing from the surviving raw corpus, and some overlap reflects fiscal-year conventions. Across the corpus, the basic documentary form remains stable enough to support systematic extraction, while language and reporting conventions evolve over time.

### 2. Corpus Structure and Source Conventions

Three source-level features are especially important for later data construction: the time unit of observation, the structure of the account page, and the language of recordkeeping.

First, the relevant temporal unit is not always the calendar year. In the earlier part of the archive, volumes are more appropriately interpreted as accounting-year records, often running from early November of one year to early November of the next. Later material appears more mixed, and some later nineteenth-century examples look closer to year-end general accounts. The year attached to a volume should therefore be read as a source label rather than assumed to mark a strict January-to-December interval.

Second, the page itself is highly regular in broad layout. A typical page contains a heading or year label at the top, a date field on the left, a central block of entry descriptions, and pre-decimal currency columns on the right for pounds, shillings, and pence, often followed by a subtotal or total. This repeated organization provides the basis for the later construction of row-level structured observations.

Suggested figure title:
- `Typical Structure of an Account Page`

Suggested example image:
- Annotated version: [exeter_college_typical_page_annotated.png](/Users/EthanJoo/PhD/Research/Archieve/exeter_college_typical_page_annotated.png)
- Source page: [1830_p1.jpg](/Users/EthanJoo/PhD/Research/Archieve/tmp/later_period_samples/1830_p1.jpg)

Suggested callouts:
- `Headings / Year Label`
- `Dates`
- `Entry Descriptions`
- `Amounts (£ | s. | d.)`
- `Subtotal / Total`

Suggested caption:
- `Example of a typical account-page layout from the Exeter College corpus. The illustrated page shows the recurring components used throughout much of the archive: headings and a year label at the top, dates on the left, entry descriptions in the center, and pre-decimal currency columns on the right for pounds, shillings, and pence, with a subtotal or total at the bottom. This regular structure underlies the subsequent extraction and structuring of page-level observations.`

Third, the language of entry shifts over time. Earlier volumes rely more heavily on Latin or Latinized accounting forms, whereas later pages make greater use of English headings and descriptions. The transition is gradual rather than abrupt, and many intermediate pages are mixed. The source should therefore be understood as historically evolving rather than linguistically uniform.

Taken together, these conventions define the terms on which later extraction, enrichment, and aggregation operate. The next stage of data preparation converts these recurring page-level structures into row-level structured observations, which are then enriched and aggregated into analysis-ready variables.
