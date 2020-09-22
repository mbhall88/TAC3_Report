---
author-meta:
- Michael B. Hall
bibliography:
- content/manual-references.json
date-meta: '2020-09-22'
header-includes: '<!--

  Manubot generated metadata rendered from header-includes-template.html.

  Suggest improvements at https://github.com/manubot/manubot/blob/master/manubot/process/header-includes-template.html

  -->

  <meta name="dc.format" content="text/html" />

  <meta name="dc.title" content="Third-year progress report for thesis advisory committee" />

  <meta name="citation_title" content="Third-year progress report for thesis advisory committee" />

  <meta property="og:title" content="Third-year progress report for thesis advisory committee" />

  <meta property="twitter:title" content="Third-year progress report for thesis advisory committee" />

  <meta name="dc.date" content="2020-09-22" />

  <meta name="citation_publication_date" content="2020-09-22" />

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

  <link rel="alternate" type="text/html" href="https://mbhall88.github.io/TAC3_Report/v/1914b4f312f5beca2bd69504539ec2c4bf4df18c/" />

  <meta name="manubot_html_url_versioned" content="https://mbhall88.github.io/TAC3_Report/v/1914b4f312f5beca2bd69504539ec2c4bf4df18c/" />

  <meta name="manubot_pdf_url_versioned" content="https://mbhall88.github.io/TAC3_Report/v/1914b4f312f5beca2bd69504539ec2c4bf4df18c/manuscript.pdf" />

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
([permalink](https://mbhall88.github.io/TAC3_Report/v/1914b4f312f5beca2bd69504539ec2c4bf4df18c/))
was automatically generated
from [mbhall88/TAC3_Report@1914b4f](https://github.com/mbhall88/TAC3_Report/tree/1914b4f312f5beca2bd69504539ec2c4bf4df18c)
on September 22, 2020.
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

<!--================================================================================-->

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

<!--================================================================================-->

### Chapter 1: Variant discovery in genome graphs

Variation in bacterial genomes can arise through a diverse range of processes. Mutations
can arise during replication and are inherited vertically, genetic material can be
transferred horizontally, and homologous recombination can lead to eukaryote-like gene
conversion [@doi:10/b4x7zf]. This breadth of ways in which bacteria can acquire new and
varied genetic material results gives rise to the phenomenon of a pan-genome. Bacterial
species with an "open" pan-genome may have individuals in their population who can share
as little as 16% of their genes (*S. enterica*) [@doi:10/gfw8gq]. Not all species'
pan-genomes are this open, but it does raise the question: what do we use as a
"reference" genome for such a species? One solution is to use the reference genome for
the specific strain of interest. This works fine when dealing with a single sample or
multiple samples of the same strain. However, when expanding to many samples from
varying strains, the reference is no longer representative. An alternative solution is
to focus solely on the core genome - the complement of genes found in all members of a
species (see Figure {@fig:pangenome}). The issue with this approach is the loss of
information about variation in all of the non-core genes, which could be a large number
if the pan-genome is open. See Figure {@fig:pangenome} for an illustration of this
reference-bias problem.

![Schematic representation of a pan-genome. Each oval represents the
genetic content of a single individual within a species. Reference [@doi:10/gfw8gq].](images/pangenome.jpg){#fig:pangenome
width="50%"}

The message we are aiming to drive home at the beginning of this chapter is that
reference-based analysis fundamentally cannot access all of the variation in a bacterial
species.

#### Prior work: Mosaic approximations and genotyping

Standard approaches to variant analysis are effectively a first-order approximation. In
such an approximation, samples are considered identical to the reference, one maps reads
to it, identifies clear SNPs via the read pileup, and then modifies the reference to get
an estimate of the sample's genome. As mentioned in
[Motivation and Background](#motivation-and-background), `pandora` is a method developed
by a previous PhD student in the lab, Rachel Colquhoun. It works on the premise of
approximating a genome as a hierarchical mosaic. At a high-level, it represents a mosaic
of loci - usually genes and intergenic regions - while at the locus-level, it is a
mosaic of previously-seen genomes.

`pandora` has two main workflows: `map` and `compare`. `map` aims to infer a consensus
sequence from a PRG for a single sample. The consensus sequence says two things about
the sample: the loci present in the sample, and the most likely path through the PRG for
each present locus. Optionally, `map` can run genotyping of the sample, providing a
Variant Call Format (VCF) file for the sample with respect to the consensus sequence (or
a user-provided sequence). `compare` aims to infer a consensus sequence that best
represents a given set of genomes and then genotype each sample with respect to this
inferred "average" genome. The advantage of this approach is that the consensus best
represents the specific samples provided. This allows for genotyping across the *entire*
pan-genome. If a gene is present in only 2 of 50 samples then genotyping information is
provided for those 2 samples and null for the other 48.

While `pandora`, before the work in this chapter, allows comparison of genomes to a
level of detail provided by no other tool, there is still a significant shortcoming: it
cannot discover novel variation. If a sample contains a variant not present in the PRG,
the best `pandora` can do is select the path that is closest to that variant. The work
in my first chapter outlines a method for removing this limitation within `pandora` and
provides an analysis of the gain in recall and precision by incorporating *de novo*
variant discovery into the `pandora` workflow.

#### Local *de novo* variant discovery in a genome graph

There are two significant difficulties in discovering *de novo* variants on a graph. The
first is finding regions within the graph that look like the reads mapping to them
contain variation we do not have in the PRG. Secondly, we need to generate new paths for
these regions and add them back into the PRG for consideration when remapping.

##### Finding candidate regions

We define a candidate region, $r$, as an interval within a local graph where coverage on
the maximum likelihood path is less than a given threshold, $c$, for more than $l$
consecutive positions. For a given read that has a mapping to $r$, we define $s_r$ to be
the subsequence of the read mapping to $r$. We define the pileup $P_r$ as the set of all
$s_r \in r$.

##### Enumerating paths through candidate regions

For $r \in R$, where $R$ is the set of all candidate regions, we construct a de Bruijn
graph $G_r$ from $P_r$.  
$A_L$ and $A_R$ are defined as kmers to the left and right of $r$ in the local graph.
They are anchors to allow re-insertion of new sequences found by *de novo* discovery
into the local graph. If $A_L \notin G_r \lor A_R \notin G_r$ then we abandon *de novo*
discovery for $r$.  
$T_r$ is the spanning tree obtained by performing depth-first search (DFS) on $G_r$ from
node $A_L$. $p_r$ is defined as a path, from the root node $A_L$ of $T_r$ and ending at
node $A_R$, which fulfills the following two conditions:

- $p_r$ is shorter than the maximum allowed path length.
- No more than $k$ nodes along $p_r$ have coverage $< (n_r \times 0.1) \times e_r$,
  where $n_r$ is the a counter, described below, and $e_r$ is the expected k-mer
  coverage for $r$.

$V_r$ is the set of all $p_r$. If $|V_r|$ is greater than a predefined threshold, $n_r$
is incremented by 1 and $V_r$ is repopulated. If $n_r \times 0.1 = 1.0$ then *de novo*
discovery is abandoned for $r$.

##### Pruning the path-space in a candidate region

As `pandora` operates on both accurate and error-prone sequencing reads, the number of
valid paths in $G_r$ can be very large. In testing, this results in run-times beyond
seven days (the longest any attempt was allowed to run). The increased run-time is due
to cycles that can occur in $G_r$ and exploring paths that will never reach our required
end anchor $A_R$. In order to reduce the path-space within $G_r$ we prune paths based on
multiple criteria. Critically, this pruning happens at each step of the graph walk
(path-building).  
In addition to $T_r$, obtained by performing DFS on $G_r$, we produce a distance map
$D_r$ that results from running reversed breadth-first search (BFS) on $G_r$, beginning
from node $A_R$. We say reversed BFS as we explore the predecessors of each node, rather
than the successors. $D_r$ is implemented as a binary search tree where each node in the
tree represents a k-mer in $G_r$ that is reachable from $A_R$ via reversed BFS. Each
node additionally has an integer attached to it that describes the shortest path from
that node to $A_R$.  
We can use $D_r$ to prune the path-space by requiring, for each node, $n \in p_r$: is $n
\in D_r$ **and** can $A_R$ be reached from $n$ in a minimum of $i$ nodes, where $i$ is
defined as the maximum allowed path length minus the number of nodes walked to reach
$n$. If one of these conditions is not met, we abandon $p_r$. The advantage of this
pruning process is that we never explore paths that will not reach our required end
point and when caught in a cycle, we will abandon the path once we have made too many
iterations around the cycle.


I programmed the above methods in C++ and added them into the code base for `pandora`.
They constitute 1325 lines of source code and 3486 lines of test code. I had help with
the implementation of multi-threading the *de novo* component and the BFS pruning from
Leandro Ishi. The overall workflow for `pandora` with *de novo* variant discovery
enabled is illustrated in Figure {@fig:pandora}.

![Schematic of the `pandora` method. Note Steps 4-6 are those developed and added
in the scope of chapter 1. 1) A Population Reference Graph (PRG) built from known
variants or previous samples. 2) Sequencing reads to try and map on to the PRG. 3) Reads
mapped on to the PRG (where possible) using minimising k-mers. Coloured segments show
paths where reads map. 4) Local assembly of the reads using a de Bruijn graph due to
lower than expected coverage on a section of the PRG (many unmapped reads). A new path
is discovered (orange). 5) The new path is added into the original PRG. 6) Reads are
remapped to the new PRG with many reads mapping to the newly included path (orange).](images/pandora.png){#fig:pandora
width="80%"}

