# wikidot-css-scraper

A quick, ad hoc script to scrape both CSS from pages on the SCP Wiki (though it could be adapted to work on any Wikidot site). It looks for both inline styling (e.g. `style="color: red;"`), and CSS modules (i.e. `[[module CSS]]`). In the absence of proper Wikidot tools to understand what styling is used on a site, this can help fill that gap.

This does not search all pages, only mainlist SCP articles (excluding -Js, 001s, etc.)

### Utilization

This repository has two scripts:

* `scraper.js` runs through pages and looks for any CSS. Any styles, as well as the entire page sources are written to `extracted-styles.json`.
* `merge.js` is able to merge different JSON files into one. Because the scraper can continue off from incomplete jobs (anything remaining in `extracted-styles.json`), this can be used to take incomplete results and combine them.

### Licensing

This code is available under the terms of the MIT License.
