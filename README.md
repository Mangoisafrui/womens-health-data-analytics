# womens-health-data-analytics
Global analysis of women's mental health disparities and gender bias in medical diagnosis
# Overlooked & Underserved
## A Global Analysis of Women's Mental Health Disparities

**Author:** Christelle Denny
**Program:** IT Data Analytics — Nova Scotia Community College (NSCC)
**Date:** Summer 2026

---

## Project Overview

This project investigates how mental health outcomes among women vary across countries at different levels of socioeconomic development, and examines the socioeconomic and gender equality factors that correlate most strongly with these disparities. Using seven publicly available global datasets, the analysis produces a reproducible, well-documented data analytics project covering 150 countries across the period 2000–2021.

A central argument of this project is that recorded mental health data reflects **detection capacity** as much as genuine burden — countries with better healthcare infrastructure and lower stigma record higher rates, while countries where women face the greatest structural inequality have the least capacity to measure their suffering.

---

## Research Question

> *"How do mental health disparities among women vary across developed, developing, and underdeveloped nations, and to what extent do underreporting, stigma, and lack of sex-disaggregated data obscure the true burden of mental illness in women globally?"*

---

## Key Findings

- **Latin America and the Caribbean** recorded the highest combined depression and anxiety rates globally
- **East Asia and Pacific** consistently recorded the lowest rates — consistent with cultural stigma suppressing reporting
- **GDP per capita** showed a significant positive correlation with recorded depression rates (r=0.206, p<0.001) — supporting detection bias hypothesis
- **Gender inequality and psychiatrist density** showed the strongest relationship in the dataset (r=-0.74) — countries with highest inequality have fewest mental health resources
- **COVID-19** caused a larger single-year increase in depression rates than the preceding 19 years combined
- **38 countries** showed disproportionately high suicide rates relative to recorded depression — potential evidence of underreporting
- **Low income countries** recorded the highest depression DALYs despite not having the highest prevalence — each case carries greater burden where treatment is least accessible

---

## Datasets Used

| Dataset | Source | Purpose |
|---|---|---|
| GBD 2021 Prevalence | IHME | Depression & anxiety rates among women 15–49 |
| GBD 2021 DALYs | IHME | Disability burden from mental illness |
| GBD 2021 Suicide | IHME | Female suicide rates |
| World Bank Classifications | World Bank | Country income group classifications |
| UNDP Gender Inequality Index | UNDP | Gender equality scores by country |
| WHO Psychiatrists per 100k | Our World in Data / WHO | Healthcare access indicator |
| World Bank GDP per Capita | World Bank | Economic development indicator |

All datasets are publicly available and free to access.

---

## Repository Structure

```
womens-health-data-analytics/
│
├── Raw Data/
│   ├── GBD_2021/
│   ├── World_Bank/
│   ├── GII_UNDP/
│   └── WHO_Atlas/
│
├── Clean Data/
│   └── master_dataset.csv
│
├── Notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda_analysis.ipynb
│   ├── 03_correlation_analysis.ipynb
│   ├── 04_prevalence_daly_analysis.ipynb
│   ├── 05_trend_analysis.ipynb
│   └── 06_visualizations.ipynb
│
├── Visualizations/
│   ├── 01_rates_by_income_group.png
│   ├── 02_rates_by_region.png
│   ├── 03_top_bottom_10_countries.png
│   ├── 04_diagnosis_gap_mismatch.png
│   ├── 06_gii_depression_by_income.png
│   ├── 07_gdp_depression_scatter.png
│   ├── 08_correlation_heatmap.png
│   ├── 09_prevalence_vs_dalys.png
│   ├── 10_global_trend.png
│   ├── 11_trend_by_income.png
│   ├── 12_trend_by_region.png
│   ├── 13_world_map_depression.html
│   ├── 14_world_map_anxiety.html
│   ├── 15_world_map_gii.html
│   └── 16_world_map_psychiatrists.html
│
└── README.md
```

---

## Tools & Technologies

- **Python 3.11** — primary programming language
- **Pandas** — data cleaning, merging, analysis
- **NumPy** — numerical operations
- **Matplotlib / Seaborn** — static visualizations
- **Plotly** — interactive choropleth world maps
- **SciPy** — Pearson correlation analysis
- **Jupyter Notebooks** — development environment
- **VS Code** — code editor
- **GitHub** — version control and portfolio hosting

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/Mangoisafrui/womens-health-data-analytics.git
```

2. Install required libraries:
```bash
pip install pandas numpy matplotlib seaborn plotly scipy openpyxl
```

3. Open notebooks in order starting with `01_data_cleaning.ipynb`

4. Update file paths in each notebook to match your local directory

---

## Limitations

- Mental health data reflects recorded diagnoses — not true prevalence
- Low income countries represent only 12% of the dataset
- GBD estimates are modelled — not direct measurements
- Significant multicollinearity exists between GII, GDP, and psychiatrist density
- No causal claims are made — all findings are correlational

See the full report for complete limitations discussion.

---

## License

MIT License — free to use with attribution.

---

*This project was completed independently as part of a self-directed summer research initiative during the IT Data Analytics program at NSCC, Halifax, Nova Scotia.*