#### Evaluation

##### Simulated data

The first step in evaluating the effect of adding *de novo* variant calling to `pandora`
is with a simulated dataset. What we aim to show here is that the addition of *de novo*
discovery allows `pandora` to improve its probability of variant detection (recall). The
first step was randomly selecting 100 gene MSAs from a pool of 29702 obtained for
*Escherichia coli* from the panX database [@doi:10/gczkbr]. Next, a PRG is constructed
for each gene MSA, and a random path through each is selected using `pandora`. Each
PRG's random path is then concatenated together to form a single "genome" sequence. We
subsequently add SNPs to the simulated genome at a specified rate of SNPs per-gene using
`snp-mutator` [@doi:10/d9np]. We then simulated Nanopore reads from this mutated genome
using `nanosim-h` [@doi:10/gbj69k; @doi:10/d9nq]. `pandora map` is then run, using the
original PRG as input, along with the reads simulated from the mutated genome. With this
approach, we know the exact SNPs we hope to find. After running the `map` routine, we
are left with a collection of candidate paths produced by the *de novo* component. We
then added these back into the PRG and iterated the `map` routine again, this time
without *de novo* discovery enabled. Re-adding variants into the graph has the effect of
making all of the *de novo* variants visible to genotyping. The result is a VCF file
that (hopefully) contains the variants we introduced in the beginning. To compare the
performance of `pandora` before and after *de novo* is added, we can compare the VCF
produced from the first round of `map` with the last VCF.

