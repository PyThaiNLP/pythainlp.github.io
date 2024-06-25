---
layout: default
---

Welcome to The Official PyThaiNLP Project Website.

The PyThaiNLP Project is a Thai Natural Language Processing project. We build softwares and datasets for Thai language. Our Main Project is PyThaiNLP.

**See all our project at [pythainlp.org/projects/](https://pythainlp.org/projects/)**

**สำหรับภาษาไทย คุณสามารถเยี่ยมชมเว็บภาษาไทยของ PyThaiNLP ได้ที่ [pythainlp.org/th/](https://pythainlp.org/th/)**

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

Please see [our tutorials](https://pythainlp.org/tutorials) on how to apply these functions to machine-learning problems.

## Who uses PyThaiNLP?

You can read at [INTHEWILD.md](https://github.com/PyThaiNLP/pythainlp/blob/dev/INTHEWILD.md).

## Development Lead
- Wannaphong Phatthiyaphaibun - foundation, distribution and maintenance
- Korakot Chaovavanich - initial tokenization and soundex codes
- Charin Polpanumas - classification and benchmarking
- Arthit Suriyawongkul - refactoring, packaging, distribution, and maintenance
- Lalita Lowphansirikul - documentation
- Pattarawat Chormai - benchmarking
- Peerat Limkonchotiwat
- Thanathip Suntorntip - nlpO3 maintenance, Rust Developer
- Can Udomcharoenchaikit - documentation and codes

## Sponsors

| Logo | Description |
| --- | ----------- |
| [![VISTEC-depa Thailand Artificial Intelligence Research Institute](https://airesearch.in.th/assets/img/logo/airesearch-logo.svg)](https://airesearch.in.th/)   | Since 2019, our contributors Korakot Chaovavanich and Lalita Lowphansirikul have been supported by [VISTEC-depa Thailand Artificial Intelligence Research Institute](https://airesearch.in.th/).                 |
| [![MacStadium](https://i.imgur.com/rKy1dJX.png)](https://www.macstadium.com)   | We get support free Mac Mini M1 from [MacStadium](https://www.macstadium.com) for doing Build CI.                  |


<div align="center">
  Made with ❤️ | PyThaiNLP Team 💻 |  "We build Thai NLP" 🇹🇭
</div>
