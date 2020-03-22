# covid-spain

Data from published updates by the Spanish Ministry of Health, detailing the number of diagnosed cases, ICU admissions and deaths, by Autonmous Region (Comunidad Autónoma).

**Up-to-date as of**: 22/03/2020 at 14h

## Read first

* The data has been extracted from the "daily" updates published by the Spanish Ministry of Health [in this webpage](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm)
* The data is published in an [unhelpful PDF format](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/documentos/Actualizacion_46_COVID-19.pdf), so I used the open-source PDF-extraction tool [Tabula](https://github.com/tabulapdf/tabula) to extract the tabular data into CSV formatted files.
* *Warning*: The format of the published data has varied several times, so in some cases I had to manually update the extracted CSVs to achieve some level of consistency in their format. I have not altered the values in any way (unless they were altered by accident during the extraction process)

## Dataset

* [`extracted_data/`](extracted_data/): Raw data as extracted by Tabula
* [`consolidated/`](consolidated/): Consolidated `diagnosed.csv`, `icu.csv` and `deaths.csv` data from the data in [`extracted_data/`](extracted_data/).

## How to contribute

1. Visit the  [Health Ministry webpage](https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm) and click on the link "Actualización nºXX: enfermedad por SARS-CoV-2 (COVID-19)"
2. Download the PDF file to your local host
3. Install [Tabula](https://github.com/tabulapdf/tabula) and follow the instructions to extract the table containing the daily update
4. Extract the data to a CSV, double check the format doesn't change and
5. Run [notebooks/000_consolidate_data.ipynb](notebooks/000_consolidate_data.ipynb) to update the consolidated files
6. Inspect the data to make sure it makes sense [notebooks/001_plots.ipynb](notebooks/001_plots.ipynb)
7. Commit and push the resulting consolidated files

