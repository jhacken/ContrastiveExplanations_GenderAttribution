# What Triggers my Model? Contrastive Explanations Inform Gender Choices by Translation Models

## Included in this repo
Data
1. ``source_data-and-contrastive_translations``
-   English Source Data of natural, ambiguous gender sentences
-   OPUS Translations into German and Spanish
-   Contrastive Gender Translations (manually crafted) both for German and Spanish
2. ``POS_data_relative15_DE``
-   For German: POS data, including salient words and POS labels of relative top 15% (Approach 4)
3. ``POS_data_relative15_ES``
-   For Spanish: POS data, including salient words and  POS labels of relative top 15% (Approach 4)
4. ``Annotations_all_majority`` & ``All_annotations_duplicates_removed_majority_min_two_agree``
- Human Annotations used for comparison in this study

Scripts
1. Computing contrastive explanations (using inseq)
-   Normalisation and pre-processing steps: ``pre_processing_saliency_analysis_contrastive_gender``
-   Measuring different 'thresholds': Approach 1, Approach 2, Approach 3, Approach 4
    ``saliency_analysis_contrastive-gender``
2. ``model-annotations_comparison_v2``
- Model-Human Comparison (for all Approaches, and for all annotators, comparatively also where min. 2 agree) 
3. ``model_human_overlap_DE_ES``
- Model-Human Overlap Analysis, including Linguistic Analysis (POS and Dependency Distance)


## OPUS MT Translations
To translate the EN Source sentences into German, we used [Helsinki OPUS MT en-de](https://huggingface.co/Helsinki-NLP/opus-mt-en-de) and into Spanish [Helsinki OPUS MT en-es](https://huggingface.co/Helsinki-NLP/opus-mt-en-es), as below

``pip uninstall transformers -y``

``pip install transformers accelerate bitsandbytes``

``from transformers import pipeline
pipe_Helsinki = pipeline("translation", model="Helsinki-NLP/opus-mt-en-de")``

The translation pipeline is also included in the pre_processing script file for reference.
