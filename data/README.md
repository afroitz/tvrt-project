# Data directory overview
The `/data` directory contains four subdirectories: 
- `/data/24_09_28-test_scrape`: data related to the pilot data collection
- `/data/main_dataset`: all data derived from the main data collection
- `/data/annotation_results`: the results of the annotation process
- `/data/tasks`: the tasks used in the annotation process

## `/data/24_09_28-test_scrape`
- `/data/24_09_28-test_scrape/24_09_28-test_scrape-raw.csv`: The raw pilot dataset
- `/data/24_09_28-test_scrape/24_09_28-test_scrape-prepro.csv`: The preprocessed and filtered dataset
- `/data/24_09_28-test_scrape/24_09_28-test_scrape-additional.csv`: The unfiltered dataset, used for resolving reply threads

## `/data/main_dataset`
- `/data/main_dataset/main_dataset.csv`: The raw main dataset
- `/data/main_dataset/main_dataset-prepro.csv`: The preprocessed and filtered dataset
- `/data/main_dataset/main_dataset-additional.csv`: The unfiltered dataset, used for resolving reply threads
- `/data/main_dataset/main_dataset-{FROM_INDEX}-{TO_INDEX}.csv`: Slices of the preprocessed dataset, used for annotation
- `/data/main_dataset/main_dataset-additional-{FROM_INDEX}-{TO_INDEX}.csv`: Data needed for resolving reply threads for each slice
- `/data/main_dataset/anno_1_set-{TOPIC}.csv`: Datasets for the first annotation iteration, one for each of the four topics. Only the first 150 samples from each were annotated.
- `/data/main_dataset/anno_2_set.csv`: Annotation set for the second iteration.
- `/data/main_dataset/anno_2_set-additional.csv`: Annotation set for two new rumors in the second iteration.
- `/data/main_dataset/anno_3_set.csv`: Annotation set for the third iteration.

## `/data/annotation_results`
- `/data/annotation_results/anno_{ITERATION}`: Directories with the JSON annotation files exported from the annotation app for each iteration. Each contains one directory per annotator with one or multiple annotation files each.
- `/data/annotation_results/anno_01_annotated.csv`: The annotated dataset from the first iteration
- `/data/annotation_results/anno_02_annotated.csv`: The annotated dataset from the second iteration
`/data/annotation_results/anno_02_positive-cleaned.csv`: Positive samples from the second iteration with message footers removed. Used for preparing the third iteration set.
- `/data/annotation_results/anno_03_annotated.csv`: The annotated dataset from the third iteration
- `/data/annotation_results/tvrt_dataset.csv`: The final dataset with the annotations


## `/data/tasks`
- `/data/tasks/task_v1.json`: The task for the first annotation iteration
- `/data/tasks/task_v2.json`: The task for the second and third annotation iteration