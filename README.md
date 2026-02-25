# dhd2026
![version](https://img.shields.io/badge/version-1.0.0-blue)
[![License: GPL v3](https://img.shields.io/badge/License-GPL_v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.html)
[![DOI](https://zenodo.org/badge/DOI/null.svg)](https://doi.org/null)

This is a repository containing the data and code for our poster ["Kombinieren statt neu trainieren. Zur automatisierten Erkennung diegetischen räumlichen Vokabulars mit Hilfe existierender Annotationen und Classifier"](https://doi.org/10.5281/zenodo.18702911) addressing the recognition of diegetic spatial vocabulary presented at [DHd2026 in Vienna](https://dhd2026.digitalhumanities.de/).

## Content
### Folders and files
- source files:
  - plain text source files for CS1 and LLPro annotations in `source_files/txt`:
    - `DEU19_001_2-3-5.txt`
    - `DEU19_030_1-1-1.txt`
    - `DEU19_058_14.txt`
  - CS1 annotation data as `.tsv` files in `source_files/cs1-data`:
    - `CANSpiN-deu-19_001_2-3-5.tsv`
    - `CANSpiN-deu-19_030_1-1-1.tsv`
    - `CANSpiN-deu-19_058_14.tsv`
  - LLPro annotation data containing the EvENT annotation as `.tsv` files in `source_files/llpro-data`:
    - `DEU19_001_2-3-5.tsv`
    - `DEU19_030_1-1-1.tsv`
    - `DEU19_058_14.tsv`
- results:
  - merged annotations as `.csv` files in `results/merged_annotations`:
    - `DEU19_001_2-3-5.csv`
    - `DEU19_030_1-1-1.csv`
    - `DEU19_058_14.csv`
  - manual evaluations of the merged annotations as `.csv` files in `results/manual_evaluations`:
    - `DEU19_001_2-3-5.csv`
    - `DEU19_030_1-1-1.csv`
    - `DEU19_058_14.csv`
  - manual evaluation statistics as `.json` files in `results/manual_evaluation_statistics`:
    - `DEU19_001_2-3-5.json`
    - `DEU19_030_1-1-1.json`
    - `DEU19_058_14.json`
    - `DEU20_021_1.json`
- notebook for generating tsv files in which the CS1 and EvENT annotations for each chapter are merged:
  - `merge_annotations.ipynb`
- notebook to get statistics of evaluated merged `.csv` files:
  - `get_manual_evaluation_statistics.ipynb`
- bibliography of the poster:
  - `bibliography.bib`

### Corpus overview
For this case study we use one chapter each of the following german 19th and 20th century novels:
 - Ernst Adolf Willkomm: *Weisse Sclaven oder die Leiden des Volkes* (1845) \[2nd part, 3rd book, 5th chapter\],
 - Gustav Freytag: *Die verlorene Handschrift* (1864) \[1st part, 1st book, 1st chapter\],
 - Marie von Ebner-Eschenbach: *Lotti, die Uhrmacherin* (1880) \[14th chapter\],
 - Uwe Johnsons *Zwei Ansichten* (1965) \[1st chapter\].

The data originates from the corpora of the [European Literary Text Collection (ELTeC)](https://github.com/COST-ELTeC) and the [Complete Works of Uwe Johnson project (CWUJ)](https://www.germanistik.uni-rostock.de/en/forschung/uwe-johnson/werkausgabe/). For legal reasons, the textual data from the 20th century can not be published. For Uwe Johnsons *Zwei Ansichten* we only provide the manually compiled evaluation statistics.

| ID | Title | Author | Year | Token | Source |
|----|-------|--------|------|-------|--------|
| DEU19_001_2-3-5 | Weisse Sclaven oder die Leiden des Volkes | Willkomm, Ernst Adolf | 1845 | 6539 | ELTeC-deu |
| DEU19_030_1-1-1 | Die verlorene Handschrift | Freytag, Gustav | 1864 | 7179 | ELTeC-deu |
| DEU19_058_14 | Lotti, die Uhrmacherin | Ebner-Eschenbach, Marie von | 1880 | 3959 | ELTeC-deu |
| DEU20_021_1 | Zwei Ansichten | Johnson, Uwe | 1965 | 744 | CWUJ |

## Annotations
We use the [**LLPro** pipeline](https://aclanthology.org/2023.konvens-main.3) containing the **EvENT** classifier for creating event annotations. The data for **CS1** comes from manual annotations. The **EvENT** annotation guideline (v1) was published [by Evelyn Gius and Michael Vauth](https://doi.org/10.5281/zenodo.5078175). The **CANSpiN.CS1** annotation guideline (v1.1.0) is available [here](https://doi.org/10.5281/zenodo.10437030).

## Usage
The notebooks (`.ipynb` files) enables the user to reproduce crucial steps we have performed in our analysis. The resulting files are created in a new folder `/notebook_output`. It is not necessary to execute the notebooks, if you wish to see the analysis results only. In this case, see our poster and the content of the `/results` folder.

## Licenses
The original texts are in the public domain, with the exception of the German-language novels from the 20th century, which are protected by copyright. The latter are therefore not available here.

We publish the annotations under [Creative Commons Attribution International 4.0 licence](https://creativecommons.org/licenses/by/4.0/) and the notebooks under [GNU General Public License 3](https://www.gnu.org/licenses/gpl-3.0.html).
