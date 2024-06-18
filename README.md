## AMRFact: Enhancing Summarization Factuality Evaluation with AMR-Driven Negative Samples Generation

<div align="center">
<b>Haoyi Qiu, Kung-Hsiang Huang*, Jingnong Qu*, Nanyun Peng</b>
</div>
<div align="center">
<b>University of California, Los Angeles</b>
<br>
<b>University of Illinois Urbana-Champaign</b>
</div>
<div align="center">
*Equal contribution, listed
in alphabetical order by last name.
</div>
<div align="center">
    <a href="https://arxiv.org/pdf/2311.09521"><img src="https://img.shields.io/badge/Paper-Arxiv-orange" ></a>
</div>


## Introduction
🔍 Ensuring factual consistency is crucial for natural language generation tasks, particularly
in abstractive summarization, where preserving the integrity of information is paramount.
Prior works on evaluating factual consistency
of summarization often take the entailmentbased approaches that first generate perturbed
(factual inconsistent) summaries and then train
a classifier on the generated data to detect the
factually inconsistencies during testing time.
However, previous approaches generating perturbed summaries are either of _low coherence_
or _lack error-type coverage_.

![](assets/amrfact_overview.png?v=1&type=image)

📌 To address these
issues, we propose **AMRFACT**, a framework
that generates perturbed summaries using Abstract Meaning Representations (AMRs). Our
approach parses factually consistent summaries
into AMR graphs and injects controlled factual
inconsistencies to create negative examples, allowing for coherent factually inconsistent summaries to be generated with high error-type
coverage.

![](assets/amrfact_error_types.png?v=1&type=image)

⚖️  Additionally, we present a data selection module **NEGFILTER** based on natural
language inference and BARTSCORE to ensure
the quality of the generated negative samples.

![](assets/amrfact_negfilter.png?v=1&type=image)

🚧 Experimental results demonstrate our approach
significantly outperforms previous systems on
the AGGREFACT-FTSOTA benchmark, showcasing its efficacy in evaluating factuality of
abstractive summarization.

![](assets/amrfact_main_results.png?v=1&type=image)

🌟 Our contributions not only advance the field in generating highquality, factually inconsistent summaries but also provide a scalable and efficient solution for enhancing the factuality evaluation of summarization systems. The results underscore the potential of AMRbased perturbations in improving the integrity and
reliability of natural language generation.


## Citation
If you found this work useful, consider giving this repository a star and citing our paper as followed:
```
@inproceedings{qiu-etal-2024-amrfact,
    title = "{AMRF}act: Enhancing Summarization Factuality Evaluation with {AMR}-Driven Negative Samples Generation",
    author = "Qiu, Haoyi  and
      Huang, Kung-Hsiang  and
      Qu, Jingnong  and
      Peng, Nanyun",
    editor = "Duh, Kevin  and
      Gomez, Helena  and
      Bethard, Steven",
    booktitle = "Proceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 1: Long Papers)",
    month = jun,
    year = "2024",
    address = "Mexico City, Mexico",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.naacl-long.33",
    pages = "594--608",
}
```
