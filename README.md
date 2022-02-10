# Python Code for Peptide Sequencing of plasma after Chlorine Exposure
## Background
Blood plasma was exposed in vitro to various concentrations of chlorine gas. After sample preparation and digestion, the peptides were measured by LC-HRMS/MS. The raw data was analyzed using Peaks (R) X+ Software. The identified peptides were exported in a .csv datafile and analyzed by Python 3.9.5.

## Aim
We aim to find specific chlorinated peptides that might serve as promising biomarkers for verification of human exposure to chlorine.

## Considerations
1. In the Peaks software three types of variable post-translational modifications (PTMs) were selected for database search: single chlorination, dichlorination and nitration of tyrosine. Besides non-chlorinated peptides, only single and double chlorination on the Tyrosine (Y) amino acids were found and exported.)
3. Duplicates were dropped if peptide sequence and RT were equal, entries with the largest area were kept.
4. Areas under a specific threshold were dropped. 
5. Peptides with a charge (z) lower than 2 were dropped.
6. Peptides of non-human origin were removed.
7. Only peptides were selected for further research that were both present in the blank and highly exposed samples and with enhanced chlorination in the latter.

## Installation
Download Jupyter Notebook per instructions on https://gerritjandebruin.nl/jupyter.html.
Then install the following environment:
```bash
conda create -y -n chlorotyrosines python=3.9.5 pandas seaborn tqdm jupyter jupyter_contrib_nbextensions
conda activate chlorotyrosines
jupyter nbextension enable toc2/main
```
When this is installed, you can run the jupyter notebook with `jupyter notebook' and open [Peptide Sequencing of Plasma after Chlorine Exposure.ipynb](Peptide Sequencing of Plasma after Chlorine Exposure.ipynb).

If this does not work, you can lookup the specific package versions in [environment.yml](environment.yml).

## Data
The data is not made publicly available due to safety considerations, but can be made available on request.

## Files
- The notebook file provides all relevant code for the publication.

## Publication
Elucidation of chlorinated tyrosine adducts in blood plasma as selective biomarkers of chlorine exposure. Mirjam de Bruin-Hoegée, Irene M. van Damme, Tomas van Groningen, Debora van der Riet-van Oeveren, Daan Noort, Arian C. van Asten. Under submission.

## Contributing
The analyses were performed by [Mirjam de Bruin](https://forensicscientist.nl) and [Gerrit-Jan de Bruin](https://gerritjandebruin.nl).
