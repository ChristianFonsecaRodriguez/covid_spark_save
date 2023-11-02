# CSV TO PARQUET SAVING PROCESS FOR COVID-19 Dataset
Link: https://www.kaggle.com/datasets/imdevskp/corona-virus-report

## Resources
I'm using a docker image for pyspark: https://hub.docker.com/r/jupyter/pyspark-notebook

## Entry Files
The dataset have 6 files with \*.csv extension (added in data/raw directory<sup>[1]</sup>).
- country_wise_latest.csv
- covid_19_clean_complete.csv
- day_wise.csv
- full_grouped.csv
- use_county_wise.csv
- worldometer_data.csv

## Output Files
The process for saving CSV files as Parquet employs both RDDs and spark.read to load each file, with the sole purpose of comparing these different techniques.
- I'm using classes to differentiate between various processes, such as schema definition and renaming.
- The main class is called BaseDataProcessor, which requires only three parameters for instantiation: name (the name of the process, which enables the use of various methods from other classes), file_path_input (the name of the CSV file including the extension), and file_path_output (the output directory where the Parquet partitions are stored).

## DER
![DER for output parquets](/images/der.png)

## Notes
[1] I'm uploading data in GitHub with the sole purpose to perform tests quickly, by only downloading the entire repository, I'm aware that is a bad practice. 





