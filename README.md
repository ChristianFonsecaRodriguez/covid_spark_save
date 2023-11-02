# CSV TO PARQUET SAVING PROCESS FOR COVID-19 Dataset
Link: https://www.kaggle.com/datasets/imdevskp/corona-virus-report

## Entry Files
The dataset have 6 files with \*.csv extension (added in data/raw directory<sup>[1]<sup>).
- country_wise_latest.csv
- covid_19_clean_complete.csv
- day_wise.csv
- full_grouped.csv
- use_county_wise.csv
- worldometer_data.csv

## Output Files
The process for save the csv files to parquet, uses RDD and spark.read for load each file (only for compare theses different techniques).
- I'm using classes to diferenciate different processes, such as schema definitions, renaming, etc.
- The principal class is named BaseDataProcessor, where this only needs 3 parameters to construct it: name (name for the process, that allows to use some different methos from the other classes), file_path_input (csv file name with extension), file_path_output (output directoria, where parquet partitions are saved).


## Notes
[1] I'm adding data in GitHub with the sole purpose to perform tests quickly, by only downloading the entire repository, I'm aware that is a bad practice. 





