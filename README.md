# Gender Bias in English-to-Greek Machine Translation

This repo contains code and data associated with MA thesis on Gender Bias in English-to-Greek Machine Translation.

## Abstract
In recent years, concern has grown over the susceptibility of machine translation (MT) systems to reinforce gender stereotypes. This study investigates gender bias in two commercial MT systems, Google Translate and DeepL, focusing on the understudied English-to-Greek language pair. Specifically, we address three aspects of gender bias: _i)_ male bias (defaulting to masculine forms), _ii)_ occupational stereotyping (assigning gender based on occupational stereotypes), and _iii)_ errors in anti-stereotypical translations (e.g. more frequent mistranslations of "female doctors" versus "male doctors"). We also explore the potential of prompted GPT-4o as a gender rewriter capable of mitigating gender bias by providing gendered and gender-neutral alternatives. To achieve this, we introduce **GendEL**, a manually crafted dataset of 240 gender-ambiguous and unambiguous English sentences, featuring stereotypical occupational nouns and adjectives. We find that gender bias is persistent in translations by both MT systems; while they perform well in cases where gender is explicitly defined – with DeepL outperforming both Google Translate and GPT-4o in the feminine gender-unambiguous sentences – they are far from producing gender-inclusive translations when the gender remains undefined. In contrast, prompted GPT-4o emerges as a promising solution for gender-inclusive translations as it offers gendered and gender-neutral alternatives for most ambiguous sentences, though some residual biases remain evident. Finally, we discuss the limitations of the models and dataset, and we open source our contributions to encourage further research in English-to-Greek machine translation.

## Contents
* **Gkovedarou_MA_thesis_06012026.pdf**: MA thesis paper
* **data** folder:
    - **GendEL.xlsx**: Full GendEL dataset with human translations, translations by Google Translate, DeepL and prompted GPT-4o, and annotations.
    - **GendEL_set_MT.csv**: Subset of GendEL including only the translations by Google Translate and DeepL (used for the uploaded code).
    - **GendEL_set_LLM.csv**: Subset of GendEL including only the translations by prompted GPT-4o (used for the uploaded code). 
* **code** folder:
    - **evaluation.ipynb**: Code for the evaluation of the translations produced by Google Translate, DeepL and prompted GPT-4o to assess the presence of gender bias in the outputs.
    - **prompted_gpt_4o.iynb**: Code for the prompting of GPT-4o, specifically customised for EN-EL gender-inclusive translations.
* **figures** folder: Contains all the plots/visualisations presented in the study.
    
## Contributions
Contributions of this study: (1) the creation and public release of **GendEL**, the first handcrafted dataset for evaluating English-to-Greek translations, and (2) emphasis on the need for more gender-inclusive translation practices in Greek.

## Citing
```
@mastersthesis{Gkovedarou25thesis,
  author    = {Eleni Gkovedarou},
  title     = {Gender Bias in English-to-Greek Machine Translation},
  year      = {2025},
  month     = {January},
  address   = {Antwerp, Belgium},
  school    = {University of Antwerp},
  type      = {Master's thesis}
}
```