To avoid error-prone conversion of linear coordinates into graph coordinates the
evaluation of whether the variants called by `pandora` are correct was undertaken in a
slightly more convoluted manner. We define a probe-set $P$ as a collection of probes,
$p$, where $p$ represents an entry, $e$, in a VCF file, $V$. For each $e \in V$, $p$ is
constructed by the concatenation of $l_w$, $e_c$, and $r_w$ (in that order), where $e_c$
is the called variant of $e$, and $l_w$ and $r_w$ are the sequences, of maximum length
$w$, in the VCF reference to the left and right, respectively, of $e_c$.

A truth probe-set, $P_t$, was constructed from the VCF of variants added to the
simulated genome and a query probe-set, $P_q$, from the variants called by `pandora`. We
then mapped all probes from $P_t$ to $P_q$ using `bwa mem` [@arxiv:1303.3997]. We then
classify each mapped probe as a false positive or true positive and calculate precision
and recall for the pre-*de novo* and post-*de novo* VCF files from `pandora`. As
expected, Figure {@fig:simulation_roc} shows that without *de novo* variant discovery,
we are unable to find almost all introduced variants. In future work, we plan to add
indels to the simulations.

![Precision-recall curve for `pandora` simulations with (circles) and without (crosses) *de novo* variant
discovery. This plot is measuring the proportion of SNPs we introduced into our
simulated genome we correctly found (recall) on the X-axis. On the Y-axis is the
proportion of calls we made which were correct (precision). Colours represent different
coverage depth. Each point represents a different genotype confidence
threshold.](images/simulation_roc_denovo_and_no_denovo.png){#fig:simulation_roc
width="90%"}

##### Empirical data - multi-sample comparison

