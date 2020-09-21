---
author-meta:
- Michael B. Hall
bibliography:
- content/manual-references.json
date-meta: '2020-09-21'
header-includes: '<!--

  Manubot generated metadata rendered from header-includes-template.html.

  Suggest improvements at https://github.com/manubot/manubot/blob/master/manubot/process/header-includes-template.html

  -->

  <meta name="dc.format" content="text/html" />

  <meta name="dc.title" content="Third-year progress report for thesis advisory committee" />

  <meta name="citation_title" content="Third-year progress report for thesis advisory committee" />

  <meta property="og:title" content="Third-year progress report for thesis advisory committee" />

  <meta property="twitter:title" content="Third-year progress report for thesis advisory committee" />

  <meta name="dc.date" content="2020-09-21" />

  <meta name="citation_publication_date" content="2020-09-21" />

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

  <link rel="alternate" type="text/html" href="https://mbhall88.github.io/TAC3_Report/v/18ad6fe582ba5e849b90bf4ef3da92a66c42b6e1/" />

  <meta name="manubot_html_url_versioned" content="https://mbhall88.github.io/TAC3_Report/v/18ad6fe582ba5e849b90bf4ef3da92a66c42b6e1/" />

  <meta name="manubot_pdf_url_versioned" content="https://mbhall88.github.io/TAC3_Report/v/18ad6fe582ba5e849b90bf4ef3da92a66c42b6e1/manuscript.pdf" />

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
([permalink](https://mbhall88.github.io/TAC3_Report/v/18ad6fe582ba5e849b90bf4ef3da92a66c42b6e1/))
was automatically generated
from [mbhall88/TAC3_Report@18ad6fe](https://github.com/mbhall88/TAC3_Report/tree/18ad6fe582ba5e849b90bf4ef3da92a66c42b6e1)
on September 21, 2020.
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



## Thesis Advisory Committee {.page_break_before}

- Zamin Iqbal (Supervisor) - EMBL-EBI
- John Marioni (Chair) - EMBL-EBI
- Georg Zeller - EMBL Heidelberg
- Estée Török - University of Cambridge

**Starting Date**: 12/10/2017  
**Qualifying Assessment Date**: 06/07/2018  
**Second TAC Meeting**: 15/10/2019  
**Third TAC Meeting**: 13/10/2020


## Part A: Progress Report {.page_break_before}

### Examining bacterial variation with genome graphs

### Executive summary

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

### Motivation and Background

In 2018, 1.4 million people died of tuberculosis (TB) globally, and over 10 million
people fell ill to the disease. There were also 484,000 new cases of
rifampicin-resistant TB reported, of which 78% were multi-drug resistant (MDR)
[@isbn:9789241565714]. Drug-resistant TB is not a new problem; the first clinical trial
using Streptomycin to treat TB reported resistance and this outcome influenced the
creation of the four-drug first-line regimen used today. Standard of care requires
phenotypic testing of the infecting organism against these four drugs to ensure that
appropriate treatment is prescribed. However, *Mycobacterium tuberculosis* (Mtb), the
causative agent of TB, is a slow-growing organism and the gold-standard phenotypic tests
("mix bug and drug") take around two months to complete. Thus, the traditional clinical
diagnostic and treatment regimen is slow and expensive. Whole-genome sequencing offers a
faster solution; recently it was shown that equivalent results are achievable by
sequencing Mtb grown in "liquid culture" (also known as MGIT, Mycobacterial Growth
Indicator Tube) after two weeks of culture in contrast to the two-month traditional
(Lowenstein-Jensen) culture method [@doi:10.1128/JCM.03073-14]. A number of genes are
implicated in drug resistance and predicting resistance from sequencing data based on a
catalogue of resistance single-nucleotide polymorphisms (SNPs) and indels (insertions or
deletions) works with high-specificity [@doi:10/f755tg; @doi:10/f3jjtq]. For the four
first-line drugs, a study by the CRyPTIC consortium is the first of its kind to
demonstrate that phenotyping is not required if genotype predicts susceptibility
[@doi:10.1056/NEJMoa1800474]. However, as the genetic basis for drug resistance is not
entirely understood, there is still a sensitivity gap that differs drug-by-drug.

Public health requirements for TB diagnostics are **resistance prediction, species
identification, and clustering** of genomes. The clusters are intended to contain
potential transmission events, thus enabling more effective contact tracing. All of the
main requirements are currently successfully achieved with Illumina sequencing
technology. However, there are reasons to consider abandoning Illumina for Oxford
Nanopore Technology's (ONT) sequencer. First, there is cost - Illumina has raised its
reagent prices considerably. Second, the burden of TB lies primarily in places where
there is neither capital nor infrastructure for purchasing or maintaining a large
machine. The third is speed: Votintseva *et al.* showed that it was feasible to go from
patient to result via a Nanopore sequencer in 12.5 hours [@doi:10.1128/JCM.02483-16].
Since this publication, the yield and quality of Nanopore has risen. Therefore, a
diagnostic that delivers results while the patient is in the clinic is now imaginable.

As an aside, it is worth noting that in high prevalence areas, there is no interest in
transmission analysis, and therefore all of the information that they need (species and
resistance) could be attained via deep amplicon sequencing. We accept this but ignore it
and focus on a whole-genome solution nevertheless; both because of the better
phylogenetic resolution, and because we do not yet know the relevant genetic mutations
associated with new drugs.

The idea of using a single, linear reference genome to represent a population of
individuals is not ideal. Even more so in the context of a bacterium such as *Salmonella
enterica*, where two individuals can differ to such a degree that they only share 16% of
their genes [@doi:10/gfw8gq; @doi:10/gczkbr]. This fluidity of genetic content leads to
the concept of a pan-genome; defined as the set of all genes observed in a species. Some
genes are more common than others within this pan-genome, leading to the distinction of
the 'core' and 'accessory' genome with the core being those shared across (most) all
individuals and accessory being everything else. The effect of using a single-reference
genome to describe variation within samples from the same species is best illustrated in
Figure {@fig:refbias}. In this toy example, the maximum number of SNPs we can hope to
discover is only 56%. Clearly, comparing many samples requires better methods than
single-reference based ones.

![An illustration of how reference bias can impact variant-calling. Each vertical
column signifies an individual genome, with the coloured blocks representing genes.
Numbers label 50 segregating SNPs. The percentages at the bottom express the proportion
of SNPs which can be detected using each of the 6 'genomes' as a reference by mapping
perfect reads from the remaining 5 to this reference.](images/refbias.png){#fig:refbias
height="4in"}

One of the first questions that arise from a computational point-of-view is how to apply
current methods, which assume a single reference, to a pan-genome? An approach to
answering this question that has been gaining considerable traction in recent years is
that of genome graphs. This new paradigm uses a population reference graph (PRG) as its
equivalent of a single, linear, reference genome. A PRG is built to represent variation
seen within a population, conceding the fact that no single genome can accurately
represent an entire species. To construct such a PRG, one takes a multiple sequence
alignment (MSA) and collapses shared sequence and creates "bubbles", or branch points,
where they do not (see Figure {@fig:prg} for an illustration of this process). We define
a collection of PRGs as a pan-genome reference graph (PanRG), which we will
interchangeably refer to as a pan-genome. Thus far, genome graph methods have focused
mainly on eukaryotes. Given the rich diversity of genetic content in the prokaryote
world, it would seem genome graphs are more suited to utilisation there.

![An illustration of how a population reference graph (PRG) is constructed. Regions 
(columns) of shared sequence are collapsed into a single node. Those that differ are 
split into "bubbles", or branching nodes.](images/prg.png){#fig:prg width="100%"}

Nanopore sequencing yields very long reads (up to 2.2Mbp [@doi:10/gfnkxj]), the
mean/mode read identity tends to fall in the range of 87-94% (using ONT's `guppy`
basecaller), while on a consensus level, it can achieve 99.94% with assembly polishing
[@doi:10/gf4jwm].  
Variant calling with Nanopore sequencing data has seen a somewhat slow development.
Currently, the main tools that have had reasonable testing done and are versatile enough
to detect both SNPs and (some) indels are `nanopolish` [@doi:10/f88652], Clair
[@doi:10/d9kq] and `medaka` [@https://github.com/nanoporetech/medaka]. A recent
benchmark showed that Nanopore variant calling provides reliable diagnostic information
for *Neisseria gonorrhoeae* [@doi:10.1101/gr.262865.120]. However, to date, there has
been no extensive Nanopore variant calling benchmark done for Mtb. Given the potential
benefits of using genome graphs and long-read Nanopore sequencing for bacterial
genomics, it makes sense to try and blend the two.

Pandora is a method being developed in the group to genotype across the *entire*
pan-genome of a bacterial sample - not just the core. It does this by working with a
PRG, rather than a linear reference. The method is based on the following intuition
(similar to that behind the Li and Stephens model in population genetics): genomes
evolve by recombination and mutation, and thus we ought to be able to approximate a
$N+1$ genome as a mosaic of the first $N$ genomes. `pandora` maps Nanopore reads to a
graph encoding of a PRG, infers a mosaic, and provides genotypes at all variants in the
PanRG. Mapping is done using minimising k-mers [@doi:10/dkhs8w] in a similar vein to
that done by `minimap`[@doi:10/f8zxc3], and is therefore fast. By using Nanopore
sequencing data, it is also possible to infer gene order as, in general, a single read
will contain multiple genes, as opposed to Illumina sequencing where multiple reads are
required to span a single gene. Note `pandora` does not (prior to this work) include any
facility for discovering novel variation.


#### Summary

This PhD seeks to develop new methods to enable Nanopore-based diagnostics and
epidemiology for Mtb and other bacteria. By using PRGs as a strong prior [@doi:10/d9ks;
@doi:10.1038/ng.3257], we should be able to mitigate the Nanopore error biases and indel
issues. In the process, we aim to construct a high-quality reference pan-genome for Mtb
that we hope will open previously inaccessible parts of its genome for investigation.


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
