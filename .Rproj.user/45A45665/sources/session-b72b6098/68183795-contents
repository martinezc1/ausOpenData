
# laOpenData

`laOpenData` provides simple, reproducible access to Los Angeles-related
datasets from the  
[Los Angeles Open Data Portal](https://data.lacity.org/) platform —
directly from R, with **no API keys** or manual downloads required.
Working directly with Socrata APIs can be cumbersome — `laOpenData`
simplifies this process into a clean, reproducible workflow.

Version **0.1.0** introduces a streamlined, catalog-driven interface for
Los Angeles Open Data, extending the open data ecosystem beyond New York
to support cross-city analysis and comparative civic research.

The package provides three core functions:

- `la_list_datasets()` — Browse available datasets from the live Los
  Angeles Open Data catalog
- `la_pull_dataset()` — Pull any cataloged dataset by key, with
  filtering, ordering, and optional date controls
- `la_any_dataset()` — Pull any Los Angeles Open Data dataset directly
  via its Socrata JSON endpoint

Datasets pulled via `la_pull_dataset()` automatically apply sensible
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
provides a more scalable interface for working with Los Angeles Open
Data.

All functions return clean **tibble** outputs and support filtering
via  
`filters = list(field = "value")`.

------------------------------------------------------------------------

## Installation

### Development version (GitHub)

``` r
devtools::install_github("martinezc1/laOpenData")
```

------------------------------------------------------------------------

## Example

``` r
library(laOpenData)

la_vacent_buildings <- la_pull_dataset(
  dataset = "building_and_safety_vacant_building_abatement",
  limit = 1000
)

head(la_vacent_buildings)
#> # A tibble: 6 × 10
#>   address         case_num    cd inspector_name area  building_type approved_use
#>   <chr>              <dbl> <dbl> <chr>          <chr> <chr>         <chr>       
#> 1 749 S KOHLER ST  1045424    14 LUCIANO GAUNA  II    III           COMMERCIAL  
#> 2 11354 W RUNNYM…  1044681     2 GLEN RAND      I     *****         <NA>        
#> 3 1346 W 5TH ST     924823     1 LUCIANO GAUNA  II    *****         COMMERCIAL  
#> 4 11354 W RUNNYM…  1044681     2 GLEN RAND      I     *****         <NA>        
#> 5 11354 W RUNNYM…  1044681     2 GLEN RAND      I     *****         <NA>        
#> 6 2219 S CENTRAL…  1026127     9 LUCIANO GAUNA  II    *****         <NA>        
#> # ℹ 3 more variables: assigned_to <chr>, building_size <chr>,
#> #   abate_effective <dttm>
```

## About

`laOpenData` makes Los Angeles’s civic datasets accessible to
students,  
educators, analysts, and researchers through a unified and user-friendly
R interface.

Developed to support reproducible research, open-data literacy, and
real-world analysis.

------------------------------------------------------------------------

## Comparison to Other Software

While the [`RSocrata`](https://CRAN.R-project.org/package=RSocrata)
package provides a general interface for any Socrata-backed portal,
`laOpenData` is specifically tailored for **Los Angeles Open Data
Portal**.

This package is part of a broader ecosystem of tools for working with
open data:

- `nycOpenData` — streamlined access to NYC Open Data  
- `nysOpenData` — streamlined access to NY State Open Data
- `mtaOpenData` — streamlined access to MTA-related NY State Open Data
- `chiOpenData` — streamlined access to Chicago-related City Open Data

Together, these packages provide a consistent, user-friendly interface
for working with civic data across jurisdictions.

- **Ease of Use**: No need to hunt for 4x4 dataset IDs (e.g.,
  `2ucp-7wg5`); use catalog-based keys instead.
- **Open Literacy**: Designed specifically for students and researchers
  to lower the barrier to entry for civic data analysis.

------------------------------------------------------------------------

## Contributing

We welcome contributions! If you find a bug or would like to request a
wrapper for a specific Los Angeles dataset, please open an issue or
submit a pull request on
[GitHub](https://github.com/martinezc1/laOpenData).

------------------------------------------------------------------------

## Authors & Contributors

### Maintainer

**Christian A. Martinez** 📧 <c.martinez0@outlook.com>  
GitHub: [@martinezc1](https://github.com/martinezc1)
