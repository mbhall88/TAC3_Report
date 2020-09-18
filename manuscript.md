---
author-meta:
- Michael B. Hall
bibliography:
- content/manual-references.json
date-meta: '2020-09-18'
header-includes: '<!--

  Manubot generated metadata rendered from header-includes-template.html.

  Suggest improvements at https://github.com/manubot/manubot/blob/master/manubot/process/header-includes-template.html

  -->

  <meta name="dc.format" content="text/html" />

  <meta name="dc.title" content="Third-year progress report for thesis advisory committee" />

  <meta name="citation_title" content="Third-year progress report for thesis advisory committee" />

  <meta property="og:title" content="Third-year progress report for thesis advisory committee" />

  <meta property="twitter:title" content="Third-year progress report for thesis advisory committee" />

  <meta name="dc.date" content="2020-09-18" />

  <meta name="citation_publication_date" content="2020-09-18" />

  <meta name="dc.language" content="en-UK" />

  <meta name="citation_language" content="en-UK" />

  <meta name="dc.relation.ispartof" content="Manubot" />

  <meta name="dc.publisher" content="Manubot" />

  <meta name="citation_journal_title" content="Manubot" />

  <meta name="citation_technical_report_institution" content="Manubot" />

  <meta name="citation_author" content="Michael B. Hall" />

  <meta name="citation_author_institution" content="EMBL-EBI" />

  <meta name="citation_author_institution" content="University of Cambridge" />

  <meta name="citation_author_orcid" content="0000-0003-3683-6208" />

  <meta name="twitter:creator" content="@mbhall88" />

  <link rel="canonical" href="https://mbhall88.github.io/TAC3_Report/" />

  <meta property="og:url" content="https://mbhall88.github.io/TAC3_Report/" />

  <meta property="twitter:url" content="https://mbhall88.github.io/TAC3_Report/" />

  <meta name="citation_fulltext_html_url" content="https://mbhall88.github.io/TAC3_Report/" />

  <meta name="citation_pdf_url" content="https://mbhall88.github.io/TAC3_Report/manuscript.pdf" />

  <link rel="alternate" type="application/pdf" href="https://mbhall88.github.io/TAC3_Report/manuscript.pdf" />

  <link rel="alternate" type="text/html" href="https://mbhall88.github.io/TAC3_Report/v/b3f08b5165b5f30988c3835f04d7faedb74e7145/" />

  <meta name="manubot_html_url_versioned" content="https://mbhall88.github.io/TAC3_Report/v/b3f08b5165b5f30988c3835f04d7faedb74e7145/" />

  <meta name="manubot_pdf_url_versioned" content="https://mbhall88.github.io/TAC3_Report/v/b3f08b5165b5f30988c3835f04d7faedb74e7145/manuscript.pdf" />

  <meta property="og:type" content="article" />

  <meta property="twitter:card" content="summary_large_image" />

  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />

  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />

  <meta name="theme-color" content="#ad1457" />

  <!-- end Manubot generated metadata -->'
keywords:
- phd
- thesis-plan
- genome-graphs
- bacterial-genomics
- nanopore
- tuberculosis
- variant-calling
- drug-resistance
lang: en-UK
manubot-clear-requests-cache: false
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
title: Third-year progress report for thesis advisory committee
...






