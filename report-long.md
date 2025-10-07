
# MDS Capstone Course Report

### _Adam Holt  21689348_


# Introduction

The [coroner project](https://github.com/AdamUWA/coroner) is result of the work of myself and my team members through working with Dr. Matt Albrecht [WACRSR](https://www.uwa.edu.au/projects/centre-for-road-safety-research/wacrsr-site-link) to design, implement, and evaluate a data extraction application for use on coroners reports. The purpose of this report is to document my personal contribution to the the project.

## Tasks 

Explanation of your tasks in the project.

## Methods (as shown in Github) & Results

- **Problem Formulation**: How did you make an informed decision for choosing the approach(es)/method(s)? Through past learning and experience, literature search, working with teams, seeking help or self directed learning? What general methodology you have learned in this project on approaching a new field with challenging problems?
 
- **Problem Solving**: For each of your chosen methods, explain the approach (with references), present the experiemental results, and discuss pros and cons. What's your take-away from such exercises? Which unit(s) in your MDS program has helped with the method selection, implementation and evaluation? What topics are missing or you wish you have studied. 

- **Ethical, Responsible AI and Broader Social Impact**: What potential social issues/impact that your models may have if wrong predictions or results are given? How would you mitgate this? Is there a non-data science or non-AI solution to this? 

## Personal Reflection

What were the technical and non-technical challenges and how did you overcome them; and what would you do differently, given your new experience and limits on time.



## Tasks

## Methods & Results

### Problem Formulation

My decision making framework for method selection can be divided into two aspects. Firstly, an intuition based methodology derived from domain knowledge and past experience. Secondly, a purely analytical methodology utilising standard academic methods of literature review and research. For the intuitive approach I relied on knowledge developed from previous coursework (eg., Natural Language Processing; Deep Learning; etc) and personal interest (eg., databases; RAG/LLM systems; etc). This intuition enabled me to recognise important aspects of the project requirements; the relevant/appropriate approaches; and the direction of focus for further investigation via the second approach - traditional research. The result of this process was to recognize that the problem, automated data extraction, was to be solved with a dynamic Retrieval Augmented Generation (RAG) system and that the system would need to address the following requirements:

- Unstructured data inputs (i.e., scanned PDF documents).
- Strictly local execution (eg., no outside network access, no external API calls).

For further details, refer to the ___ section of the [project overview](LINK).

### Problem Solving

The main design choice to use a RAG system was influenced by several factors. Firstly, the system would need to be able to handle dynamic requests. In other words, a rules based system for information extraction would be inappropriate as it would require determining/enumerating all possible peices of information that may be requested. For example, regular expression matching is optimal for deterministic and precise pattern matching in structured text (REF). RAG on the other hand is superior for tasks involving contextual reasoning and can enhance generative AI with dynamic knowledge retrieval from unstructured data (REF). Furthermore, regex techniques are often brittle and present difficulties in implementation (REF).






## NB

## References

- [A Case Study on Pros and Cons of Regular Expression Detection and Dependency Parsing for Negation Extraction from German Medical Documents. Technical Report](https://arxiv.org/abs/2105.09702)

- [Regexes are Hard: Decision-making, Difficulties, and Risks in Programming Regular Expressions](https://arxiv.org/abs/2303.02555)

- [A Systematic Review of Key Retrieval-Augmented Generation (RAG) Systems: Progress, Gaps, and Future Directions](https://arxiv.org/abs/2507.18910)

- [Engineering RAG Systems for Real-World Applications: Design, Development, and Evaluation](https://arxiv.org/abs/2506.20869v1)































