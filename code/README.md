# Code directory overview
All code is in the form of Jupyter notebooks. The `/code` directory contains the following subdirectories:
- `/code/24_09_28-test_scrape`: Code related to the pilot data collection
_ `/code/main_dataset`: Code related to the main data collection

## `/code/24_09_28-test_scrape`
- `/code/24_09_28-test_scrape/dataset_statistics.ipynb`: Generates very basic statistics about the pilot dataset
- `/code/24_09_28-test_scrape/influential_node_statistics.ipynb`: Computes ratio of messages in influential chats matching topic regular expressions
- `/code/24_09_28-test_scrape/topic_querying.ipynb`: Queries the dataset for messages matching topic regular expressions
- `/code/24_09_28-test_scrape/preprocessing.ipynb`: Preprocesses and filters the dataset for usage in rumor extraction

## `/code/main_dataset`
- `/code/main_dataset/dataset_statistics.ipynb`: Generates statistics about the main dataset: General, message distribution over time, language distribution
- `/code/main_dataset/preprocessing.ipynb`: Preprocesses and filters the dataset for usage in rumor tracking, including dividing into subsets
- `/code/main_dataset/anno_1_preparation.ipynb`: Prepares the first annotation set by sorting by similarity to topic representations
- `/code/main_dataset/anno_2_preparation.ipynb`: Prepares the second annotation set by filtering out off-topic samples and sorting by similarity to the positive samples from the first annotation
- `/code/main_dataset/anno_3_preparation.ipynb`: Prepares the third annotation set by filtering out off-topic samples and sorting by similarity to the positive samples from the second annotation
- `/code/main_dataset/packaging.ipynb`: Packages the annotation sets so they are ready for import into the annotation app
- `/code/main_dataset/anno_1_eval.ipynb`: Evaluates the first annotation iteration, including implementing the changes agreed on during the discussion. Also, contains an experiment for identifying tokens negatively correlated with the rumors.
- `/code/main_dataset/anno_2_eval.ipynb`: Evaluates the second annotation iteration, including implementing the changes agreed on during the discussion.
- `/code/main_dataset/anno_3_eval.ipynb`: Evaluates the third annotation iteration, including implementing the changes agreed on during the discussion.
- `/code/main_dataset/inter_annotator_agreement.ipynb`: Generates statistics about inter annotator agreement and rumor distribution in all annotation iterations
- `/code/main_dataset/release_dataset.ipynb`: Prepares the final dataset for release by removing unnecessary columns, removing unresolved differences and adding the label column