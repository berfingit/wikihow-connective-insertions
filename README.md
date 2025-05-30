# MisDR dataset

A dataset of **connective insertions** observed in the revision history of instructional texts from WikiHow.

---

##  Data Description

This dataset is based on the revision histories of WikiHow articles, extracted from the [wikiHowToImprove dataset](https://github.com/irshadbhat/wikiHowToImprove). WikiHow is a collaboratively edited platform offering step-by-step guides for everyday tasks, and each article contains a rich revision history created by various contributors.

**We use the same train/dev/test split as in the original `wikiHowToImprove` dataset**.

The dataset consists of two components:

### 1. WikiHow Connective Insertions

This part includes revisions in which a **discourse connective** (e.g., "However", "As a result") has been inserted at the beginning of a sentence, without any other changes between the original and revised versions. These insertions help make previously implicit discourse relations explicit, serving as clarifications or coherence improvements.

For each data split (i.e., **train**, **dev**, and **test**), the following TSV file is provided:

insert_connective_begin_{split}_with_context.tsv

Each file contains the following columns:

- `Article.Filename`: Name of the WikiHow article file  
- `Article.Original-section`: Section where the original sentence appears  
- `Sentence.Original`: The sentence before the revision  
- `Article.Revision-section`: Section where the revised sentence appears  
- `Sentence.Revision`: The sentence after the connective was inserted  
- `Sentence.Edits`: Type of edits made (in this case, insertion)  
- `Sentence.Context-before`: Text that precedes the revision  
- `Sentence.Context-after`: Sentence that follows the revision  



### 2. Crowdsourced Annotations

This part includes **human judgments** collected via crowdsourcing on a selection of the connective insertions. Each revision was evaluated for **plausibility** in its context.

For development and test splits, the following TSV file is provided:

{split}_crowdsourced_annotations.tsv

Each file contains the following columns:

- `Input.Title`: Title of the WikiHow article  
- `Input.ContextBefore`: Text immediately preceding the connective  
- `Input.ContextAfter`: Text immediately following the connective  
- `Input.Selected_Connectives`: The connective inserted  
- `Input.Sent`: The full sentence after revision  
- `Input.ID`: Unique identifier for the instance  
- `label_aggregated`: Aggregated human plausibility rating  

---

## License

This dataset is distributed under the [Creative Commons Attribution-NonCommercial-ShareAlike 3.0 License (CC BY-NC-SA 3.0)](https://creativecommons.org/licenses/by-nc-sa/3.0/), in accordance with the licensing of the original WikiHow content.

---

## Contact

If you have any questions about this dataset, feel free to contact:

📧 **berfin.aktas@utn.de**

---

## Citation

If you use this dataset in your research, please cite the following paper:

> **Berfin Aktaş and Michael Roth.** 2025. *Clarifying Underspecified Discourse Relations in Instructional Texts*. Findings of the Association for Computational Linguistics: ACL 2025. Association for Computational Linguistics, Vienna, Austria. *(To appear)*


