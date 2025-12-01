---
title: 'DBCLS BioHackathon 2025 report: Template for the very long title'
title_short: 'BioHackJP25: How we found breakfast'
tags:
  - Semantic web
  - Ontologies
  - Workflows
authors:
  - name: Andra Waagmeester
    orcid: 0000-0001-9773-4008
    affiliation: 1
  - name: Vincent Emonet
    orcid: 0000-0002-1501-1082
    affiliation: 2
  - name: Jerven Bolleman
    orcid: 0000-0002-7449-1266
    affiliation: 2
affiliations:
  - name: AmsterdamUMC, Amsterdam, the Netherlands
    ror: 05grdyy37
    index: 1
  - name: SIB Swiss Institute of Bioinformatics, Geneva, Switzerland
    ror: 002n09z45
    index: 2
date: 1 December 2025
cito-bibliography: paper.bib
event: BH25JP
biohackathon_name: "DBCLS BioHackathon 2025"
biohackathon_url:   "https://2025.biohackathon.org/"
biohackathon_location: "Mie, Japan, 2025"
group: YOUR-PROJECT-NAME-GOES-HERE
# URL to project git repo --- should contain the actual paper.md:
git_url: https://github.com/biohackathon-japan/bh25-bhxiv-template
# This is the short authors description that is used at the
# bottom of the generated paper (typically the first two authors):
authors_short: First Author \emph{et al.}
---

# Introduction

As part of the DBCLS BioHackathon 2025, we here report an extension to the SPARQL-examples repository maintained by the Swiss Bioinformatics Institute (SIB) [@citesAsAuthority:10.1093/gigascience/giaf045]. 
SIB maintaines a large set of SPARQL endpoints and has been doing so since 20xx (TODO:citation). Often these SPARQL endpoints are documented by a large set of example queries. To streamline and centralize the collection of 
example queries, SIB's sparql-examples has been developed using GitHub's pages and actions. This allows hosting those examples as documents with some appealing visualization. Upon submitting an example, a github action will publish the example as an extension to the platform with a visualization like the one in Figure 1 (todo). 

## Hosting a sparql examples
The sparql-example at SIB host primarily example queries for the resources maintained by the SIB. However, GitHub's forking allows duplicating the sparql-examples within other institutes. Doing so is straightforward. 
1. Fork the repository to an account that will host the examples
2. Enable GitHub pages and GitHub Actions
3. Remove the examples from SIB and replace with examples
4. Update the `index.md` in the main directory to point to the new examples

## SPARQLTree
Once the sparql-examples from SIB has been forked, ones own sparql examples can be added by embedding the queries in a metadata format that captures metadata as triples. This format contains keywords, endpoints to which the query can be submitted to get sensible results. 
Maintaining this can be tedious, since the SPARQL query has to be added within the RDF. During the biohackathon we worked on a more userfriendly approach to collect SPARQL examples. This by using the approach used in [SPARQLSponge](https://github.com/andrawaag/SPARQLSponge)

## Author information

Information about the authors is given in the [YAML](https://en.wikipedia.org/wiki/YAML) format at the top of this template.
For authors you provide their names, their affiliations, and ideally their [ORCID](https://orcid.org/)
identifier. For affiliations, the [Research Organization Registry](https://ror.org/) (ROR) identifier can be given.
For example, this is the author information for this template:

```yaml
authors:
  - name: First Author
    affiliation: 1
  - name: Last Author
    orcid: 0000-0000-0000-0000
    affiliation: 2
affiliations:
  - name: First Affiliation
    index: 1
  - name: ELIXIR Europe
    ror: 044rwnt51
    index: 2
```

# Formatting

This document use Markdown and you can look at [this tutorial](https://www.markdowntutorial.com/).

## Subsection level 2

Please keep sections to a maximum of only two levels.

## Tables

Tables can be added in the following way, though alternatives are possible:

```markdown
Table: Note that table caption is automatically numbered and should be
given before the table itself.

| Header 1 | Header 2 |
| -------- | -------- |
| item 1 | item 2 |
| item 3 | item 4 |
```

This gives:

Table: Note that table caption is automatically numbered and should be
given before the table itself.

| Header 1 | Header 2 |
| -------- | -------- |
| item 1 | item 2 |
| item 3 | item 4 |

## Figures

A figure is added with:

```markdown
![Caption for BioHackrXiv logo figure](./biohackrxiv.png)
```

This gives:

![Caption for BioHackrXiv logo figure](./biohackrxiv.png)

Figures can be scaled by adding the width or height to the Markdown like this:

```markdown
![Caption for BioHackrXiv logo figure](./biohackrxiv.png){ width=50px }
```

# Other main section on your manuscript level 1

Lists can be added with:

1. Item 1
2. Item 2

# Citation Typing Ontology annotation

You can use [CiTO](http://purl.org/spar/cito/2018-02-12) annotations, as explained in [this BioHackathon Europe 2021 write up](https://raw.githubusercontent.com/biohackrxiv/bhxiv-metadata/main/doc/elixir_biohackathon2021/paper.md) and [this CiTO Pilot](https://www.biomedcentral.com/collections/cito).
Using this template, you can cite an article and indicate _why_ you cite that article, for instance DisGeNET-RDF [@citesAsAuthority:Queralt2016].

The syntax in Markdown is as follows: a single intention annotation looks like
`[@usesMethodIn:Krewinkel2017]`; two or more intentions are separated
with colons, like `[@extends:discusses:Nielsen2017Scholia]`. When you cite two
different articles, you use this syntax: `[@citesAsDataSource:Ammar2022ETL; @citesAsDataSource:Arend2022BioHackEU22]`.

Possible CiTO typing annotation include:

* citesAsDataSource: when you point the reader to a source of data which may explain a claim
* usesDataFrom: when you reuse somehow (and elaborate on) the data in the cited entity
* usesMethodIn
* citesAsAuthority
* citesAsEvidence
* citesAsPotentialSolution
* citesAsRecommendedReading
* citesAsRelated
* citesAsSourceDocument
* citesForInformation
* confirms
* documents
* providesDataFor
* obtainsSupportFrom
* discusses
* extends
* agreesWith
* disagreesWith
* updates
* citation: generic citation


# Results


# Discussion

...

## Acknowledgements

...

## References
