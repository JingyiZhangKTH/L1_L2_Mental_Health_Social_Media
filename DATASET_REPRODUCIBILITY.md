# Dataset Reproducibility Guide

**Paper:** *The Impact of Non-Native English on Emotion and Mental
Health Condition Classification in Social Media Text*  
**Venue/version:** EACL 2027 Main Conference


This document lists the datasets and source corpora identified in the
paper, with links to the original sources, access routes, and practical
notes for reproduction. The corpus sizes below are copied from **Table 1
of the paper** unless explicitly marked otherwise. They describe the
amounts reported as used in the experiments; they are not necessarily
the current official corpus sizes.


## 1. At-a-glance access summary

| Resource                            | Access route                                                       |                                           Must contact/request access? | Important restriction                                                       |
|-------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------:|-----------------------------------------------------------------------------|
| BNC2014 Written                     | Free corpus search through \#LancsBox X                            |                          No for search; full-text download unavailable | Copyright; full written texts cannot currently be released                  |
| Brown Corpus                        | Direct NLTK download                                               |                                                                     No | Non-commercial use only                                                     |
| LOCNESS                             | Complete the CECL/Learner Corpus Association form                  |                                                       Yes: submit form | Non-commercial; no redistribution                                           |
| OANC                                | Direct download                                                    |                                                                     No | Open/unrestricted                                                           |
| AMALGUM                             | Public GitHub release; complete Reddit-containing version by email |                                  Only for complete version with Reddit | Underlying source texts have their own terms                                |
| COREFL                              | Public Search/Download interface                                   |                                                                     No | CC BY-NC-ND 3.0 ES                                                          |
| ICNALE                              | Register to receive archive password                               |               Registration required; no separate owner approval stated | Redistribution prohibited                                                   |
| Lang-8 Learner Corpus               | Submit download form                                               |                                Yes: form with name, email, affiliation | Research/education only; commercial use requires Lang-8 contact             |
| NUCLE                               | Public Hugging Face repository                                     |                            No individual request; agree to NUS licence | NUS licence agreement applies                                               |
| CAWSE                               | University of Leeds RADAR restricted repository                    |                                  Yes: access request with intended use | Restricted access; response stated as within 10 working days                |
| Write & Improve (W&I)               | Complete Cambridge registration form and licence                   |                                                 Yes: registration form | Non-commercial only; no redistribution; approval needed for derived outputs |
| ELFA transcripts                    | Direct download via Language Bank of Finland                       |                                                     No for transcripts | CC BY; audio requires individual access rights                              |
| JFLEG                               | Public GitHub repository                                           |                                                                     No | CC BY-NC-SA 4.0                                                             |
| L2-Reddit / Reddit L1-L2            | Original project link cited by the paper                           | Original link currently appears unavailable; contact authors if needed | Reddit platform terms still apply                                           |
| ENNTT                               | Public GitHub repository                                           |                  No for repository download; ask authors about licence | Repository does not state a clear licence                                   |
| Reddit Mental Health Dataset (RMHD) | Direct Zenodo download                                             |                                                                     No | PDDL 1.0 dataset licence; Reddit API terms also apply                       |
| Universal Joy                       | Direct GitHub release / Zenodo                                     |                                                                     No | CC BY 4.0                                                                   |

**Status meanings**

- **Direct download:** the source provides a public download route
  without a personal access request.
- **Registration/licence:** a form, account, password, or click-through
  licence is required before use.
- **Request access:** the owner or repository must approve an access
  request.
- **Unclear/unavailable:** the historical source is documented, but a
  current, working download route or a clear licence could not be
  confirmed.

------------------------------------------------------------------------

## 2. L1/L2 identification corpus

The paper builds its L1/L2 identification data by combining multiple
corpora. Table 1 contains **17 labelled source entries**: six L1-only
corpora, seven L2-only corpora, and two mixed L1/L2 corpora (Reddit and
ENNTT). The mixed corpora contribute one L1 and one L2 entry each.