This section will be the major focus for the evaluation of both *de novo* *and*
`pandora` and will constitute the results section of the `pandora` paper (near
completion). We aim to show, with the *compare* routine, the power of using a PRG
instead of a single reference along with `pandora`'s performance compared to
`nanopolish` and `medaka` (Nanopore) and `snippy` (Illumina)
[@https://github.com/tseemann/snippy]. We compare 20 samples, from across the *E. coli*
phylogeny. As other variant callers do not use a PRG we carefully selected 24
single-reference genomes representing the diversity of the *E. coli* phylogenetic tree
as best as possible. Each variant caller was run once for each reference genome with the
aim being to show that the more samples in the analysis, the lower the number of
variants the caller can find.

The evaluation will again follow a similar method to the
[Simulated data](#simulated-data). The truth for this analysis, however, is a bit more
complicated. In the process of developing an evaluation framework, we produced a python
package called `varifier` (<https://github.com/iqbal-lab-org/varifier>). Briefly, for
precision, `varifier` creates 'probes' for each variant in the VCF, using the genome the
variants we called with-respect-to. It then maps these probes to the truth genome for
the sample and determines the distance between the variant component of the probe and
the part of the truth genome it maps to. For recall evaluation, `varifier` collects all
differences in the pairwise alignment between the truth and VCF-reference genomes.
Probes are created for these differences (based on the truth genome) and they are mapped
to an augmented version of the VCF-reference genome, which has had the variants applied
to it. The mappings are then evaluated in the same way as for precision.  
As `pandora compare` calls variants for each sample with respect to an inferred best
approximation sequence for all samples, creating the set of truth variants is slightly
different. We perform a pairwise alignment for all pairs of samples and collect all the
differences from this alignment. We then deduplicate this panel to ensure variants are
not "double counted", meaning core genome variants would have an unbalanced effect on
the overall precision and recall. We then follow the same probe-mapping approach from
`varifier` with these truth variants.

<!--https://github.com/iqbal-lab/pandora1_paper/issues/209-->
We filtered `pandora` variants based on the following criteria:

- Depth less than 15x
- Less than 20% of reads are on one strand
- 50% or more of kmers on the allele have zero coverage

After we have run this analysis, we will also most likely need to investigate applying
filters to the VCF file to remove any biases relating to problems like strand bias or
coverage.


Whilst I wrote nearly all of the code and associated tests for evaluating the recall for
this analysis, a lot of it has since been refactored by Leandro Ishi and by Martin Hunt
in the form of `varifier`. Due to the novelty of the method we are proposing, this has
taken quite a lot of time and thought. I wrote 1250 lines of code to evaluate the
methods, along with 3500 lines of test code to ensure there are no bugs in our
evaluation. Additionally, I built the original `snakemake` [@doi:10/gd2xzq] pipeline of
approximately 3500 lines of codes to orchestrate the entire evaluation and simulations
(However, much of this has been rewritten by Leandro Ishi).

<!--TODO add ROC and associated text-->

<!--TODO do we still want to do this?-->
<!--\subsubsection{CPU and Memory Performance} In this section, we will investigate the-->
<!--`pandora` CPU and memory performance impact of adding *de novo* variant discovery. Both-->
<!--in single- and multi-threaded modes.-->

#### Outstanding work

The major work still outstanding for this project is the direct integration of *de novo*
candidates back into the PRG. The current procedure requires a fairly laborious,
multi-step process for adding *de novo* candidates into the PRG, requiring the user to
run a separate pipeline from `pandora`. Ultimately this will need to be handled all
within the `pandora` program with no intervention from the user.  
To measure whether the reference bias effect in Figure {@fig:refbias} is real and
significant, we plan to measure it in three species: *E. coli*, *Klebsiella pneumoniae*,
and *Streptococcus pneumoniae*. For each of the species, we will take a set of
high-quality reference genomes, and perform the pair-wise alignment-based evaluation
from the `pandora` [multi-sample comparison](#empirical-data---multi-sample-comparison).
This work will aid the message in the introduction to my first chapter. Much of this
work is being completed by Leandro Ishi, but it borrows heavily on some of the
evaluation code I have written for the multi-sample comparison.  
Lastly, there is an ongoing refinement of the *de novo* variant discovery process from
the work in Chapters 2 and 3. The analysis in these chapters lean heavily on `pandora`,
but for Mtb, which has a very different pan-genome to that of *E. coli* - which was used
for most of the development of `pandora`'s methods.

<!--================================================================================-->


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
