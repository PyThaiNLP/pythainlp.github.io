---
layout: post
title: "PyThaiTTS v1.0.0 and MakHamTTS Released"
gh-repo: wannaphong/MakHamTTS
gh-badge: [star, fork]
categories: [news]
comments: true
---

Today, we are announcing the release of PyThaiTTS v1.0.0 alongside the MakHamTTS model. Both are tools for Thai speech synthesis, starting with PyThaiTTS.

## PyThaiTTS v1.0.0

What's new in PyThaiTTS v1.0.0:

* **Pronunciation customization support:** You can now customize the pronunciation of words to be synthesized in PyThaiTTS.
* **Added MakHamTTS model and makham_paradee model.**

Read more details at: [https://github.com/PyThaiNLP/PyThaiTTS/tree/v1.0.0](https://github.com/PyThaiNLP/PyThaiTTS/tree/v1.0.0)

## MakHamTTS

MakHamTTS (มะขาม) is a TTS model trained on a synthetic voice dataset. It shares the same codebase with FastThaiG2P, a Kokoro-82M-based model, but is trained on over 100 hours of voice data featuring both female and male voices. In addition, we distilled the Kokoro-82M model following [Paradee: Distilling Kokoro-82M into an 8M-Parameter Single-Voice Text-to-Speech Model](https://arxiv.org/abs/2610.06817), reducing the model size to just 8.07 MB (name as makham_paradee). It is well-suited for basic tasks, produces decent voice quality, runs faster than ~45x Real-Time, and requires fewer resources than FastThaiG2P or original Kokoro-82M-based models.

* **Online demo**: [https://github.wannaphong.com/MakHamTTS/webdemo/](https://github.wannaphong.com/MakHamTTS/webdemo/)
* **Model Repository**: [pythainlp/MakHamTTS](https://huggingface.co/pythainlp/MakHamTTS)
* **Dataset Repository**: [pythainlp/MakHamTTS-dataset](https://huggingface.co/datasets/pythainlp/MakHamTTS-dataset)
* **Source Code & Training Suite**: [GitHub: wannaphong/MakHamTTS](https://github.com/wannaphong/MakHamTTS)


# ภาษาไทย

วันนี้เราได้เปิดตัว PyThaiTTS v1.0.0 พร้อมกับโมเดล MakHamTTS โดยทั้งคู่เป็นเครื่องมือสำหรับสังเคราะห์เสียงภาษาไทย โดยเริ่มจาก PyThaiTTS

## PyThaiTTS v1.0.0

PyThaiTTS v1.0.0 มีอะไรใหม่:

- รองรับการปรับแต่งคำอ่าน: คุณสามารถปรับแต่งคำอ่านของคำที่ต้องการสังเคราะห์ใน PyThaiTTS ได้แล้ว
- เพิ่มโมเดล MakHamTTS และ makham_paradee

อ่านรายละเอียดได้ที่ [https://github.com/PyThaiNLP/PyThaiTTS/tree/v1.0.0](https://github.com/PyThaiNLP/PyThaiTTS/tree/v1.0.0)

## MakHamTTS

MakHamTTS (มะขาม) เป็นโมเดล TTS ที่สร้างจากชุดข้อมูลเสียงที่สังเคราะห์ขึ้นมา โดยใช้โค้ดเดียวกันกับ FastThaiG2P โมเดลบนฐาน Kokoro-82M แต่เทรนด้วยข้อมูลเสียงที่มีขนาดใหญ่กว่า 100 ชั่วโมง มีทั้งเสียงผู้หญิงกับเสียงผู้ชาย นอกจากนั้น เราได้ย่อขนาดโมเดล  Kokoro-82M ตาม [Paradee: Distilling Kokoro-82M into an 8M-Parameter Single-Voice Text-to-Speech Model](https://arxiv.org/abs/2610.06817) จนได้โมเดลขนาดเพียง 8.07 MB ชื่อว่า makham_paradee เหมาะสมกับงานพื้นฐานและเสียงอยู่ในระดับพอใช้ได้ เร็วกว่า ~45x Real-Time และใช้ทรัพยากรน้อยกว่า FastThaiG2P หรือโมเดลบนฐาน Kokoro-82M

- **Online demo**: [https://github.wannaphong.com/MakHamTTS/webdemo/](https://github.wannaphong.com/MakHamTTS/webdemo/)
- **Model Repository**: [pythainlp/MakHamTTS](https://huggingface.co/pythainlp/MakHamTTS)
- **Dataset Repository**: [pythainlp/MakHamTTS-dataset](https://huggingface.co/datasets/pythainlp/MakHamTTS-dataset)
- **Source Code & Training Suite**: [GitHub: wannaphong/MakHamTTS](https://github.com/wannaphong/MakHamTTS)
