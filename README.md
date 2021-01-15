# VOC missives data

This repository provides NAF-formatted data of the VOC [Generale Missiven](http://resources.huygens.knaw.nl/vocgeneralemissiven),
as well as a corpus of named-entity annotations created as part of [Clariah WP6](https://www.clariah.nl/en/work-packages/focus-areas/text?layout=blog), in cooperation with [INT](https://ivdnt.org/) and [Huygens ING](https://www.huygens.knaw.nl/).

## Generale Missiven

The Generale Missiven are given in TEI form (`generale-missiven/tei`), as prepared by INT. Conversion to NAF (`generale-missiven/naf`) and selection of textual/editorial content (`generale-missiven/text-and-notes`) were performed by the VU; see [voc-missives](https://cltl.github.io/voc-missives/) for the code.

## Named-Entity annotations

Manual annotations were prepared by Huygens ING (see `NER-annotations/manual`, and delivered in three parts:

* 31/03/20: annotations based on raw text input, and formatted in UIMA CAS XMI
* 20/05/20: annotations based on system input, and formatted in Conll 2002
* 17/06/20: annotations based on raw text input, and formatted in UIMA CAS XMI

The text input for the first and third parts was extracted from TEI with [teiReader](https://github.com/cltl/teiReader), and manually annotated by Huygens ING. 

The second part corresponds to a single missive, which was converted from TEI to Conll with an earlier version of the [voc-missives](https://cltl.github.io/voc-missives/) code, and enriched with NER system annotations. The NER system used was that of [Reimers and Gurevych (2017)](https://arxiv.org/abs/1707.09861), trained on the first group of annotations. The annotations were then corrected by Huygens ING. 

Manual annotations were integrated into reference NAF files (see `generale-missiven/text-and-notes`) and written to `NER-annotations/naf`, and then converted to Conll2002 (`NER-annotations/conll`) with the [voc-missives](https://cltl.github.io/voc-missives/) code.

## Authors

* Sophie Arnoult (VU): s.i.arnoult@vu.nl
* Jesse de Does (INT)
* Lodewijk Petram (Huygens ING)
