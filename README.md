# RPA

This repo attempts to compare different approaches to detect topics in political and media content, and compare their effectiveness.

---
This repo contains the following elements:

-  Data preparation
    - Prep and combine data from coders, newspapers and parlementairly questions
- Evaluation of classification accuracy of these documents:
	- Dictionary approach, using word lists constructed in [here](https://www.almendron.com/tribuna/wp-content/uploads/2017/05/CAP2013v2.pdf)
	- 'Classic' Supervised Machine Learning
	- CNN models using pretrained word embedding models trained on Dutch news and parliamentary questions.

We extend our dataset with the newspaper dataset reported here: https://journals.sagepub.com/doi/10.1177/0002716215569441

---
## Python scripts:

### analysis

#### run_classifier.py

### helpers / dataprep:

In the folder `helpers/`, you find helpers to parse the parliamentary questions and to scripts to prep the annotated data and merge with the original text files (newspapers + kamervragen)

`kamervragen_parser.py` : use this script to parse the parliamentary questions

`prep_annotated_data.py` : this scrips prepares the raw file with annotated data (derived from Qualtrics).
`prep_kamervragen_data.py` : this script merges the annotated data with the text of the newspaper articles that were annotated
`prep_newspaper_data.py` : this script merges the annotated data with the parsed questions belonging to parliamentary questions


## Commands:

run parser for kamervragen:

```
python3 helpers/kamervragen_parser.py --data_path ~/Dropbox/kamervragen-xml/  --output ~/surfdrive/uva/projects/RPA_KeepingScore/data/

```
