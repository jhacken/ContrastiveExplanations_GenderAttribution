# Repo to include scripts and data for LREC Submission

Submitted paper: "What Triggers my Model? Contrastive Explanations Inform Gender Choices by Translation Models"

## Included in this repo
- Data
-   English Source Data of natural, ambiguous gender sentences
-   OPUS Translations into German
-   Contrastive Gender Translations (manually crafted)
-   Link to Human Annotations used for comparison in this study
- Scripts
-   Translating using Helsinki-OPUS-EN-DE
-   Using inseq, computing contrastive explanations
-   Normalisation and pre-processing steps
-   Measuring different 'thresholds': Approach 1, Approach 2, Approach 3, Approach 4
-   Model-Human Comparison (example for one approach)


## OPUS MT Translations
To translate the EN Source sentences into German, we used the [Helsinki OPUS MT en-de](https://huggingface.co/Helsinki-NLP/opus-mt-en-de), as below

``!pip uninstall transformers -y``
``!pip install transformers accelerate bitsandbytes``

``from transformers import pipeline
pipe_Helsinki = pipeline("translation", model="Helsinki-NLP/opus-mt-en-de")``
