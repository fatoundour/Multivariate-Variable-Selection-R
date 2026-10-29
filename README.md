# Multivariate Variable Selection in R — Proteomics (FH)

**Academic team project** — Master 2, Université Paris Cité, course *Questions de sciences des données*.

## Objective

Study how **temperature** (Low, Medium, Elevated), **seed imbibition stage** (DS, EI, LI) and their combinations relate to protein abundance in freshly harvested seeds (FH). The analysis uses multivariate linear modeling and variable selection to account for dependencies across protein measurements.

## Method

- Explore and preprocess proteomics data (log transformation, standardization, PCA and visualizations).
- Build the multivariate linear model `Y = XB + E` using temperature × stage experimental groups.
- Investigate residual covariance and whitening using **MultiVarSel**.
- Apply stability selection to identify protein–condition associations.
- Re-estimate and interpret selected effects, with heatmaps and boxplots.

## Results

The original report describes **27 samples** with **494 protein measurements**. With a stability-frequency threshold of **0.93**, the reported analysis retains **223 protein–experimental-condition pairs** (not 223 distinct proteins). The higher-temperature DS and LI groups feature prominently among selected associations. Results are exploratory, given the small sample size.

## Files

- `Analyse_proteome_FH.qmd` — original Quarto source with R code and analysis.
- `.gitignore` — excludes course-provided data and locally generated result files.

## Data availability & reproducibility

The dataset `Table_proteome_FH_all.csv` was supplied by the course instructor and **is not redistributed in this public repository**. The cached selection results (`Freqs_FH.rds`) are also omitted pending confirmation that derivative data can be shared. To rerun, obtain the dataset through an authorized source, place it alongside the Quarto file, and review the local paths in the script before rendering. R and packages used in the source, including `MultiVarSel`, are required. **End-to-end reproduction has not been independently verified** for this public version.

## Credits

**Team project:** Adam Aabadli, Fatoumata Ndour, Myriam Abouda. The data and course framework were provided by the teaching staff; this repository does not claim authorship of the MultiVarSel package or of the underlying dataset.

## Note

For educational and portfolio purposes. Selected associations should not be interpreted as proof of biological causation.