### 2.1 L1-only source corpora

| Corpus                                 | Label in paper | Words reported in paper | Original source / download                                                                                                                                                  | Access and reproduction notes                                                                                                                                                                                                                                                                                                                                                                                                         | Dataset reference                                                                                                            |
|----------------------------------------|---------------:|------------------------:|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| British National Corpus 2014 (BNC2014) |             L1 |                    668K | [BNC2014 project](https://corpora.lancs.ac.uk/bnc2014/) · [CASS access guide](https://cass.lancs.ac.uk/bnc2014/)                                                            | The paper cites the **Written BNC2014**. It can be searched free through \#LancsBox X, but the full written texts cannot currently be released for download because of copyright. The spoken component has a separate user-licence and registration route; it is not a substitute for the written component.                                                                                                                          | Brezina, Hawtin & McEnery (2021), *The Written British National Corpus 2014: Design and Comparability*.                      |
| Brown Corpus                           |             L1 |                      1M | [NLTK Brown package](https://raw.githubusercontent.com/nltk/nltk_data/gh-pages/packages/corpora/brown.zip) · [NLTK data instructions](https://www.nltk.org/data)            | Direct download via NLTK; no individual owner request is indicated. NLTK lists the Brown Corpus as **non-commercial use only**.                                                                                                                                                                                                                                                                                                       | Francis & Kucera (1979), *A Standard Corpus of Present-Day Edited American English*.                                         |
| LOCNESS                                |             L1 |                    281K | [LOCNESS access page](https://www.learnercorpusassociation.org/resources/tools/locness-corpus/) · [CECL page](https://uclouvain.be/en/research-institutes/ilc/cecl/locness) | Complete the access form and agree to the licence. Non-commercial use only; publications must acknowledge CECL; do not redistribute the corpus to third parties without CECL permission. The current access page reports 324,304 words, whereas the paper reports 281K—use the paper’s figure only as the amount it says it used.                                                                                                     | Granger (1998), *The Computer Learner Corpus: A Versatile New Source of Data for SLA Research*.                              |
| Open American National Corpus (OANC)   |             L1 |                     15M | [OANC download page](https://anc.org/data/oanc/download/) · [OANC description](https://anc.org/data/oanc/)                                                                  | Freely downloadable. The OANC project describes the corpus as unrestricted for use and redistribution, including commercial use.                                                                                                                                                                                                                                                                                                      | Open American National Corpus (2024), [official site](https://anc.org/).                                                     |
| AMALGUM                                |             L1 |                      3M | [AMALGUM GitHub repository](https://github.com/gucorpling/amalgum) · [Corpus paper](https://aclanthology.org/2020.lrec-1.648/)                                              | The public repository contains the release **without Reddit texts**. The repository says the complete corpus including Reddit data is available by request from `lg876@georgetown.edu`. The corpus paper describes about 4M tokens, while this paper reports 3M words; confirm the exact snapshot/subset used. Annotation licence and underlying source-text terms are not identical: check the repository and source-specific terms. | Gessler et al. (2020), *AMALGUM – A Free, Balanced, Multilayer English Web Corpus*.                                          |
| COREFL (native-English control subset) |             L1 |                     17K | [COREFL Search/Download](https://corefl.learnercorpora.com/search) · [COREFL home and licence](https://corefl.learnercorpora.com/)                                          | Publicly searchable and freely downloadable without an owner request. Current site identifies version 2.0 (October 2025), under CC BY-NC-ND 3.0 ES. The paper uses the COREFL L1/native-English portion for training and reserves the L2 learner portion for a separate proficiency-based evaluation. Pin the version used; the current website may not be byte-identical to the version used in the paper.                           | Lozano, Díaz-Negrillo & Callies (2020), *Designing and Compiling a Learner Corpus of Written and Spoken Narratives: COREFL*. |

### 2.2 L2-only source corpora

| Corpus                                                           | Label in paper | Words reported in paper | Original source / download                                                                                                                                                                                                 | Access and reproduction notes                                                                                                                                                                                                                                                                                                                                                       | Dataset reference                                                                                                     |
|------------------------------------------------------------------|---------------:|------------------------:|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| ICNALE                                                           |             L2 |                      1M | [ICNALE download page](https://language.sakura.ne.jp/icnale/download.html)                                                                                                                                                 | Register through the ICNALE User Registration Form linked on the download page. Registered users receive the password needed to unzip the files. This is a registration/password step, not an owner-approved research proposal according to the current instructions. The terms prohibit reproducing or redistributing any part of the data.                                        | Ishikawa (2023), *The ICNALE Guide: An Introduction to a Learner Corpus Study on Asian Learners’ L2 English*.         |
| Lang-8 Learner Corpus                                            |             L2 |                      6M | [NAIST Lang-8 Learner Corpora](https://sites.google.com/site/naistlang8corpora) · [download request form](https://docs.google.com/forms/d/17gZZsC_rnaACMXmPiab3kjqBEtRHPMz0UG9Dk-x_F0k/viewform)                           | The download page asks for name, email address, and affiliation. The corpus is for research and educational purposes; commercial use requires contacting Lang-8 (`support@lang-8.com`). The site lists an English learner corpus v1.0 with 100,051 English entries and a multilingual raw corpus v2.0. Confirm which release and preprocessing produced the paper’s 6M-word figure. | Tajiri, Komachi & Matsumoto (2012), *Tense and Aspect Error Correction for ESL Learners Using Global Context*.        |
| NUCLE (NUS Corpus of Learner English)                            |             L2 |                    301K | [NUCLE dataset card and files](https://huggingface.co/datasets/nusnlp/NUCLE) · [NUS NLP data page](https://www.comp.nus.edu.sg/~nlp/corpora.html)                                                                          | Publicly downloadable. By downloading, users agree to the standard NUS licensing agreement; no separate owner approval is stated. Questions: `nght@nus.edu.sg`. The official description reports about 1,400 essays and over one million words; the paper reports 301K words, so record the exact subset/preprocessing used.                                                        | Dahlmeier, Ng & Wu (2013), *Building a Large Annotated Corpus of Learner English: The NUS Corpus of Learner English*. |
| CAWSE (Corpus of Chinese Academic Written and Spoken English)    |             L2 |                    985K | [University of Leeds data record](https://archive.researchdata.leeds.ac.uk/1568/) · [RADAR dataset record](https://radar.researchdata.leeds.ac.uk/81/) · [historical CAWSE site](https://cawse.transcribear.com/)          | The current University of Leeds record places the data in a **Restricted Access Data Repository**. Submit a request form and state the intended use; the record says an initial response is normally sent within 10 working days. Do not assume that the older Transcribear page provides unrestricted access. Contact listed on the record: `y.chen8@leeds.ac.uk`.                 | Chen et al. (2019), *CAWSE: The UNNC Corpus of Chinese Academic Written and Spoken English*.                          |
| Write & Improve Corpus (W&I)                                     |             L2 |                    454K | [Cambridge ELiT dataset page](https://researchdatasets.cambridge.org/datasets/write-and-improve-corpus-2024)                                                                                                               | Complete the registration form on the dataset page and agree to the licence. Non-commercial research/education only. The licence is non-transferable; the corpus (whole or partial) must not be shared with others, including via GitHub/Hugging Face. Derived outputs (including models/statistics) require prior CUP&A approval. Contact: `researchdatasets@cambridge.org`.       | Nicholls, Caines & Buttery (2024), *The Write & Improve Corpus 2024*.                                                 |
| ELFA (Corpus of English as a Lingua Franca in Academic Settings) |             L2 |                    630K | [University of Helsinki ELFA page](https://www.helsinki.fi/en/researchgroups/english-as-a-lingua-franca-in-academic-settings/research/elfa-corpus) · [Kielipankki resource page](https://www.kielipankki.fi/corpora/elfa/) | The **transcripts** are publicly available for download in plain-text/XML formats under CC BY. The audio files are a different resource and require individual access rights because they contain personal data. For this paper’s text-based experiment, use the transcript download, not the restricted audio.                                                                     | Mauranen (2008), *ELFA: The Corpus of English as a Lingua Franca in Academic Settings*.                               |
| JFLEG                                                            |             L2 |                     14K | [JFLEG GitHub repository](https://github.com/keisks/jfleg)                                                                                                                                                                 | Direct public download from GitHub; no individual request is indicated. Repository states CC BY-NC-SA 4.0. Follow the repository’s citation instructions and use the latest version available there.                                                                                                                                                                                | Napoles, Sakaguchi & Tetreault (2017), *JFLEG: A Fluency Corpus and Benchmark for Grammatical Error Correction*.      |

### 2.3 Mixed L1/L2 source corpora

| Corpus                                                             | Label in paper | Words reported in paper | Original source / download                                                                                                                   | Access and reproduction notes                                                                                                                                                                                                                                                                                                                                                                       | Dataset reference                                                                                           |
|--------------------------------------------------------------------|----------------|------------------------:|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| L2-Reddit / Reddit L1                                              | L1             |                   40.1M | [Rabinovich et al. (2018) paper](https://aclanthology.org/Q18-1024/) · [historical project download URL](https://cl.haifa.ac.il/projects/L2) | The original paper says the anonymized dataset would be freely available at the project URL. That URL did not respond during this access check. If it remains unavailable, contact the authors. The paper says released data does not expose author-identifying information. Reddit data reuse remains subject to Reddit’s applicable terms.                                                        |                                                                                                             |
| L2-Reddit / Reddit L2                                              | L2             |                  257.9M | Same source as above                                                                                                                         | Same corpus and access caveat. The source paper describes posts from users whose country flair was used to infer native-language background; this is not a self-reported language annotation for every post. Do not substitute a newly scraped Reddit corpus or Pushshift dump and call it the same dataset.                                                                                        | Rabinovich, Tsvetkov & Wintner (2018), *Native Language Cognate Effects on Second Language Lexical Choice*. |
| ENNTT (Europarl corpus of Native, Non-native and Translated Texts) | L1             |                   3.04M | [ENNTT GitHub repository](https://github.com/senisioi/enntt-release)                                                                         | Repository and release files are public. However, the repository does not state a clear dataset licence; contact the authors before redistribution or any use that requires explicit permission. The README lists `sergiu.nisioi@gmail.com` and `ellarabi@csweb.haifa.ac.il` for questions. The paper uses the native and non-native English portions; the corpus also contains translated English. |                                                                                                             |
| ENNTT (Europarl corpus of Native, Non-native and Translated Texts) | L2             |                    760K | Same source as above                                                                                                                         | Same access and licence caveat.                                                                                                                                                                                                                                                                                                                                                                     | Nisioi, Rabinovich, Dinu & Wintner (2016), *A Corpus of Native, Non-native and Translated Texts*.           |

------------------------------------------------------------------------

## 3. Downstream mental-health classification dataset

### Reddit Mental Health Dataset (RMHD)

- **Paper citation:** Low et al. (2020).
- **Dataset record:** [Zenodo: Reddit Mental Health
  Dataset](https://zenodo.org/records/3941387).
- **Download:** Direct from Zenodo; no owner request or registration is
  indicated.
- **Licence:** Public Domain Dedication and License (PDDL) v1.0. The
  Zenodo record explicitly notes that the data was collected using
  Pushshift and that reuse is also subject to Reddit API terms.
- **Source coverage:** Posts from 28 subreddits, covering 2018–2020. The
  Zenodo record lists 15 specific mental-health support groups, two
  broad mental-health subreddits, and 11 non-mental-health subreddits.
- **Paper’s selection:**
  - ADHD: `r/adhd`
  - Anxiety: combined `r/socialanxiety` and `r/healthanxiety`
  - Depression: `r/depression`
  - Suicide: `r/suicidewatch`
  - Non-mental-health control: `r/fitness` and `r/teaching`
- **Important interpretation:** The paper assigns categories based on
  the source subreddit. These are **topic-based subreddit labels**, not
  clinical diagnoses and not proof that an individual author has a
  condition.
- **Paper’s preprocessing:** The source dataset contains approximately
  110K posts in the paper’s selected set. Posts are split into
  non-overlapping 100-word chunks; the paper then retains only L1/L2
  predictions with confidence ≥ 0.90.

**Citation**

Low, D. M., Rumker, L., Talkar, T., Torous, J., Cecchi, G., & Ghosh, S.
S. (2020). Natural Language Processing Reveals Vulnerable Mental Health
Support Groups and Heightened Health Anxiety on Reddit During COVID-19:
Observational Study. *Journal of Medical Internet Research*, 22(10),
e22635. <https://doi.org/10.2196/22635>

------------------------------------------------------------------------

## 4. Downstream emotion-classification dataset

### Universal Joy (English subset)

- **Paper citation:** Lamprinidis et al. (2021).
- **Dataset release:** [GitHub
  release](https://github.com/sotlampr/universal-joy/releases/tag/dataset-models).
- **Dataset DOI:** [Zenodo record
  4620610](https://doi.org/10.5281/zenodo.4620610).
- **Download:** Direct public download; no owner request or registration
  is indicated.
- **Licence:** Creative Commons Attribution 4.0 International (CC BY
  4.0), according to the Zenodo record.
- **Original dataset:** More than 530,000 anonymized public Facebook
  posts across 18 languages, labelled with five emotions.
- **Paper’s English labels:** anger, anticipation, fear, joy, and
  sadness.
- **Paper’s preprocessing:** Uses the English subset; retains L1/L2
  predictions with confidence ≥ 0.90 and removes posts shorter than 50
  words. Each retained post is one input (no 100-word segmentation). The
  paper reports **9,631 retained English posts** after filtering.

**Citation**

Lamprinidis, S., Bianchi, F., Hardt, D., & Hovy, D. (2021). Universal
Joy: A Data Set and Results for Classifying Emotions Across Languages.
In *Proceedings of the Eleventh Workshop on Computational Approaches to
Subjectivity, Sentiment and Social Media Analysis (WASSA 2021)*,
pp. 62–75. [ACL Anthology](https://aclanthology.org/2021.wassa-1.7/).

------------------------------------------------------------------------

## 5. Reproduction workflow and preprocessing details from the paper

This section records the paper’s stated pipeline. It is not a substitute
for the released code; use the final code/model release when available.

### 5.1 L1/L2 identification corpus

1.  Obtain the source corpora listed in Section 2, subject to each
    source’s access terms.
2.  Preserve the original source and label provenance for every
    document.
3.  Split texts into **non-overlapping 100-word blocks**.
4.  Discard residual segments shorter than **50 words**.
5.  Use a **70/15/15 train/development/test split**, preserving the
    L1/L2 distribution.
6.  Use class-weighted cross-entropy to address class imbalance.
7.  The paper selects RoBERTa-base as its best-performing L1/L2
    classifier.
8.  For downstream assignment, retain only predictions with confidence
    **≥ 0.90**. The paper reports macro-F1 of 0.95 on this
    high-confidence subset.

### 5.2 Mental-health classification

1.  Start from the RMHD source posts and select the subreddits listed in
    Section 3.
2.  Assign the paper’s topic categories based on subreddit.
3.  Apply the L1/L2 classifier and retain predictions with confidence ≥
    0.90.
4.  Segment posts into non-overlapping 100-word chunks.
5.  Follow the paper’s 70/15/15 stratified split and class-weighted
    training setup.
6.  Report metrics separately for L1 and L2 subsets.

### 5.3 Emotion classification

1.  Obtain the Universal Joy release and select the English subset.
2.  Apply the L1/L2 classifier and retain predictions with confidence ≥
    0.90.
3.  Remove posts shorter than 50 words.
4.  Use each remaining post as one input; do not split it into 100-word
    chunks.
5.  Preserve the five emotion labels: anger, anticipation, fear, joy,
    sadness.
6.  Follow the paper’s 70/15/15 stratified split and class-weighted
    training setup.

### 5.4 What to record for a reproducible release

For every downloaded source, record:

- Original dataset name and URL
- Dataset version/release date
- Date downloaded
- Licence or access agreement version
- File name(s) and SHA-256 checksum(s)
- Exact subset and fields used
- Number of documents/posts before filtering
- Number of items after filtering and segmentation
- Random seed and split identifiers
- Any transformations, deduplication, text cleaning, or exclusion rules

Do not put restricted data, raw text, or prohibited derived outputs in
this repository. Where redistribution is prohibited, provide the
official access route and a script that runs after the user obtains
their own licensed copy.

------------------------------------------------------------------------

## 6. Items to clarify before claiming exact reproduction

The following points are visible in the submitted paper and should be
checked against the final code or author-side data manifests:

1.  **Mental-health count discrepancy:** Section 4.1 states that the
    final mental-health corpus contains **147,994 chunks**, but Table
    2’s category counts sum to **110,616** (83,122 L1 + 27,494 L2). The
    final release should explain which number is correct and whether the
    difference reflects an additional filtering or counting stage.
2.  **BNC2014 access:** The paper cites the Written BNC2014. The
    official CASS page says the written corpus can be searched via
    \#LancsBox X but that the full written texts cannot currently be
    released. Explain how the 668K-word subset was obtained and which
    files or query/export were used.
3.  **LOCNESS size:** The paper reports 281K words; the current LOCNESS
    access page reports 324,304 words. Identify the exact release and
    any exclusions/preprocessing.
4.  **NUCLE size:** The NUS description reports over one million words;
    the paper reports 301K. Identify the exact subset and filtering.
5.  **AMALGUM size/version:** The AMALGUM paper describes about 4M
    tokens, while this paper reports 3M words. The public GitHub release
    excludes Reddit texts, while the complete Reddit-containing version
    is available by request. Identify the precise snapshot used.
6.  **COREFL evaluation:** The paper says the COREFL L2 portion is held
    out for a separate proficiency-based evaluation, even though Table 1
    lists only the COREFL L1 training portion. Include the COREFL L2
    evaluation procedure and version in the final reproduction
    materials.
7.  **L2-Reddit availability:** The original paper’s project download
    URL did not respond during this check. Confirm a working official
    download route or document author contact and the exact archive
    version.
8.  **CAWSE version:** The current Leeds repository is restricted access
    and may differ in metadata from the earlier 2019 release. Record the
    precise release obtained.
9.  **W&I redistribution:** Cambridge’s terms prohibit redistribution of
    the corpus and require prior approval for derived items. Do not
    upload the data, partial samples, models, or statistics derived from
    it unless CUP&A has approved that specific release.

------------------------------------------------------------------------

## 7. References and source links

- Brezina, V., Hawtin, A., & McEnery, T. (2021). The Written British
  National Corpus 2014: Design and Comparability. *Text & Talk*,
  41(5–6), 595–615. [BNC2014
  project](https://corpora.lancs.ac.uk/bnc2014/)
- Chen, Y.-H. et al. (2019). CAWSE: The UNNC Corpus of Chinese Academic
  Written and Spoken English. [CAWSE
  archive](https://archive.researchdata.leeds.ac.uk/1568/)
- Dahlmeier, D., Ng, H. T., & Wu, S. M. (2013). Building a Large
  Annotated Corpus of Learner English: The NUS Corpus of Learner
  English. [ACL Anthology](https://aclanthology.org/W13-1704/) · [NUCLE
  data](https://huggingface.co/datasets/nusnlp/NUCLE)
- Francis, W. N., & Kucera, H. (1979). A Standard Corpus of Present-Day
  Edited American English. [Brown Corpus via
  NLTK](https://raw.githubusercontent.com/nltk/nltk_data/gh-pages/packages/corpora/brown.zip)
- Gessler, L. et al. (2020). AMALGUM – A Free, Balanced, Multilayer
  English Web Corpus. [ACL
  Anthology](https://aclanthology.org/2020.lrec-1.648/) ·
  [GitHub](https://github.com/gucorpling/amalgum)
- Granger, S. (1998). The Computer Learner Corpus: A Versatile New
  Source of Data for SLA Research. [LOCNESS
  access](https://www.learnercorpusassociation.org/resources/tools/locness-corpus/)
- Ishikawa, S. (2023). The ICNALE Guide: An Introduction to a Learner
  Corpus Study on Asian Learners’ L2 English. [ICNALE
  download](https://language.sakura.ne.jp/icnale/download.html)
- Lamprinidis, S., Bianchi, F., Hardt, D., & Hovy, D. (2021). Universal
  Joy: A Data Set and Results for Classifying Emotions Across Languages.
  [ACL Anthology](https://aclanthology.org/2021.wassa-1.7/) ·
  [Zenodo](https://doi.org/10.5281/zenodo.4620610)
- Low, D. M. et al. (2020). Natural Language Processing Reveals
  Vulnerable Mental Health Support Groups and Heightened Health Anxiety
  on Reddit During COVID-19: Observational Study.
  [JMIR](https://doi.org/10.2196/22635) · [Zenodo
  RMHD](https://zenodo.org/records/3941387)
- Lozano, C., Díaz-Negrillo, A., & Callies, M. (2020). Designing and
  Compiling a Learner Corpus of Written and Spoken Narratives: COREFL.
  [COREFL](https://corefl.learnercorpora.com/)
- Mauranen, A. (2008). ELFA: The Corpus of English as a Lingua Franca in
  Academic Settings. [ELFA
  project](https://www.helsinki.fi/en/researchgroups/english-as-a-lingua-franca-in-academic-settings/research/elfa-corpus)
- Napoles, C., Sakaguchi, K., & Tetreault, J. (2017). JFLEG: A Fluency
  Corpus and Benchmark for Grammatical Error Correction. [ACL
  Anthology](https://aclanthology.org/E17-2037/) ·
  [GitHub](https://github.com/keisks/jfleg)
- Nicholls, D., Caines, A., & Buttery, P. (2024). The Write & Improve
  Corpus 2024. [Cambridge ELiT dataset
  page](https://researchdatasets.cambridge.org/datasets/write-and-improve-corpus-2024)
- Nisioi, S., Rabinovich, E., Dinu, L. P., & Wintner, S. (2016). A
  Corpus of Native, Non-native and Translated Texts. [ENNTT
  GitHub](https://github.com/senisioi/enntt-release)
- Open American National Corpus (2024). [OANC
  download](https://anc.org/data/oanc/download/)
- Rabinovich, E., Tsvetkov, Y., & Wintner, S. (2018). Native Language
  Cognate Effects on Second Language Lexical Choice. *Transactions of
  the Association for Computational Linguistics*, 6, 329–342. [ACL
  Anthology](https://aclanthology.org/Q18-1024/)
- Tajiri, T., Komachi, M., & Matsumoto, Y. (2012). Tense and Aspect
  Error Correction for ESL Learners Using Global Context. [ACL
  Anthology](https://aclanthology.org/P12-2040/)
