---
layout: default
permalink: /
---

Welcome to The Official PyThaiNLP Project Website.

The PyThaiNLP Project is a Thai Natural Language Processing project. We build softwares and datasets for Thai language. Our Main Project is PyThaiNLP.

**See all our project at [pythainlp.github.io/projects/](https://pythainlp.github.io/projects/)**

**สำหรับภาษาไทย คุณสามารถเยี่ยมชมเว็บภาษาไทยของ PyThaiNLP ได้ที่ [pythainlp.github.io/th/](https://pythainlp.github.io/th/)**

PyThaiNLP is a Python package for text processing and linguistic analysis, similar to nltk, with focus on Thai language.

## PyThaiNLP Features
- Convenient character and word classes, like Thai consonants (pythainlp.thai_consonants), vowels (pythainlp.thai_vowels), digits (pythainlp.thai_digits), and stop words (pythainlp.corpus.thai_stopwords) -- comparable to constants like string.letters, string.digits, and string.punctuation
- Thai linguistic unit segmentation/tokenization, including sentence (sent_tokenize), word (word_tokenize), and subword segmentations based on Thai Character Cluster (subword_tokenize)
- Thai part-of-speech tagging (pos_tag)
- Thai spelling suggestion and correction (spell and correct)
- Thai transliteration (transliterate)
- Thai soundex (soundex) with three engines (lk82, udom83, metasound)
- Thai collation (sort by dictionary order) (collate)
- Read out number to Thai words (bahttext, num_to_thaiword)
- Thai datetime formatting (thai_strftime)
- Thai-English keyboard misswitched fix (eng_to_thai, thai_to_eng)
- Command-line interface for basic functions, like tokenization and pos tagging (run thainlp in your shell)

Please see [our tutorials](https://pythainlp.github.io/tutorials) on how to apply these functions to machine-learning problems.

## Who uses PyThaiNLP?

You can read at [INTHEWILD.md](https://github.com/PyThaiNLP/pythainlp/blob/dev/INTHEWILD.md).

## Development Lead
- Wannaphong Phatthiyaphaibun - founder, distribution and maintainance
- Korakot Chaovavanich - initial tokenization and soundex code
- Charin Polpanumas - classification and benchmarking
- Arthit Suriyawongkul - refactoring, packaging, distribution, and maintainance
- Chakri Lowphansirikul - documentation
- Pattarawat Chormai - benchmarking
- Thanathip Suntorntip - nlpO3 maintainance, Rust Developer
- Can Udomcharoenchaikit - documentation and code


## Sponsors

| Logo | Description |
| --- | ----------- |
| [![VISTEC-depa Thailand Artificial Intelligence Research Institute](https://airesearch.in.th/assets/img/logo/airesearch-logo.svg)](https://airesearch.in.th/)   | Since 2019, our contributors Korakot Chaovavanich and Lalita Lowphansirikul have been supported by [VISTEC-depa Thailand Artificial Intelligence Research Institute](https://airesearch.in.th/).                 |
| [![MacStadium](https://i.imgur.com/rKy1dJX.png)](https://www.macstadium.com)   | We get support free Mac Mini M1 from [MacStadium](https://www.macstadium.com) for doing Build CI.                  |


<div align="center">
  Made with ❤️ | PyThaiNLP Team 💻 |  "We build Thai NLP" 🇹🇭
</div>