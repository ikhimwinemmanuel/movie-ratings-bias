# Data Analysis & Visualization Capstone Project

> *In 2015 a journalists said Fandango’s movie stars rating on their site looked a little too shiny and thus may be a strategy used to attract more customers to buy movie tickets. This is the sole motivation for this project. As I wanted to see for myself if this actually holds true.

---

## Project Brief

In 2015 FiveThirtyEight published an article suggesting Fandango’s displayed movie stars were **inflated**.  
So my goal here was to **replicate and extend** that investigation using Python and modern data-vizualization tools so that I could:

* quantify any bias in Fandango’s “Stars” and “Rating” columns relative to other platforms  
* surface **where** and **how big** these discrepancies are  
* finally communicate my findings through clear and interactive visuals

The guiding hypothesis for this project: “Determine if Fandango’s ratings in 2015 had a bias towards rating movies better to promote ticket sales”.

---

## Data Sources


`all_sites_scores.csv` = Scraped scores for every film with ≥30 fan reviews on Fandango plus Rotten Tomatoes, Metacritic, IMDb scores. Pulled 24 Aug 2015.


`fandango_scrape.csv` = Raw Fandango page scrape used to compute “Stars” vs “Rating”.

Original datasets are from [FiveThirtyEight’s open-data repo](https://github.com/fivethirtyeight/data).

---

## Methodology

1. **Cleaning & Normalisation**  
   * Standardised all ratings to a 0–5 scale (`_norm` columns).  
   * Re-combined individual site metrics into a tidy pandas dataframe.

2. **Exploratory Data Analysis**  
   * Several Distribution comparisons with KDE plots for each platform.  
   * Cross-site behaviour investigation.

3. **Hypothesis Tests**  
   * Paired tests Fandango vs RT critics/users, Metacritic critics/users, IMDb.

4. **Visual Storytelling**  
   * Matplotlib/Seaborn Vizualizations (histograms, density overlays, scatter plots).  

---

## Key Findings

* **Systematic Inflation** – Fandango’s displayed *Stars* average **0.37 points higher** than their underlying numeric *Rating*.  

* **Outlier Amplification** – Low-rated films on RT (< 2 / 5) still showed ≥ 3 stars on fandango site

* **Business Impact** – Inflation is most pronounced in the >3.5 star window; exactly where purchase decisions are most sensitive.

---

