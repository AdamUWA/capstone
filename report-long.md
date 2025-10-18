
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

My role was team leader...

My research...

I designed, implemented, and tested the entire application architecture end to end.

I utilised generated code sparingly, preferring to leverage library/API documentation and traditional programming techniques of writing, testing, and debugging in conjuction with intuition lead trial and error.


## Methods & Results

### Problem Formulation

My decision making framework for method selection can be divided into two approaches. Firstly, an intuition based methodology derived from domain knowledge and past experience. Secondly, a purely analytical methodology utilising standard academic methods of literature review and research. For the intuitive approach I relied on knowledge developed from previous coursework (eg., Natural Language Processing; Deep Learning; etc) and personal interests such as databases; Large Language Models (LLM); and Retrieval Augmented Generation (RAG) systems. This intuition enabled me to recognise important aspects of the project requirements; the relevant/appropriate methods; and the direction of focus for further investigation via the second approach - traditional research. The result of this process was to recognize that the problem, automated data extraction, would be optimally solved with a dynamic RAG system. And that the system would need to address the following **requirements**:

- Unstructured data inputs (i.e., poor quality scanned PDF documents).
- Dynamic information retrieval requests (i.e., non-static user queries).
- Strictly local hosting and execution (eg., restricted from networked external API calls).

The general methodology employed is thus comprised of intuition grounded in predeveloped knowledge; traditional academic research; and ad hoc problem identification and formulation.


### Problem Solving

Based on the formulated problem, the **requirements** therefore depend upon the following implementation **techniques**:

- Data preprocessing pipeline with Optical Character Recognition (OCR) capabilites.
- RAG with vector database for similarity search based context retrieval in conjuction with pre-trained LLMs for query/context augmentation.
- On device generative LLM hosting and non-remote in-memory vector store.

For detailed rational behind the above **techniques** refer to the [TODO] [project overview](LINK) wherein the architecture of the system was heavily inspired by the experience report of Khan and Hasan (REF) whithin which the authors present Figure 1.

![Figure 1.](architecture.png)

_Figure 1. RAG system architecture_

Several factors influenced the main design choice to use a RAG system. Firstly, the system would need to handle _dynamic_ requests. Specifically, a _static_ rules based system for information extraction was inappropriate as it would require determining/enumerating all possible peices of information that may be requested. For example, regular expression matching is optimal for deterministic and precise pattern matching in structured text (REF) whereas RAG is superior for tasks involving contextual reasoning and can modulate generative results with _dynamic_ and factually grounded knowledge retrieval from unstructured data (REF). Furthermore, regular expression systems are often brittle and present difficulties in implementation (REF).

OCR integrated document preprocessing is a well established standard technique for dealing with poor quality text based data. Given that the system was required to handle scanned copies of the original reports as the default input format, OCR was the natural choice (REF Hasan&Khan). The process and implementation specifics were inspired by the Docling project. Additional choices for the system such as pre-chunking and serializing the documents into JSON ojbect file for efficient vector store loading were influenced by Auer et al from their Docling Technical Report (REF). System dependent document preprocessing times are exhibited in Figure 2.


| Document | Pages | Pre-processing Time (sec) |
|----|----|----|
| Rodier-Finding.pdf | 6 | 31.14 |
| Blood-results-redacted.pdf | 7 | 26.1 |
| Forkin-finding-2014.pdf | 20 | 80.02 |
| TAULELEI-Jacob-Finding.pdf | 35 | 156.53 |
| Baby-H-finding.pdf | 50 | 200.99 |
| Nicholls-Diver-finding.pdf | 172 | 582.72 |

_Table 1. OCR document preprocessing with chunking & serializing; times: seconds; system: Apple M3 (10 core) with GPU accelaration._


The system dependence of the pre-processing times highlights the...

Benefits, limitations...


## NB

## References

- [A Case Study on Pros and Cons of Regular Expression Detection and Dependency Parsing for Negation Extraction from German Medical Documents. Technical Report](https://arxiv.org/abs/2105.09702)

- [Regexes are Hard: Decision-making, Difficulties, and Risks in Programming Regular Expressions](https://arxiv.org/abs/2303.02555)

- [A Systematic Review of Key Retrieval-Augmented Generation (RAG) Systems: Progress, Gaps, and Future Directions](https://arxiv.org/abs/2507.18910)

- [Engineering RAG Systems for Real-World Applications: Design, Development, and Evaluation](https://arxiv.org/abs/2506.20869v1)































