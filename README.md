# wikihow-connective-insertions

A dataset of **connective insertions** observed in the revision history of instructional texts from WikiHow.

---

## 📄 Data Description

This dataset is based on the revision histories of WikiHow articles, extracted from the [wikiHowToImprove dataset](https://github.com/irshadbhat/wikiHowToImprove). WikiHow is a collaboratively edited platform offering step-by-step guides for everyday tasks, and each article contains a rich revision history created by various contributors.

👉 **We use the same train/dev/test split as in the original `wikiHowToImprove` dataset**, for consistency and comparability.

The dataset consists of two components:

### 1. WikiHow Connective Insertions

This part includes revisions in which a **discourse connective** (e.g., *"However"*, *"As a result"*) has been inserted at the beginning of a sentence. These insertions often make implicit relationships in the text more explicit and serve as clarifications or improvements for coherence.

These revisions can be useful for studying:
- Discourse structure and coherence
- Collaborative text improvement
- Implicit relation clarification

### 2. Crowdsourced Annotations

This part includes **human judgments** collected via crowdsourcing on a selection of the connective insertions. Each revision was evaluated for **plausibility** in its context.

For each development and test split, the following TSV file is provided:

