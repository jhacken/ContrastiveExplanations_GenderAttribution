# What Triggers my Model? Contrastive Explanations Inform Gender Choices by Translation Models

## Included in this repo
Data
1. ``source_data-and-contrastive_translations``
-   English Source Data of natural, ambiguous gender sentences
-   OPUS Translations into German
-   Contrastive Gender Translations (manually crafted)
2. ``POS_data_relative20``
-   POS data, including POS labels for salient words of relative top 20% (Approach 4)
3. [REDACTED] Link to Human Annotations used for comparison in this study

Scripts
1. Computing contrastive explanations (using inseq)
-   Normalisation and pre-processing steps: ``pre_processing_saliency_analysis_contrastive_gender``
-   Measuring different 'thresholds': Approach 1, Approach 2, Approach 3, Approach 4
    ``saliency_analysis_contrastive-gender``
2. Linguistic Analysis (POS and Dependency Distance)
-  ``linguistic_analysis_of_salient_words``
3. Model-Human Comparison (for all Approaches, and for all annotators, comparatively also where min. 2 agree) 
[Link to annotation files in script REDACTED for anonymity until camera-ready version]


## OPUS MT Translations
To translate the EN Source sentences into German, we used [Helsinki OPUS MT en-de](https://huggingface.co/Helsinki-NLP/opus-mt-en-de), as below

``pip uninstall transformers -y``

``pip install transformers accelerate bitsandbytes``

``from transformers import pipeline
pipe_Helsinki = pipeline("translation", model="Helsinki-NLP/opus-mt-en-de")``
