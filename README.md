# Gender Bias in English-to-Greek Machine Translation

This repo contains code and data associated with the paper and MA thesis on "Gender Bias in English-to-Greek Machine Translation".


## Abstract
In recent years, concern has grown over the susceptibility of machine translation (MT) systems to reinforce gender stereotypes. This study investigates gender bias in two commercial MT systems, Google Translate and DeepL, focusing on the understudied English-to-Greek language pair. Specifically, we address three aspects of gender bias: _i)_ male bias (defaulting to masculine forms), _ii)_ occupational stereotyping (assigning gender based on occupational stereotypes), and _iii)_ errors in anti-stereotypical translations (e.g. more frequent mistranslations of "female doctors" versus "male doctors"). We also explore the potential of prompted GPT-4o as a gender rewriter capable of mitigating gender bias by providing gendered and gender-neutral alternatives. To achieve this, we introduce GendEL, a manually crafted dataset of 240 gender-ambiguous and unambiguous English sentences that feature stereotypical occupational nouns and adjectives. We find that gender bias is persistent in translations by both MT systems; while they perform well in cases where gender is explicitly defined, with DeepL outperforming both Google Translate and GPT-4o in the feminine gender-unambiguous sentences, they are far from producing gender-inclusive translations when the gender remains unspecified. In contrast, prompted GPT-4o emerges as a promising solution for gender-inclusive translations as it offers gendered and gender-neutral alternatives for most ambiguous sentences, though some residual biases remain evident. Finally, we discuss the limitations of the models and dataset, and we open source our contributions to encourage further research in English-to-Greek machine translation.


## Contents
* **Eleni_Gkovedarou_DTA_thesis.pdf**: MA thesis paper
* **data** folder:
    - **GendEL.csv**: GendEL dataset with handcrafted English sentences and Greek (alternate) translations.
    - **GendEL_set_MT.csv**: Subset of GendEL including the English sentences with Google Translate and DeepL translations (used for evaluation).
    - **GendEL_set_LLM.csv**: Subset of GendEL including the English sentences with GPT-4o translations (used for evaluation). 
* **code** folder:
    - **evaluation.ipynb**: Code for gender bias evaluation of GendEL translations produced by Google Translate, DeepL and prompted GPT-4o.
    - **prompted_gpt_4o.iynb**: Code for the prompting of GPT-4o, specifically customised for EN-EL gender-inclusive translations.
* **figures** folder: Contains all the plots/visualisations presented in the study.


## Contributions
The creation and public release of **GendEL**, the first handcrafted dataset for evaluating English-to-Greek translations.


## Citing
```
@inproceedings{gkovedarou-etal-2025-gender,
    title = "Gender Bias in {E}nglish-to-{G}reek Machine Translation",
    author = "Gkovedarou, Eleni  and
      Daems, Joke  and
      De Bruyne, Luna",
    editor = "Hackenbuchner, Jani{\c{c}}a  and
      Bentivogli, Luisa  and
      Daems, Joke  and
      Manna, Chiara  and
      Savoldi, Beatrice  and
      Vanmassenhove, Eva",
    booktitle = "Proceedings of the 3rd Workshop on Gender-Inclusive Translation Technologies (GITT 2025)",
    month = jun,
    year = "2025",
    address = "Geneva, Switzerland",
    publisher = "European Association for Machine Translation",
    url = "https://aclanthology.org/2025.gitt-1.2/",
    pages = "17--45",
    ISBN = "978-2-9701897-4-9",
    abstract = "As the demand for inclusive language increases, concern has grown over the susceptibility of machine translation (MT) systems to reinforce gender stereotypes. This study investigates gender bias in two commercial MT systems, Google Translate and DeepL, focusing on the understudied English-to-Greek language pair. We address three aspects of gender bias: i) male bias, ii) occupational stereotyping, and iii) errors in anti-stereotypical translations. Additionally, we explore the potential of prompted GPT-4o as a bias mitigation tool that provides both gender-explicit and gender-neutral alternatives when necessary. To achieve this, we introduce GendEL, a manually crafted bilingual dataset of 240 gender-ambiguous and unambiguous sentences that feature stereotypical occupational nouns and adjectives. We find persistent gender bias in translations by both MT systems; while they perform well in cases where gender is explicitly defined, with DeepL outperforming both Google Translate and GPT-4o in feminine gender-unambiguous sentences, they are far from producing gender-inclusive or neutral translations when the gender is unspecified. GPT-4o shows promise, generating appropriate gendered and neutral alternatives for most ambiguous cases, though residual biases remain evident. As one of the first comprehensive studies on gender bias in English-to-Greek MT, we provide both our data and code at \url{https://github.com/elenigkove/genderbias_EN-EL_MT}."
}
```
