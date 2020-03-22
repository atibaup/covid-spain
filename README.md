# covid-spain

Data from published updates by the Spanish Ministry of Health, detailing the number of diagnosed cases, ICU admissions and deaths, by Autonmous Region (Comunidad Autónoma).

Up-to-date as of: 22/03/2020 at 14h

## Read first

* The data has been extracted from the "daily" updates published by the Spanish Ministry of Health (in this webpage)[https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/situacionActual.htm]
* The data is published in an (unhelpful PDF format)[https://www.mscbs.gob.es/profesionales/saludPublica/ccayes/alertasActual/nCov-China/documentos/Actualizacion_46_COVID-19.pdf], so I used the open-source PDF-extraction tool (Tabula)[https://github.com/tabulapdf/tabula] to extract the tabular data into CSV formatted files.
* *Warning*: The format of the published data has varied several times, so in some cases I had to manually update the extracted CSVs to achieve some level of consistency in their format. I have not altered the values in any way (unless they were altered by accident during the extraction process)

## Dataset

* (`processed/`)[processed/]: Raw data as extracted by Tabula
* (`consolidated/`)[consolidated/]: Consolidated `diagnosed.csv`, `icu.csv` and `deaths.csv` data from the data in (`processed/`)[processed/].


