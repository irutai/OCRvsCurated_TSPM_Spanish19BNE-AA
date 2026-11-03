# OCRvsCurated_TSPM_Spanish19BNE-AA
Paired OCR / curated full-length Spanish texts (30 documents: 15 OCR works from Spanish19BNE-AA and each corresponding curated work) used to evaluate the Transferable Shared–Private Mixture (TSPM).

This repository contains the text data used in the paper introducing **TSPM**, a probabilistic framework that separates two related textual collections into a *shared* lexical component and *condition-specific (private)* components, and transfers the learned representation to unseen text. Here the two conditions are:

- **OCR**: digitized 19th–20th century editions from the Biblioteca Nacional de España (BNE), in particular from Spanish19BNE-AA dataset.
- **Curated**: more recent, manually curated digital editions of the same works.

## Origin of the data

### OCR texts: Spanish19BNE-AA

The OCR texts are a subset of the **Spanish19BNE-AA** dataset ([github.com/irutai/Spanish19BNE-AA](https://github.com/irutai/Spanish19BNE-AA)), a large-scale authorship-attribution dataset of OCR transcriptions from the BNE digitized collections (8,041 works by 425 authors, Spanish, 19th–20th centuries). The chosen files are copied from that dataset, which have been adapted --both the curated and the OCR-based texts-- to trim a percentage of the works at the beginning and at the end to avoid indices and some prologues, trying to skip author's name, and BNE or title headers and footers whenever possible. For the full structure, provenance manifest and licensing analysis, please refer to the original repository, which should also be cited when using these texts.

### Curated texts

| Source | Works |
|---|---|
| [Project Gutenberg](https://www.gutenberg.org) | 14 works (Gutenberg ebook number in the file name) |
| [Biblioteca Virtual Miguel de Cervantes](https://www.cervantesvirtual.com/obra/critica-popular-2015/) | *La crítica popular* (Leopoldo Alas "Clarín"), 2015 edition |

Curated texts were restricted to the substantive text (prologues, appendices and other peripheral material excluded), as were the OCR counterparts. Minor editorial, orthographic and segmentation differences remain, so the pairs are **not token-aligned**.


## Contents

15 works by 8 different authors, each in two manifestations: OCR and curated in the folder OCRvsCurated_texts

```
OCR/        # one file per work, from Spanish19BNE-AA
Curated/    # matching curated edition (files marked _OK_)
```

File naming:
- OCR: `<BNE_code>_<year>_<Author>_<birth>-<death>.txt`
- Curated: `<BNE_code>_OK_<year>_<Author>_<birth>-<death>[_pg<Gutenberg_no>]_<title>.txt`

The `<year>` is that of the BNE edition and is shared by both files of a pair.


## Intended use

Studying systematic differences between OCR and curated manifestations of the same works, shared–private modelling, OCR-noise characterisation, and transfer to unseen works (the paper uses work-seen and leave-one-pair-out protocols).


## Licensing and rights
Original contributions of this repository (selection, pairing, documentation) are offered under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/), following Spanish19BNE-AA. This repository does not relicense any underlying work. Please check each source:

- **OCR texts**: © original sources. Data source: **Biblioteca Nacional de España**, via Spanish19BNE-AA. See that repository's *provenance, public-domain status and reuse rights* section and the [BNE legal notice](https://www.bne.es/es/aviso-legal).
- **Project Gutenberg texts**: the underlying works are in the public domain. Texts were adapted (peripheral material and Gutenberg boilerplate removed). Gutenberg's [terms of use](https://www.gutenberg.org/policy/permission.html) apply to the name "Project Gutenberg" and to unmodified distribution of its files.
- **Biblioteca Virtual Miguel de Cervantes text**: obtained from [this page](https://www.cervantesvirtual.com/obra/critica-popular-2015/). Please consult the site's [legal conditions](https://www.cervantesvirtual.com) for the reuse terms of this edition.


### Attribution Requirement
If you use, modify, or distribute this work, you must give appropriate credit by citing the following papers:

, 2026.
DOI:  https://doi.org/xxx

In addition, you must indicate if changes were made and include a link to this repository.
