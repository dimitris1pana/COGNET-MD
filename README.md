---
license: cc-by-nc-nd-4.0
size_categories:
- n<1K
language:
- en
pretty_name: cognetmd
tags:
- medical
- MCQ
---

# Dataset Card for Dataset Name
Cognitive Network Evaluation Toolkit for Medical Domains (COGNET-MD) 


## Dataset Details
Testing the ability of LLMs in finding more than one correct choices in a medical domains, where a penalty is added for incorrect ones, simulating real world evaluating scenarios 
of medical students.
Large Language Models (LLMs) constitute a breakthrough state-of-the-art Artificial Intelligence (AI) technology which is rapidly evolving and promises to aid in medical diagnosis either by assisting doctors or by simulating a doctor's workflow in more advanced and complex implementations. In this technical paper, we outline Cognitive Network Evaluation Toolkit for Medical Domains (COGNET-MD), which constitutes a novel benchmark for LLM evaluation in the medical domain. Specifically, we propose a scoring-framework with increased difficulty to assess the ability of LLMs in interpreting medical text. The proposed framework is accompanied with a database of Multiple Choice Quizzes (MCQs). To ensure alignment with current medical trends and enhance safety, usefulness, and applicability, these MCQs have been constructed in collaboration with several associated medical experts in various medical domains and are characterized by varying degrees of difficulty. The current (first) version of the database includes the medical domains of Psychiatry, Dentistry, Pulmonology, Dermatology and Endocrinology, but it will be continuously extended and expanded to include additional medical domains.

### Dataset Description
Cognitive Network Evaluation Toolkit for Medical Domains (COGNET-MD) consists of 542 datapoints of domain-specific questions (MCQs) with one or more correct choices/answers.

Version 1 includes MCQs in Dentistry , Dermatology , Endocrinology , Psychiatry and Pulmonology. We have included a scoring system as a python code for benchmarking purposes (see associated files).
See #Uses
The dataset can be used to assess the model’s ability to infer relationships between specialties and knowledge spaces. Thus it can be analyzed either as a whole, encompassing all included specialties-full Dataset, partially or it can be narrowed down to focus on a specific medical domain-specialty.

- **Curated by:** Dimitrios P. Panagoulias, Persephone Papatheodosiou, Anastasios P. Palamidas, Mattheos Sanoudos, Evridiki Tsoureli-Nikita, Maria Virvou, George A. Tsihrintzis
- **Language(s) (NLP):** English
- **License:** https://creativecommons.org/licenses/by-nc-nd/4.0/

### Dataset Sources

- **Paper:** COGNET-MD, an evaluation framework and dataset for Large Language Model benchmarks in the medical domain
- **Code** Included in Files
-  Or direct dl with with datasets (pip install datasets) 
  ```python
from datasets import load_dataset
dataset = load_dataset('DimitriosPanagoulias/COGNET-MD', split='train')
```

## Uses
Scoring should be: 
* Partial Credit: At least one correct answer equals to a half point - 0.5.
* Full Credit: To achieve full points depending on difficulty either all correct answers must be selected and no incorrect ones or a correct response gets the full credit, equals to 1 point.
* Penalty for Incorrect Answers: Points are deducted for any incorrect an- swers selected. -(minus) 0.5 point for each incorrect answer selected.

| Specialty   | Beta    | Production    |
|:------------|:------------|:------------|
| Partial Credit(0.5) | Partial Credit(0.5) | Partial Credit(0.5) |
| Full Credit(P+0.5=1) | Full Credit(P+0.5=1) |Full Credit(P+0.5=1) |
| MistakePenalty (0.5) | MistakePenalty (0.5) | MistakePenalty (0.5) |
|Domain-Specific|50% per specialty|full Dataset|


## Dataset Structure
To be added

## Dataset Creation
2024
### Curation Rationale
This is a dataset curated by domain-experts.
For a score to be valid and be added in the COGNET-MD’s leader-boards the developers, should clearly state model used, add a short model description and use case scenario used, 
as described in the previous section. In the following Benchmark Card two examples are presented:
Benchmark Card should include: 
MODEL -- Description -- Domain -- Difficulty COGNET-MD VERSION 


## Citation

COGNET-MD, an evaluation framework and dataset for Large Language Model benchmarks in the medical domain

**BibTeX:**

@misc{panagoulias2024cognetmd,
      title={COGNET-MD, an evaluation framework and dataset for Large Language Model benchmarks in the medical domain}, 
      author={Dimitrios P. Panagoulias and Persephone Papatheodosiou and Anastasios P. Palamidas and Mattheos Sanoudos and Evridiki Tsoureli-Nikita and Maria Virvou and George A. Tsihrintzis},
      year={2024},
      eprint={2405.10893},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}

## Dataset Card Contact

panagoulias_d@unipi.gr