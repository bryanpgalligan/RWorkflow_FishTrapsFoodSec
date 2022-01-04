# FishTrapsFoodSec

## Escape gaps contribute to ecosystem health and food security in an artisanal coral reef trap fishery.

**Authors:**

-   Bryan P. Galligan, S.J. ([bgalligan\@jesuits.org](mailto:bgalligan@jesuits.org))

-   Austin Humphries ([humphries\@uri.edu](mailto:humphries@uri.edu))

-   Tim McClanahan ([tmcclanahan\@wcs.org](mailto:tmcclanahan@wcs.org))

## Overview

This repository is the data management and analysis workflow of a research project investigating the ecosystem and food security benefits of adding escape gaps to traditional African fish traps. It includes 10 years of landings data from artisanal fishers operating in the inshore waters of Kenya and Tanzania. Our hypotheses correspond to the FAO's food security framework (Stability, Availability, Access, and Utilization) (FAO et al., 2021):

-   Modified fish traps contribute to the **stability** of coastal East African food systems, enhancing coral reef resilience...

    -   ...by generating less functionally diverse catches.

    -   ...by catching fewer herbivorous fish.

-   Modified fish traps contribute to the **availability** of food, enhancing stock status...

    -   ...by catching lower proportions of immature individuals and individuals below optimum length.

    -   ...but selectively target larger individuals and thus do not help maintain a population of mega-spawners.

-   Modified fish traps increase **access** to food...

    -   ...by catching as much or more fish and key micronutrients by mass as traditional traps.

    -   ...by maintaining or increasing catch value in comparison to traditional traps.

-   Modified traps could influence **utilization** of food...

    -   ...by making it more expensive to retain enough catch to satisfy the micronutrient needs of a child under five.

    -   ...by increasing or maintaining catch value after fishers retain enough catch to satisfy the micronutrient needs of a child under five.

## Instructions

R scripts should be run in numeric order, beginning with `01_CleanData_FishTrapsFoodSec.R`. Each script has two corresponding folders in the repository, one called `temp` and one called `out`. The `temp` folder contains temporary output files that are not needed for further analysis or reference. The `out` folder contains output files that will be used by subsequent scripts, kept for future reference, or formatted as data tables for publication.

## Repository Files

| File/Folder                                                                                                                             | Enclosed File                                                                                                                                                                  | Type            | Notes                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [00_RawData](https://github.com/bryanpgalligan/FishTrapsFoodSec/tree/master/00_RawData)                                                 |                                                                                                                                                                                | Folder          | Contains raw data                                                                                                                                       |
|                                                                                                                                         | [CombinedTrapData_2010_2019_Anonymized.csv](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/00_RawData/CombinedTrapData_2010_2019_Anonymized.csv)               | Spreadsheet     | WCS landings data                                                                                                                                       |
|                                                                                                                                         | [FunctionalGroupKey_DietBased_Condy2015.xlsx](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/00_RawData/FunctionalGroupKey_DietBased_Condy2015.xlsx)           | Spreadsheet     | A key developed for previous WCS studies assigning select species to diet-based functional groups                                                       |
| [01_CleanData_FishTrapsFoodSec.R](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/01_CleanData_FishTrapsFoodSec.R)       |                                                                                                                                                                                | R Script        | Cleans the data from WCS and saves an edited and more compact version                                                                                   |
| [01_CleanData_Out](https://github.com/bryanpgalligan/FishTrapsFoodSec/tree/master/01_CleanData_Out)                                     |                                                                                                                                                                                | Folder          | Contains output files from eponymous R script                                                                                                           |
|                                                                                                                                         | [TrapData_Cleaned.csv](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/01_CleanData_Out/TrapData_Cleaned.csv)                                                   | Spreadsheet     | Cleaned version of landings data                                                                                                                        |
| [01_CleanData_Temp](https://github.com/bryanpgalligan/FishTrapsFoodSec/tree/master/01_CleanData_Temp)                                   |                                                                                                                                                                                | Folder          | Contains temporary output files from eponymous R script                                                                                                 |
|                                                                                                                                         | [Unique_Species.csv](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/01_CleanData_Temp/Unique_Species.csv)                                                      | Spreadsheet     | A list of species found in the WCS landings data                                                                                                        |
| [02_Stability_FishTrapsFoodSec.R](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/02_Stability_FishTrapsFoodSec.R)       |                                                                                                                                                                                | R Script        | Analysis of the stability pillar of the food security framework                                                                                         |
| [02_Stability_Out](https://github.com/bryanpgalligan/FishTrapsFoodSec/tree/master/02_Stability_Out)                                     |                                                                                                                                                                                | Folder          | Contains output files from the eponymous R script                                                                                                       |
|                                                                                                                                         | [CatchComposition_DietCt_ModelComparison.csv](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/02_Stability_Out/CatchComposition_DietCt_ModelComparison.csv)     | Spreadsheet     | Results of model comparisons for an ANOVA testing effect of trap type on catch composition (no. of fish, categorized by diet-based functional groups)   |
|                                                                                                                                         | [CatchComposition_DietCt_Results.csv](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/02_Stability_Out/CatchComposition_DietCt_Results.csv)                     | Spreadsheet     | Results of ANOVA testing effect of trap type on catch composition (no. of fish, categorized by diet-based functional groups)                            |
|                                                                                                                                         | [CatchComposition_DietMass_ModelComparison.csv](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/02_Stability_Out/CatchComposition_DietMass_ModelComparison.csv) | Spreadsheet     | Results of model comparisons for an ANOVA testing effect of trap type on catch composition (biomass ratio, categorized by diet-based functional groups) |
|                                                                                                                                         | [CatchComposition_DietMass_Results.csv](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/02_Stability_Out/CatchComposition_DietMass_Results.csv)                 | Spreadsheet     | Results of ANOVA testing the effect of trap type on catch composition (biomass ratio, categorized by diet-based functional groups)                      |
|                                                                                                                                         | [CatchComposition_FunGrDiet_Data.csv](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/02_Stability_Out/CatchComposition_FunGrDiet_Data.csv)                     | Spreadsheet     | Datasheet used to analyze catch composition by diet-based functional group                                                                              |
| 02_Stability_Temp                                                                                                                       |                                                                                                                                                                                | Folder          | Empty                                                                                                                                                   |
| [03_Availability_FishTrapsFoodSec.R](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/03_Availability_FishTrapsFoodSec.R) |                                                                                                                                                                                | R Script        | Analysis of the availability pillar of the food security framework                                                                                      |
| 03_Availability_Out                                                                                                                     |                                                                                                                                                                                | Folder          | Contains model comparisons and results for effect of trap type on length                                                                                |
|                                                                                                                                         | LengthAOV_ModelComparison.csv                                                                                                                                                  | Spreadsheet     | Comparison of four ANOVAs for finding effect of trap type on length                                                                                     |
|                                                                                                                                         | LengthAOV_Results.csv                                                                                                                                                          | Spreadsheet     | Effect of trap type on length ANOVA results                                                                                                             |
| 03_Availability_Temp                                                                                                                    |                                                                                                                                                                                | Folder          | Empty                                                                                                                                                   |
| 04_Access_FishTrapsFoodSec.R                                                                                                            |                                                                                                                                                                                | R Script        | Analysis of the access pillar of the food security framework                                                                                            |
| 04_Access_Out                                                                                                                           |                                                                                                                                                                                | Folder          | Contains data, model comparisons, and results for effect of trap type on CPUE                                                                           |
|                                                                                                                                         | CPUE_Data.csv                                                                                                                                                                  | Spreadsheet     | Data for CPUE by trip for trips that only used one trap type (gated or traditional)                                                                     |
|                                                                                                                                         | CPUE_ModelComparison.csv                                                                                                                                                       | Spreadsheet     | Comparison of four ANOVAs for finding effect of trap type on CPUE                                                                                       |
|                                                                                                                                         | CPUE_Results.csv                                                                                                                                                               | Spreadsheet     | Effect of trap type on CPUE (ANOVA results)                                                                                                             |
| 04_Access_Temp                                                                                                                          |                                                                                                                                                                                | Folder          | Empty                                                                                                                                                   |
| 06_TabsFigs_FishTrapsFoodSec.R                                                                                                          |                                                                                                                                                                                | R Script        | Assembles tables and figures                                                                                                                            |
| 06_TabsFigs_Out                                                                                                                         |                                                                                                                                                                                | Folder          | Contains figures assembled so far                                                                                                                       |
|                                                                                                                                         | CPUE.jpeg                                                                                                                                                                      | Image           | Effect of trap type on CPUE                                                                                                                             |
|                                                                                                                                         | KeyHerbivores.jpeg                                                                                                                                                             | Image           | Effect of trap type on catch composition (ratio of key herbivores by mass)                                                                              |
|                                                                                                                                         | Length.jpeg                                                                                                                                                                    | Image           | Effect of trap type on length                                                                                                                           |
| 06_TabsFigs_Temp                                                                                                                        |                                                                                                                                                                                | Folder          | Empty                                                                                                                                                   |
| [README.md](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/README.md)                                                   |                                                                                                                                                                                | Markdown        | This document                                                                                                                                           |
| [RWorkflow_FishTrapsFoodSec.Rproj](https://github.com/bryanpgalligan/FishTrapsFoodSec/blob/master/RWorkflow_FishTrapsFoodSec.Rproj)     |                                                                                                                                                                                | RStudio Project | Sets working directory, source documents, etc. in RStudio                                                                                               |

## Data

### Trap Data

**Filepath**: `01_CleanData_Out/TrapData_Cleaned.csv`

**Date** of data collection: 2010-2019

Geographic **location** of data collection: southern coast of Kenya, northern coast of Tanzania

Information about **funding** sources that supported the collection of the data: data were collected by Wildlife Conservation Society, Mombasa, Kenya

**Restrictions** placed on the data: Please contact Tim McClanahan before using data.

Portions of this data have been **used by** Condy et al. (2015), Gomes et al. (2014), Mbaru et al. (2020), and Mbaru and McClanahan (2013).

Number of **variables**: 42

Number of **observations**: 27793

**Missing** **data** code: `NA`

#### Variable List

| Variable       | Notes                                                                                                         |
|----------------|---------------------------------------------------------------------------------------------------------------|
| Date           | Sampling date (d)                                                                                             |
| Month          | Sampling date (m)                                                                                             |
| Year           | Sampling date (yyyy)                                                                                          |
| Country        | Sampling location                                                                                             |
| Site           | Sampling location (landing site)                                                                              |
| Data collector | Name of researcher                                                                                            |
| TrapType       | Traditional or gated                                                                                          |
| GateCode       | Traditional (T) or gated (G) plus gap size if applicable (i.e., G2 = 2 cm gated trap)                         |
| TrapLocation   | Fishing location (different from landing site)                                                                |
| SoakTime_Days  | Days between fishing trip and previous set                                                                    |
| GapSize_cm     | Size of escape gap                                                                                            |
| Fisher         | Unique alphanumeric code to identify each fisher or combination of fishers                                    |
| TotalCrew      | Total number of fishers participating in trip                                                                 |
| TrapsOwned     | Number of traps owned by this fisher                                                                          |
| TrapsFished    | Number of traps fished on this trip                                                                           |
| TotalCatch_g   | Total catch for the trip in g                                                                                 |
| KiswahiliName  | Common name of fish species in Kiswahili                                                                      |
| Family         | Taxonomic family                                                                                              |
| Genus          | Taxonomic genus                                                                                               |
| Species        | Scientific name of species (*Genus species*)                                                                  |
| FishGroups     | Coarse groups for species (i.e., Rabbitfishes)                                                                |
| EnglishName    | Common name of fish species in English                                                                        |
| Bycatch        | Is this species considered bycatch? (Yes/No)                                                                  |
| FD_HC          | According to the fisher, will this fish be sold to a fish dealer (FD) or kept for household consumption (HC)? |
| Length_cm      | Total length (cm)                                                                                             |
| Depth_m        | Water depth where trap was set (m)                                                                            |
| Weight_g       | Mass of fish (g)                                                                                              |
| Price_KSH/kg   | Value of fish (Kenya shillings per kg)                                                                        |
| FunGr_Diet     | Categorization into coarse functional groups by species based on diet                                         |
| Latitude       | Fishing location (decimal degrees)                                                                            |
| Longitude      | Fishing location (decimal degrees)                                                                            |

## Built With

-   R version 4.1.2 (2021-11-01) -- "Bird Hippie"

-   RStudio 2021.09.1+372 "Ghost Orchid" Release (8b9ced188245155642d024aa3630363df611088a, 2021-11-08) for macOS

-   The following R packages:

    -   `AICcmodavg`

    -   `data.table`

    -   `dplyr`

    -   `magrittr`

    -   `readr`

    -   `readxl`

    -   `rfishbase`

    -   `stringr`

    -   `taxize`

    -   `tidyr`

## Links

-   The GitHub [repository](https://github.com/bryanpgalligan/FishTrapsFoodSec) for this project

## References

Condy, M., Cinner, J. E., McClanahan, T. R., & Bellwood, D. R. (2015). Projections of the impacts of gear-modification on the recovery of fish catches and ecosystem function in an impoverished fishery. *Aquatic Conservation: Marine and Freshwater Ecosystems*, *25*(3), 396–410. <https://doi.org/10.1002/aqc.2482>

FAO, IFAD, UNICEF, WFP, & WHO. (2021). *The state of food security and nutrition in the world 2021: Transforming food systems for food security, improved nutrition, and affordable healthy diets for all*. FAO. <https://doi.org/10.4060/cb4474en>

Gomes, I., Erzini, K., & McClanahan, T. R. (2014). Trap modification opens new gates to achieve sustainable coral reef fisheries: Escape gaps in African traditional trap fisheries. *Aquatic Conservation: Marine and Freshwater Ecosystems*, *24*(5), 680–695. <https://doi.org/10.1002/aqc.2389>

Mbaru, E. K., Graham, N. A. J., McClanahan, T. R., & Cinner, J. E. (2020). Functional traits illuminate the selective impacts of different fishing gears on coral reefs. *Journal of Applied Ecology*, *57*(2), 241–252. <https://doi.org/10.1111/1365-2664.13547>

Mbaru, E. K., & McClanahan, T. R. (2013). Escape gaps in African basket traps reduce bycatch while increasing body sizes and incomes in a heavily fished reef lagoon. *Fisheries Research*, *148*, 90–99. <https://doi.org/10.1016/j.fishres.2013.08.011>
