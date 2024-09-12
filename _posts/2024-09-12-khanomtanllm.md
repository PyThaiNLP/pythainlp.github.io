---
layout: post
title: KhanomTanLLM: Open Source Thai LLM
gh-repo: pythainlp/pythainlp
gh-badge: [star, fork]
categories: [news]
comments: true
---

![](https://imgur.com/LpQmJqY.png)
> Image gen from [FLUX.1 [dev]](https://huggingface.co/spaces/black-forest-labs/FLUX.1-dev)

วันนี้เรายินดีที่จะเปิดตัว KhanomTanLLM เป็น Open Source language model แรกของภาษาอังกฤษ-ภาษาไทย ที่เทรนด้วยชุดข้อมูลเปิด และปล่อยชุดข้อมูลที่ใช้เทรน LLM ทั้งหมด พร้อม pipeline ในการเทรน และโมเดลที่สามารถนำไปใช้งานในเชิงพาณิชย์ได้ นอกจากนั้นเรายังปล่อยโมเดลทั้งขนาด 1B กับ 3B ถือเป็น small lm ตัวแรกที่ออกแบบมาสำหรับ

หลังจากที่ Phi model ออกมา ได้จุดประกายโมเดล LLM ที่มีขนาดน้อยกว่า 7B ในการใช้งานในโลกจริง แต่โมเดลที่มีขนาด 1B และ 3B ที่รองรับภาษาไทย ยังมีจำนวนน้อย ได้แก่ [gemma-2b](https://huggingface.co/google/gemma-2b), [Qwen2-1.5B](https://huggingface.co/Qwen/Qwen2-1.5B) และ [RWKV](https://huggingface.co/RWKV/) เป็นต้น แต่ทั้งหมดไม่ได้เปิดเผยชุดข้อมูลที่นำมาเทรนโมเดลเพื่อทำ pretrained model สู่สาธารณะ และ gemma-2b ไม่ได้ถูกนับว่าเป็น Open Source ด้วยเงื่อนไขในการใช้งานโมเดล

## Dataset

เราได้ทำการปล่อยชุดข้อมูลสำหรับการทำ Pretrained LLM ตัวนี้ไว้ที่

Pretraining dataset: [https://huggingface.co/datasets/wannaphong/KhanomTanLLM-pretrained-dataset](https://huggingface.co/datasets/wannaphong/KhanomTanLLM-pretrained-dataset)
- Thai subset only: [https://huggingface.co/datasets/wannaphong/KhanomTanLLM-pretrained-dataset-thai-subset](https://huggingface.co/datasets/wannaphong/KhanomTanLLM-pretrained-dataset-thai-subset)
- List Thai subset: [https://huggingface.co/collections/pythainlp/datasets-for-pretrained-thai-llm-65db96ab730386b492889a98](https://huggingface.co/collections/pythainlp/datasets-for-pretrained-thai-llm-65db96ab730386b492889a98)

โดยชุดข้อมูลทั้งหมดมี 53,376,211,711 Tokens

- English: 31,629,984,243 Tokens
- Thai: 12,785,565,497 Tokens
- Code: 8,913,084,300 Toekns
- Parallel data: 190,310,686 Tokens

Based on Typhoon-7B (https://huggingface.co/scb10x/typhoon-7b) tokenizer

สำหรับภาษาอังกฤษ เรานำชุดข้อมูลสังเคราะห์ทำตาม Cosmopedia ของ HuggingFace ที่สังเคราะห์ชุดข้อมูลภาษาอังกฤษไว้ [https://huggingface.co/datasets/HuggingFaceTB/cosmopedia](https://huggingface.co/datasets/HuggingFaceTB/cosmopedia) และนำชุดข้อมูลอย่าง openwebtext ชุดข้อมูลเว็บ, epfl-llm/guidelines, MathPile_Commercial ชุดข้อมูลคณิตศาสตร์, minipile ชุดข้อมูลขนาดย่อจาก The Pile, goodwiki ชุดข้อมูลวิกิแบบ markdown และชุดข้อมูลจาก bigscience ที่เทรน Bloom LM มาใช้งาน

สำหรับรายละเอียดชุดข้อมูลอ่านได้ที่ [https://huggingface.co/datasets/wannaphong/KhanomTanLLM-pretrained-dataset](https://huggingface.co/datasets/wannaphong/KhanomTanLLM-pretrained-dataset)

## Tokenizer

เราตัดสินใจใช้ Tokenizer ของ Typhoon-7B (https://huggingface.co/scb10x/typhoon-7b) ในโมเดลของเรา เพื่อประหยัดทรัพยากรในการเทรน Tokenizer

## Pretraining

เราได้ใช้ pipeline สำหรับเทรน LLM ของเราด้วย [EasyLM project](https://github.com/young-geng/EasyLM) เป็นชุด pipeline ของ[โมเดล OpenLLaMA](https://github.com/openlm-research/open_llama)  เราได้ยืนขอการสนับสนุน TPU ผ่านโครงการ [TPU Research Cloud](https://sites.research.google/trc/about/) ของ Google และเราได้ใช้เครติดฟรีของ Googel Cloud สำหรับการทำ pretrained model  ทำให้เราไม่เสียค่าใช้จ่ายใด ๆ ในการเทรนโมเดลเลย

เราได้ทำการเทรนโมเดลทั้งขนาด 1B กับ 3B บนชุดข้อมูลเดียวกัน โดยใช้สถาปัตยกรรม Llama 2

สำหรับ pipeline ในการทำ pretrained model สามารถดูได้ที่ [https://github.com/wannaphong/EasyLM/tree/KhanomTanLLM-pretraining](https://github.com/wannaphong/EasyLM/tree/KhanomTanLLM-pretraining)

Pretrained Models:
- 1B: [https://huggingface.co/pythainlp/KhanomTanLLM-1B](https://huggingface.co/pythainlp/KhanomTanLLM-1B)
- 3B: [https://huggingface.co/pythainlp/KhanomTanLLM-3B](https://huggingface.co/pythainlp/KhanomTanLLM-3B)

## Model

หลังจากที่เราได้โมเดลจาก pretraining แล้ว เราได้นำไปทำ SFT โดยมีโมเดลกับชุดข้อมูลดังนี้

Instruct Models:
- Instruct dataset: [wannaphong/KhanomTanLLM-Instruct-dataset](https://huggingface.co/datasets/wannaphong/KhanomTanLLM-Instruct-dataset)
- SFT Script: [https://github.com/PyThaiNLP/KhanomTanLLM/tree/main/fineturning](https://github.com/PyThaiNLP/KhanomTanLLM/tree/main/fineturning)
- 1B: [https://huggingface.co/pythainlp/KhanomTanLLM-1B-Instruct](https://huggingface.co/pythainlp/KhanomTanLLM-1B-Instruct)
- 3B: [https://huggingface.co/pythainlp/KhanomTanLLM-3B-Instruct/](https://huggingface.co/pythainlp/KhanomTanLLM-3B-Instruct/)

## บทส่งท้าย

หากคุณนำโมเดลไป eval จะพบว่าโมเดลมีประสิทธิภาพค่อนข้างต่ำในหลายชุดทดสอบ เพราะเราไม่มีทรัพยากรมากเพียงพอที่จะนำชุดข้อมูลขนาดใหญ่จากภาษาอังกฤษมาเทรนร่วมด้วย เช่น [FineWeb](https://huggingface.co/datasets/HuggingFaceFW/fineweb), [Dolma](allenai/dolma), [The Pile](EleutherAI/the_pile_deduplicated) เป็นต้น เราได้เทรน LLM ตัวนี้ด้วยชุดข้อมูลข้อความเพียง 53B tokens หากได้รับการเทรนขนาด >1T tokens น่าจะมีประสิทธิภาพมากยิ่งขึ้น นอกจากนี้ชุดข้อมูลภาษาไทยยังมีขนาดเล็กเกินไปสำหรับการเทรน LLM ให้มีที่มีประสิทธิภาพดี ทางแก้ที่ดีที่สุด คือ การปล่อยชุดข้อมูลออกสู่สาธารณะให้มากยิ่งขึ้น และแนวทางการสังเคราะห์ชุดข้อมูลอาจเป็นหนึ่งในแนวทางแก้ไขปัญหาได้

เราหวังว่า ชุดข้อมูล pretrained, pipeline, และโมเดลที่เราปล่อยออกสู่สาธารณะจะเป็นประโยชน์ต่อผู้ที่สนใจทำ pretrained Thai LLM และช่วยส่งเสริมวงการ Open Source AI ในประเทศไทยมากยิ่งขึ้น

เขียนโดย วรรณพงษ์ ภัททิยไพบูลย์
