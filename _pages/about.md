---
layout: page
title: About PyThaiNLP
permalink: /about/
---

PyThaiNLP Project is an open source community for natural Language Processing project in the Thai language. We build softwares and datasets for Thai language. Our Main Project is PyThaiNLP.

## About Project

Our project are open source. We create softwares, models, and datasets for Thai language to public and are open source license.

**See all our project at [pythainlp.org/projects/](https://pythainlp.org/projects/)**

Hugging Face: [https://huggingface.co/pythainlp](https://huggingface.co/pythainlp)


## About PyThaiNLP

PyThaiNLP is a Python package for text processing and linguistic analysis, similar to nltk, with focus on Thai language.

See: [Our Paper](https://aclanthology.org/2023.nlposs-1.4/)

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
