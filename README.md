# wikihow-connective-insertions

A dataset of **connective insertions** observed in the revision history of instructional texts from WikiHow.

---

##  Data Description

This dataset is based on the revision histories of WikiHow articles, extracted from the [wikiHowToImprove dataset](https://github.com/irshadbhat/wikiHowToImprove). WikiHow is a collaboratively edited platform offering step-by-step guides for everyday tasks, and each article contains a rich revision history created by various contributors.

**We use the same train/dev/test split as in the original `wikiHowToImprove` dataset**.

The dataset consists of two components:

### 1. WikiHow Connective Insertions

This part includes revisions in which a **discourse connective** (e.g., *"However"*, *"As a result"*) has been inserted at the beginning of a sentence. These insertions often make implicit relationships in the text more explicit and serve as clarifications or improvements for coherence.


### 2. Crowdsourced Annotations

This part includes **human judgments** collected via crowdsourcing on a selection of the connective insertions. Each revision was evaluated for **plausibility** in its context.

For each development and test split, the following TSV file is provided:

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


