# ausOpenData

`ausOpenData` provides simple, reproducible access to Austin-related
datasets from the  
[Austin Open Data Portal](https://data.austintexas.gov/) platform — directly
from R, with **no API keys** or manual downloads required. Working directly with
Socrata APIs can be cumbersome — `ausOpenData` simplifies this process
into a clean, reproducible workflow.

Version **0.1.0** introduces a streamlined, catalog-driven interface for
Austin Open Data, extending the open data ecosystem beyond New York to support 
cross-city analysis and comparative civic research.

The package provides three core functions:

- `aus_list_datasets()` — Browse available datasets from the live Austin
  Open Data catalog
- `aus_pull_dataset()` — Pull any cataloged dataset by key, with
  filtering, ordering, and optional date controls
- `aus_any_dataset()` — Pull any Austin Open Data dataset directly via its
  Socrata JSON endpoint

Datasets pulled via `aus_pull_dataset()` automatically apply sensible
defaults from the catalog (such as default ordering and date fields),
while still allowing user control over:

- limit
- filters
- date / from / to
- where
- order
- clean_names
- coerce_types

This redesign reduces maintenance burden, improves extensibility, and
provides a more scalable interface for working with Austin Open Data.

All functions return clean **tibble** outputs and support filtering
via  
`filters = list(field = "value")`.

------------------------------------------------------------------------

## Installation

### Development version (GitHub)

``` r
devtools::install_github("martinezc1/ausOpenData")
```

------------------------------------------------------------------------

## Example

```{r message=FALSE, warning=FALSE}
library(ausOpenData)

aus_vacent_buildings <- aus_pull_dataset(
  dataset = "golf_courses_in_austin",
  limit = 10
)

head(la_vacent_buildings)
```

## About

`ausOpenData` makes Austin's civic datasets accessible to
students,  
educators, analysts, and researchers through a unified and user-friendly
R interface.

Developed to support reproducible research, open-data literacy, and
real-world analysis.

------------------------------------------------------------------------

## Comparison to Other Software

While the [`RSocrata`](https://CRAN.R-project.org/package=RSocrata)
package provides a general interface for any Socrata-backed portal,
`ausOpenData` is specifically tailored for **Austin Open Data Portal**.

This package is part of a broader ecosystem of tools for working with
open data:

- `nycOpenData` — streamlined access to NYC Open Data  
- `nysOpenData` — streamlined access to NY State Open Data
- `mtaOpenData` — streamlined access to MTA-related NY State Open Data
- `chiOpenData` — streamlined access to Chicago-related City Open Data
- `laOpenData` — streamlined access to Los Angeles-related City Open Data

Together, these packages provide a consistent, user-friendly interface
for working with civic data across jurisdictions.

- **Ease of Use**: No need to hunt for 4x4 dataset IDs (e.g.,
  `9t4d-g238`); use catalog-based keys instead.
- **Open Literacy**: Designed specifically for students and researchers
  to lower the barrier to entry for civic data analysis.

------------------------------------------------------------------------

## Contributing

We welcome contributions! If you find a bug or would like to request a
wrapper for a specific Austin dataset, please open an issue or submit a
pull request on [GitHub](https://github.com/martinezc1/ausOpenData).

------------------------------------------------------------------------

## Authors & Contributors

### Maintainer

**Christian A. Martinez** 📧 <c.martinez0@outlook.com>  
GitHub: [@martinezc1](https://github.com/martinezc1)