<small><em>
This manuscript
([permalink](https://mbhall88.github.io/TAC3_Report/v/b3f08b5165b5f30988c3835f04d7faedb74e7145/))
was automatically generated
from [mbhall88/TAC3_Report@b3f08b5](https://github.com/mbhall88/TAC3_Report/tree/b3f08b5165b5f30988c3835f04d7faedb74e7145)
on September 18, 2020.
</em></small>

## Authors



+ **Michael B. Hall**<br>
    ![ORCID icon](images/orcid.svg){.inline_icon}
    [0000-0003-3683-6208](https://orcid.org/0000-0003-3683-6208)
    · ![GitHub icon](images/github.svg){.inline_icon}
    [mbhall88](https://github.com/mbhall88)
    · ![Twitter icon](images/twitter.svg){.inline_icon}
    [mbhall88](https://twitter.com/mbhall88)<br>
  <small>
     EMBL-EBI; University of Cambridge
     · Funded by EMBL International PhD Programme (EIPP)
  </small>



## Part A: Progress Report {.page_break_before}

### Thesis Advisory Committee

- Zamin Iqbal (Supervisor) - EMBL-EBI
- John Marioni (Chair) - EMBL-EBI
- Georg Zeller - EMBL Heidelberg
- Estée Török - University of Cambridge

**Starting Date**: 12/10/2017  
**Qualifying Assessment Date**: 06/07/2018  
**Second TAC Meeting**: 15/10/2019  
**Third TAC Meeting**: 13/10/2020

### Examining bacterial variation with genome graphs

#### Executive summary

Genomics is now ubiquitous in clinical and public health microbiology, at least in the
developed world. However, many significant challenges remain.
- Bacterial genomes harbour huge amounts of diversity, even within a species, and
  traditional reference-based approaches are problematic.
- Much of the variation in bacteria is fundamentally inaccessible to short reads.
- Long Nanopore reads are noisy, and SNP calling with this data is not properly
  benchmarked or standardised.
- Since *Mycobacterium tuberculosis* (Mtb) infects so many people, there is potential
  for considerable impact for clinical applications.
- There is also much to be gained from a high-quality pan-genome of Mtb as well as a
  detailed map of its enigmatic *pe/ppe* gene repertoire.


These motivations drive the following PhD thesis structure:
1. Develop algorithms and software for variant discovery using bacterial genome graphs,
   building on work of a previous student in the lab (my first paper, second author).
2. Benchmark Nanopore versus Illumina SNP calling, showing our algorithms meet the needs
   of clinical and public health users, validate, and publish (second paper).
3. Improve upon current whole-genome sequencing-based drug resistance prediction for Mtb
   using genome graphs.
4. Curate a high-quality reference pan-genome for Mtb that includes a detailed map of
   the *pe/ppe* genes.



## Part B: Training and career development {.page_break_before}

### Publication Strategy

> Briefly outline the publication strategy; set priorities if needed.

### List of publications, papers in press, preprints, manuscripts submitted/in preparation to date

### Work plan and timeline for thesis submission 

> Provide a work plan to be completed prior to thesis writing and a timeline for submission.

### List of scientific courses and conferences attended to date and planned for next year

> Please list all events in reverse chronological order.

###  List of additional training, teaching and other relevant activities to date

> Please list all training and other activities in reverse chronological order.

### Career development plan

#### Please describe your current long-term career aims (i.e. 3-5 years after PhD). 

#### Please comment on the types of position you would like to apply to for after the PhD and your expected application timeline? 

> If applying for postdoc positions, which fields/fellowships are you considering? If you are applying for non-academic careers, what type of role? Do you have target companies or organisations in mind?

#### What do you see as your strengths (2-3 skills)?

#### What do you see as your areas for improvement1 (2-3 areas)?

#### What are your career development priorities until the end of your contract? 

> Please take into account both the scientific and non-scientific skills you will need to work on a successful and timely completion of the PhD. List the skills you still need to acquire to achieve your longer-term career aims. 

#### What actions will you take to develop these skills?

> This may include training courses, opportunities to practice and develop these skills, or seeking feedback/guidance. N.B. fellows should take 1-2 non-scientific trainings or career development workshops per year, and at least one international conference during their PhD.







## Part C: Impact of COVID-19 pandemic {.page_break_before}

> As outlined in the Procedures for COVID-19 related fellows’ contract extensions, students and their GTL should document the impact of the corona crisis on the PhD project. The TAC should assess the approximate project delay and discuss how this could be mitigated over the remaining PhD period. Please use the space below to outline the impact of corona crisis on your project (e.g. lost productivity / project delays).


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
