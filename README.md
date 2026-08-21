# Awesome-SpeechLM-Survey
<!-- [![Hugging Face%20-%20VoxEval](https://img.shields.io/badge/🤗%20Hugging%20Face%20-%20VoxEval-blue)](https://huggingface.co/datasets/qqjz/VoxEval) -->
[![arXiv](https://img.shields.io/badge/arXiv-2501.04962-red)](https://arxiv.org/abs/2410.03751)

**🎉🎉🎉Our survey paper "Recent Advances in Speech Language Models: A Survey" has been accepted to ACL 2025 main conference!**

This is the Github repository for paper: [*Recent Advances in Speech Language Models: A Survey*](https://arxiv.org/abs/2410.03751). In this paper, we survey the field of Speech Language Models (SpeechLMs), which are capable of performing end-to-end speech interactions with humans and serve as autoregressive foundation models.

# News
- The short version of our [audio reasoning survey paper](https://arxiv.org/abs/2605.21008) has been accepted to **EMNLP 2026 Findings**! 🎉
- Our paper [*SpeechSense: A Paralinguistic-Focused Dataset for Fine-Grained Speech Sentiment Analysis*](https://arxiv.org/abs/2608.17931) has been accepted to **ACM Multimedia 2026 (Dataset Track)**! 🎉
- We have released [*TextPro-SLM: Minimizing Modality Gap from the Input Side: Your Speech LLM Can Be a Prosody-Aware Text LLM*](https://arxiv.org/abs/2605.05927) on arXiv! 🎉
- We have released [*A Survey of Audio Reasoning in Multimodal Foundation Models*](https://arxiv.org/abs/2605.21008) on arXiv! 🎉
- Our paper [*TurnGuide: Enhancing Meaningful Full Duplex Spoken Interactions via Dynamic Turn-Level Text-Speech Interleaving*](https://arxiv.org/abs/2508.07375) has been accepted to **Interspeech 2026 Long Paper Track as an Oral presentation**! 🎉 Check it out on [GitHub](https://github.com/dreamtheater123/TurnGuide).
- Our paper [*MTR-DuplexBench: Towards a Comprehensive Evaluation of Multi-Round Conversations for Full-Duplex Speech Language Models*](https://arxiv.org/abs/2511.10262) has been accepted to **Findings of ACL 2026**! 🎉 Check it out on [GitHub](https://github.com/ZhangHe0918/MTR-DuplexBench).
- We have released [*VoxEval: Benchmarking the Knowledge Understanding Capabilities of End-to-End Spoken Language Models*](https://arxiv.org/abs/2501.04962) on arXiv!🎉 Also check it out on [Github](https://github.com/dreamtheater123/VoxEval).

## Introduction
Why SpeechLMs? SpeechLMs are used for end-to-end speech-based interactions. Traditional ASR + LLM + TTS setups suffer from information loss and cumulative errors during conversion. SpeechLMs directly model speech data, capturing both semantic and paralinguistic information for richer interactions!

In this repository, we distinguish between two closely related model families:

- **Speech Language Models (SpeechLMs)** directly accept speech/audio and generate speech/audio. They may operate in turn-based, streaming, or full-duplex settings, but do not rely on an external ASR-LLM-TTS cascade as their core interaction mechanism.
- **Large Audio Language Models (LALMs)** use a generative language model to understand speech, environmental sound, or music and produce text. Speech-centric LLM-ASR models are included as a dedicated LALM category, while conventional encoder-only ASR models are outside the scope of this list.

Models supporting both text and speech output are listed under SpeechLMs to avoid duplication.

![Intro Figure](./figures/intro_figure.jpg)

## Taxonomy
We introduce a novel taxonomy for SpeechLMs, categorizing them based on their architecture and training recipes.

![taxonomy](./figures/taxonomy.png)

## Speech Language Models (SpeechLMs)

The models below support speech/audio input and speech/audio output within the model. The list covers turn-based, streaming, and full-duplex interaction.

| Model | Paper / Release | Year | Interaction |
|-------|-----------------|------|-------------|
| Lychee-FD | [Hierarchical Acoustic-Semantic Modeling for Full-Duplex Speech Interaction](https://arxiv.org/abs/2607.06540) | 2026 | Full-duplex |
| DuplexSLA | [DuplexSLA](https://arxiv.org/abs/2605.20755) · [GitHub](https://github.com/hyzhang24/DuplexSLA) | 2026 | Full-duplex speech-language-action |
| MiniCPM-o 4.5 | [MiniCPM-o 4.5](https://arxiv.org/abs/2604.27393) | 2026 | Full-duplex omni-modal |
| Qwen3.5-Omni | [Qwen3.5-Omni Technical Report](https://arxiv.org/abs/2604.15804) | 2026 | Streaming omni-modal |
| PersonaPlex | [PersonaPlex: Voice and Role Control for Full Duplex Conversational Speech Models](https://arxiv.org/abs/2602.06053) · [GitHub](https://github.com/NVIDIA/personaplex) | 2026 | Full-duplex |
| F-Actor | [F-Actor: Controllable Full-Duplex Conversational Speech Generation](https://arxiv.org/abs/2601.11329) | 2026 | Full-duplex |
| MiMo-Audio | [MiMo-Audio Technical Report](https://arxiv.org/abs/2512.23808) | 2025 | Spoken dialogue and audio generation |
| LFM2-Audio | [LFM2 Technical Report](https://arxiv.org/abs/2511.23404) | 2025 | Real-time speech-to-speech |
| MOSS-Speech | [MOSS-Speech](https://arxiv.org/abs/2510.00499) | 2025 | Native speech-to-speech |
| Qwen3-Omni | [Qwen3-Omni Technical Report](https://arxiv.org/abs/2509.17765) | 2025 | Streaming omni-modal |
| TurnGuide | [Enhancing Meaningful Full Duplex Spoken Interactions via Dynamic Turn-Level Text-Speech Interleaving](https://arxiv.org/abs/2508.07375) · [GitHub](https://github.com/dreamtheater123/TurnGuide) | 2025 | Full-duplex |
| Step-Audio 2 | [Step-Audio 2 Technical Report](https://arxiv.org/abs/2507.16632) | 2025 | End-to-end speech interaction |
| Audio Flamingo 3 | [Audio Flamingo 3: Advancing Audio Intelligence with Fully Open Large Audio Language Models](https://arxiv.org/abs/2507.08128) | 2025 | General audio and voice-to-voice |
| OpenS2S | [OpenS2S: Advancing Fully Open-Source End-to-End Empathetic Large Speech Language Model](https://arxiv.org/abs/2507.05177) | 2025 | End-to-end speech-to-speech |
| NTPP | [Generative Speech Language Modeling for Dual-Channel Spoken Dialogue via Next-Token-Pair Prediction](https://arxiv.org/abs/2506.00975) | 2025 | Dual-channel dialogue |
| SALMONN-omni | [A Standalone Speech LLM without Codec Injection for Full-duplex Conversation](https://arxiv.org/abs/2505.17060) | 2025 | Full-duplex |
| VITA-Audio | [Fast Interleaved Cross-Modal Token Generation for Efficient Large Speech-Language Model](https://arxiv.org/abs/2505.03739) | 2025 | Streaming speech interaction |
| Voila | [Voice-Language Foundation Models for Real-Time Autonomous Interaction and Voice Role-Play](https://arxiv.org/abs/2505.02707) | 2025 | Real-time interaction |
| LLaMA-Omni 2 | [LLM-based Real-time Spoken Chatbot with Autoregressive Streaming Speech Synthesis](https://arxiv.org/abs/2505.02625) | 2025 | Streaming speech-to-speech |
| Kimi-Audio | [Kimi-Audio Technical Report](https://arxiv.org/abs/2504.18425) | 2025 | Audio understanding and generation |
| Qwen2.5-Omni | [Qwen2.5-Omni Technical Report](https://arxiv.org/abs/2503.20215) | 2025 | Streaming omni-modal |
| Slamming | [Training a Speech Language Model on One GPU in a Day](https://arxiv.org/abs/2502.15814) | 2025 | Speech-to-speech |
| Baichuan-Audio | [A Unified Framework for End-to-End Speech Interaction](https://arxiv.org/abs/2502.17239) | 2025 | End-to-end speech interaction |
| Step-Audio | [Unified Understanding and Generation in Intelligent Speech Interaction](https://arxiv.org/abs/2502.11946) | 2025 | Speech interaction |
| MinMo | [A Multimodal Large Language Model for Seamless Voice Interaction](https://arxiv.org/abs/2501.06282) | 2025 | Streaming voice interaction |
| VITA-1.5 | [Towards GPT-4o Level Real-Time Vision and Speech Interaction](https://arxiv.org/abs/2501.01957) | 2025 | Real-time omni-modal |
| MiniCPM-o | [A GPT-4o Level MLLM for Vision, Speech and Multimodal Live Streaming on Your Phone](https://github.com/OpenBMB/MiniCPM-o) | 2025 | Streaming omni-modal |
| SLAM-Omni | [Timbre-Controllable Voice Interaction System with Single-Stage Training](https://arxiv.org/abs/2412.15649) | 2024 | Voice interaction |
| Lyra | [An Efficient and Speech-Centric Framework for Omni-Cognition](https://arxiv.org/abs/2412.09501) | 2024 | Speech interaction |
| Flow-Omni | [Continuous Speech Tokens Makes LLMs Robust Multi-Modality Learners](https://arxiv.org/abs/2412.04917) | 2024 | Speech understanding and generation |
| GLM-4-Voice | [Towards Intelligent and Human-Like End-to-End Spoken Chatbot](https://arxiv.org/abs/2412.02612) | 2024 | End-to-end speech interaction |
| Scaling Speech-Text Pre-training | [Scaling Speech-Text Pre-training with Synthetic Interleaved Data](https://arxiv.org/abs/2411.17607) | 2024 | Speech-text generation |
| Freeze-Omni | [A Smart and Low Latency Speech-to-speech Dialogue Model with Frozen LLM](https://arxiv.org/abs/2411.00774) | 2024 | Streaming speech-to-speech |
| OmniFlatten | [An End-to-end GPT Model for Seamless Voice Conversation](https://arxiv.org/abs/2410.17799) | 2024 | End-to-end voice interaction |
| Mini-Omni2 | [Towards Open-source GPT-4o with Vision, Speech and Duplex Capabilities](https://arxiv.org/abs/2410.11190) | 2024 | Duplex omni-modal |
| IntrinsicVoice | [Empowering LLMs with Intrinsic Real-time Voice Interaction Abilities](https://arxiv.org/abs/2410.08035) | 2024 | Real-time voice interaction |
| Moshi | [A Speech-Text Foundation Model for Real-Time Dialogue](https://arxiv.org/abs/2410.00037) | 2024 | Full-duplex |
| SyncLLM | [Beyond Turn-Based Interfaces: Synchronous LLMs as Full-Duplex Dialogue Agents](https://arxiv.org/abs/2409.15594) | 2024 | Full-duplex |
| EMOVA | [Empowering Language Models to See, Hear and Speak with Vivid Emotions](https://arxiv.org/abs/2409.18042) | 2024 | Emotional speech interaction |
| LLaMA-Omni | [Seamless Speech Interaction with Large Language Models](https://arxiv.org/abs/2409.06666) | 2024 | Streaming speech-to-speech |
| Mini-Omni | [Language Models Can Hear, Talk While Thinking in Streaming](https://arxiv.org/abs/2408.16725) | 2024 | Streaming speech-to-speech |
| VITA | [Towards Open-Source Interactive Omni Multimodal LLM](https://arxiv.org/abs/2408.05211) | 2024 | Real-time omni-modal |
| LSLM | [Language Model Can Listen While Speaking](https://arxiv.org/abs/2408.02622) | 2024 | Full-duplex |
| Spirit-LM | [Interleaved Spoken and Written Language Model](https://arxiv.org/abs/2402.05755) | 2024 | Interleaved speech-text generation |
| SpeechGPT-Gen | [Scaling Chain-of-Information Speech Generation](https://arxiv.org/abs/2401.13527) | 2024 | Speech generation |
| GPST | [Generative Pre-trained Speech Language Model with Efficient Hierarchical Transformer](https://aclanthology.org/2024.acl-long.97) | 2024 | Speech generation and continuation |
| Parrot | [Autoregressive Spoken Dialogue Language Modeling with Decoder-only Transformers](https://openreview.net/forum?id=Ttndg2Jl5F) | 2023 | Spoken dialogue modeling |
| SUTLM | [Toward Joint Language Modeling for Speech Units and Text](https://arxiv.org/abs/2310.08715) | 2023 | Speech-text generation |
| tGSLM | [Generative Spoken Language Model Based on Continuous Word-Sized Audio Tokens](https://arxiv.org/abs/2310.05224) | 2023 | Spoken language generation |
| LauraGPT | [Listen, Attend, Understand, and Regenerate Audio with GPT](https://arxiv.org/abs/2310.04673) | 2023 | Audio understanding and regeneration |
| Spectron | [Spoken Question Answering and Speech Continuation Using Spectrogram-Powered LLM](https://openreview.net/forum?id=izrOLJov5y) | 2023 | Spoken QA and continuation |
| VoxtLM | [Unified Decoder-Only Models for Speech Recognition, Synthesis, and Continuation](https://ieeexplore.ieee.org/document/10447112) | 2023 | Speech-text generation |
| TWIST | [Textually Pretrained Speech Language Models](https://proceedings.neurips.cc/paper_files/paper/2023/hash/c859b99b5d717c9035e79d43dfd69435-Abstract-Conference.html) | 2023 | Spoken language modeling |
| AudioPaLM | [A Large Language Model That Can Speak and Listen](https://arxiv.org/abs/2306.12925) | 2023 | Speech understanding and generation |
| VioLA | [Unified Codec Language Models for Speech Recognition, Synthesis, and Translation](https://arxiv.org/abs/2305.16107) | 2023 | Speech understanding and generation |
| SpeechGPT | [Empowering Large Language Models with Intrinsic Cross-Modal Conversational Abilities](https://arxiv.org/abs/2305.11000) | 2023 | Speech conversation |
| dGSLM | [Generative Spoken Dialogue Language Modeling](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00545/115240/Generative-Spoken-Dialogue-Language-Modeling) | 2023 | Spoken dialogue modeling |
| pGSLM | [Text-Free Prosody-Aware Generative Spoken Language Modeling](https://arxiv.org/abs/2109.03264) | 2021 | Prosody-aware spoken language modeling |
| GSLM | [On Generative Spoken Language Modeling from Raw Audio](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00430/108611/On-Generative-Spoken-Language-Modeling-from-Raw) | 2021 | Spoken language modeling |

### Commercial and Closed Voice Systems

These entries are tracked separately because public information may describe a product or API rather than disclose a standalone end-to-end model architecture.

| System | Release | Year | Notes |
|--------|---------|------|-------|
| OpenAI GPT-Live | [Introducing GPT-Live](https://openai.com/index/introducing-gpt-live/) | 2026 | Full-duplex voice model |
| OpenAI GPT-Realtime-2 | [Advancing Voice Intelligence with New Models in the API](https://openai.com/index/advancing-voice-intelligence-with-new-models-in-the-api/) | 2026 | Native audio input and output |
| OpenAI gpt-realtime | [Introducing gpt-realtime](https://openai.com/index/introducing-gpt-realtime/) | 2025 | Native audio input and output |
| Gemini Native Audio / Live API | [Live API Capabilities](https://ai.google.dev/gemini-api/docs/live-api/capabilities) | 2025 | Native real-time audio interaction |
| OpenAI Advanced Voice Mode | [Advanced Voice Mode FAQ](https://help.openai.com/en/articles/9617425-advanced-voice-mode-faq) | 2024 | Commercial voice experience |
| Claude Voice Mode | [Using Voice Mode on Claude Mobile Apps](https://support.anthropic.com/en/articles/11101966-using-voice-mode-on-claude-mobile-apps) | 2025 | Product feature; native end-to-end architecture not publicly documented |
| MindGPT-4o-Audio | [MindGPT-4o-Audio Release](https://mp.weixin.qq.com/s?__biz=MzkyNzc3ODYzMQ==&mid=2247483808&idx=1&sn=15b2d0fc5c415066e9e85a0e17fa4094) | 2025 | Commercial real-time voice model |

### SpeechLM Training and Alignment

These papers improve the interaction behavior of full-duplex SpeechLMs rather than introducing a separate foundation-model family.

| Paper | Year | Focus |
|-------|------|-------|
| [Aligning Spoken Dialogue Models from User Interactions](https://arxiv.org/abs/2506.21463) | 2025 | Preference alignment from user interactions |
| [Multi-Faceted Interactivity Alignment in Full-Duplex Speech Models](https://arxiv.org/abs/2606.11167) | 2026 | Reinforcement learning for full-duplex interactivity |

## Large Audio Language Models (LALMs)

LALMs accept speech, environmental sound, and/or music and generate text. Models that additionally generate speech are listed only in the SpeechLM section above.

### General Audio Understanding

| Model | Paper / Release | Year | Audio Scope |
|-------|-----------------|------|-------------|
| MOSS-Audio | [MOSS-Audio](https://arxiv.org/abs/2606.01802) | 2026 | Speech, sound, and music |
| Audio Flamingo Next | [Audio Flamingo Next](https://arxiv.org/abs/2604.10905) | 2026 | Speech, sound, music, and long audio |
| Voxtral | [Voxtral](https://arxiv.org/abs/2507.13264) | 2025 | Speech and long audio |
| Gemma 3n | [Gemma 3n](https://deepmind.google/models/gemma/gemma-3n/) | 2025 | Speech and multimodal understanding |
| Audio Flamingo 2 | [Audio Flamingo 2: An Audio-Language Model with Long-Audio Understanding and Expert Reasoning Abilities](https://arxiv.org/abs/2503.03983) | 2025 | Speech, sound, music, and long audio |
| Phi-4-Multimodal | [Phi-4-Multimodal Technical Report](https://arxiv.org/abs/2503.01743) | 2025 | Speech, audio, vision, and text |
| Qwen2-Audio | [Qwen2-Audio Technical Report](https://arxiv.org/abs/2407.10759) | 2024 | Speech, sound, and music |
| GAMA | [A Large Audio-Language Model with Advanced Audio Understanding and Complex Reasoning Abilities](https://arxiv.org/abs/2406.11768) | 2024 | Sound and music |
| WavLLM | [Towards Robust and Adaptive Speech Large Language Model](https://arxiv.org/abs/2404.00656) | 2024 | Speech and paralinguistics |
| Audio Flamingo | [A Novel Audio Language Model with Few-Shot Learning and Dialogue Abilities](https://arxiv.org/abs/2402.01831) | 2024 | General audio |
| Qwen-Audio | [Advancing Universal Audio Understanding via Unified Large-Scale Audio-Language Models](https://arxiv.org/abs/2311.07919) | 2023 | Speech, sound, music, and song |
| SALMONN | [Towards Generic Hearing Abilities for Large Language Models](https://arxiv.org/abs/2310.13289) | 2023 | Speech, sound, and music |
| LTU-AS | [Joint Audio and Speech Understanding](https://arxiv.org/abs/2309.14405) | 2023 | Speech, paralinguistics, and sound |
| Pengi | [An Audio Language Model for Audio Tasks](https://arxiv.org/abs/2305.11834) | 2023 | General audio |
| LTU | [An Audio-Enhanced Large Language Model for Long-Tail Audio Understanding](https://arxiv.org/abs/2305.10790) | 2023 | General audio |

### Audio Reasoning, Music, and Prosody

| Model | Paper | Year | Focus |
|-------|-------|------|-------|
| TextPro-SLM | [Minimizing Modality Gap from the Input Side: Your Speech LLM Can Be a Prosody-Aware Text LLM](https://arxiv.org/abs/2605.05927) | 2026 | Speech and prosody understanding |
| Audio-Cogito | [Audio-Cogito](https://arxiv.org/abs/2604.12527) | 2026 | Deep audio reasoning |
| Step-Audio-R1 | [Step-Audio-R1](https://arxiv.org/abs/2511.15848) | 2025 | Speech, sound, and music reasoning |
| Music Flamingo | [Music Flamingo](https://arxiv.org/abs/2511.10289) | 2025 | Music understanding and reasoning |
| Audio-Reasoner | [Improving Reasoning Capability in Large Audio Language Models](https://arxiv.org/abs/2503.02318) | 2025 | Chain-of-thought audio reasoning |
| LLark | [A Multimodal Instruction-Following Language Model for Music](https://arxiv.org/abs/2310.07160) | 2023 | Music understanding and reasoning |
| MusiLingo | [Bridging Music and Text with Pre-trained Language Models for Music Captioning and Query Response](https://arxiv.org/abs/2309.08730) | 2023 | Music captioning and QA |
| MU-LLaMA | [Music Understanding Large Language Model](https://arxiv.org/abs/2308.11276) | 2023 | Music understanding |

### Speech-Centric LALMs and LLM-ASR

This category contains speech-conditioned generative language models whose primary output is text. Conventional encoder-only ASR systems are excluded.

| Model | Paper / Release | Year | Focus |
|-------|-----------------|------|-------|
| FireRedASR2S | [A Fully Open-Source Industrial-Grade All-in-One Speech Recognition System](https://arxiv.org/abs/2603.10420) | 2026 | Multilingual ASR |
| Qwen3-ASR | [Qwen3-ASR Technical Report](https://arxiv.org/abs/2601.21337) | 2026 | Multilingual and multidialect ASR |
| VibeVoice-ASR | [VibeVoice-ASR Technical Report](https://arxiv.org/abs/2601.18184) | 2026 | Long-form ASR, diarization, and timestamps |
| GLM-ASR-Nano | [GLM-ASR](https://github.com/zai-org/GLM-ASR) | 2025 | LLM-based ASR |
| Fun-ASR | [Fun-ASR: A Large Language Model Based Speech Recognition System](https://arxiv.org/abs/2509.12508) | 2025 | Multilingual speech-to-text |
| FireRedASR | [Open-Source Industrial-Grade Speech Recognition Models from Encoder-Decoder to LLM Integration](https://arxiv.org/abs/2501.14350) | 2025 | ASR and LLM integration |
| Seed-ASR | [Understanding Diverse Speech and Contexts with LLM-based Speech Recognition](https://arxiv.org/abs/2407.04675) | 2024 | Context-aware LLM-ASR |

## Related Audio and Speech Generation Systems

The following works are closely related but are not included in the strict SpeechLM or LALM lists because they do not provide a unified speech-input/speech-output dialogue model or an audio-conditioned generative text LLM.

| Model / Family | Paper / Release | Scope |
|----------------|-----------------|-------|
| CSM | [Conversational Speech Generation Model](https://www.sesame.com/research/crossing_the_uncanny_valley_of_voice) | Conversational speech generation / TTS |
| FunAudioLLM | [Voice Understanding and Generation Foundation Models for Natural Interaction Between Humans and LLMs](https://arxiv.org/abs/2407.04051) | SenseVoice and CosyVoice model family |
| UniAudio | [An Audio Foundation Model Toward Universal Audio Generation](https://arxiv.org/abs/2310.00704) | Universal audio generation |
| Voicebox | [Text-Guided Multilingual Universal Speech Generation at Scale](https://proceedings.neurips.cc/paper_files/paper/2023/hash/2d8911db9ecedf866015091b28946e15-Abstract-Conference.html) | Text-guided speech generation |

## SpeechLM Tokenizers
### Semantic Tokenizers
| Name | Title | Url |
|-------|-------|-----|
|  Whisper     | Robust Speech Recognition via Large-Scale Weak Supervision | [Link](https://arxiv.org/abs/2212.04356)  |
|  CosyVoice     | CosyVoice: A Scalable Multilingual Zero-shot Text-to-speech Synthesizer based on Supervised Semantic Tokens | [Link](https://arxiv.org/abs/2407.05407)  |
|  Google USM     | Google USM: Scaling Automatic Speech Recognition Beyond 100 Languages | [Link](https://arxiv.org/abs/2303.01037)  |
|  WavLM     | WavLM: Large-Scale Self-Supervised Pre-Training for Full Stack Speech Processing | [Link](https://arxiv.org/abs/2110.13900)  |
|  HuBERT     | HuBERT: Self-Supervised Speech Representation Learning by Masked Prediction of Hidden Units | [Link](https://arxiv.org/abs/2106.07447)  |
|  W2v-bert     | W2v-BERT: Combining Contrastive Learning and Masked Language Modeling for Self-Supervised Speech Pre-Training | [Link](https://arxiv.org/abs/2108.06209)  |
|  Wav2vec 2.0     | wav2vec 2.0: A Framework for Self-Supervised Learning of Speech Representations | [Link](https://arxiv.org/abs/2006.11477)  |

### Acoustic Tokenizers
| Name | Title | Url |
|-------|-------|-----|
|  WavTokenizer     | WavTokenizer: an Efficient Acoustic Discrete Codec Tokenizer for Audio Language Modeling | [Link](https://arxiv.org/abs/2408.16532)  |
|  SNAC     | SNAC: Multi-Scale Neural Audio Codec | [Link](https://arxiv.org/abs/2410.14411)  |
|  Encodec     | High Fidelity Neural Audio Compression | [Link](https://arxiv.org/abs/2210.13438)  |
|  SoundStream     | SoundStream: An End-to-End Neural Audio Codec | [Link](https://arxiv.org/abs/2107.03312)  |

### Mixed Tokenizers
| Name | Title | Url |
|-------|-------|-----|
|  SpeechTokenizer     | SpeechTokenizer: Unified Speech Tokenizer for Speech Large Language Models | [Link](https://arxiv.org/abs/2308.16692)  |
|  Mimi     | Moshi: a speech-text foundation model for real-time dialogue | [Link](https://arxiv.org/abs/2410.00037)  |

## Popular Training Datasets
| Dataset                                                 | Type                   | Phase              | Hours | Year |
|---------------------------------------------------------|------------------------|--------------------|-------|------|
| [LibriSpeech](https://www.openslr.org/12)                       | ASR                    | Pre-Training       | 1k    | 2015 |
| [Multilingual LibriSpeech](https://www.openslr.org/94/) | ASR                    | Pre-Training       | 50.5k | 2020 |
| [LibriLight](https://github.com/facebookresearch/libri-light)         | ASR                    | Pre-Training       | 60k   | 2019 |
| [People dataset](https://github.com/mlcommons/peoples-speech)                  | ASR                    | Pre-Training       | 30k   | 2021 |
| [VoxPopuli](https://github.com/facebookresearch/voxpopuli)                            | ASR                    | Pre-Training       | 1.6k  | 2021 |
| [Gigaspeech](https://github.com/SpeechColab/GigaSpeech)                  | ASR                    | Pre-Training       | 40k   | 2021 |
| [Common Voice](https://commonvoice.mozilla.org/zh-CN)                       | ASR                    | Pre-Training       | 2.5k  | 2019 |
| [VCTK](https://paperswithcode.com/dataset/voice-bank-demand)                                         | ASR                    | Pre-Training       | 0.3k  | 2017 |
| [WenetSpeech](https://wenet.org.cn/WenetSpeech/)               | ASR                    | Pre-Training       | 22k   | 2022 |
| [LibriTTS](https://www.openslr.org/60/)                                 | TTS                    | Pre-Training       | 0.6k  | 2019 |
| [CoVoST2](https://github.com/facebookresearch/covost)                           | S2TT                   | Pre-Training       | 2.8k  | 2020 |
| [CVSS](https://github.com/google-research-datasets/cvss)                                      | S2ST                   | Pre-Training       | 1.9k  | 2022 |
| [VoxCeleb](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox1.html)                                 | Speaker Identification | Pre-Training       | 0.4k  | 2017 |
| [VoxCeleb2](https://www.robots.ox.ac.uk/~vgg/data/voxceleb/vox2.html)                                | Speaker Identification | Pre-Training       | 2.4k  | 2018 |
| [Spotify Podcasts](https://podcastsdataset.byspotify.com/)            | Podcast                | Pre-Training       | 47k   | 2020 |
| [Fisher](https://catalog.ldc.upenn.edu/LDC2004T19)                      | Telephone conversation | Pre-Training       | 2k    | 2004 |
| [SpeechInstruct](https://huggingface.co/datasets/fnlp/SpeechInstruct)                         | Instruction-following  | Instruction-Tuning | -     | 2023 |
| InstructS2S-200K                       | Instruction-following  | Instruction-Tuning | -     | 2024 |
| [VoiceAssistant-400K](https://huggingface.co/datasets/gpt-omni/VoiceAssistant-400K)              | Instruction-following  | Instruction-Tuning | -     | 2024 |


## Evaluation Benchmarks
| Name                                                                   | Eval Type      | \# Tasks | Audio Type           | I/O                   |
|------------------------------------------------------------------------|----------------|----------|----------------------|-----------------------|
| ABX | Representation | 1        | Speech               | $A \rightarrow -$     |
| sWUGGY                                      | Linguistic     | 1        | Speech               | $A \rightarrow -$     |
| sBLIMP                                      | Linguistic     | 1        | Speech               | $A \rightarrow -$     |
| [sStoryCloze](https://github.com/slp-rl/SpokenStoryCloze)                                | Linguistic     | 1        | Speech               | $A/T \rightarrow -$   |
| [STSP](https://github.com/facebookresearch/spiritlm/blob/main/spiritlm/eval/README.md)                               | Paralinguistic | 1        | Speech               | $A/T \rightarrow A/T$ |
| [MMAU](https://github.com/apple/axlearn/tree/main/docs/research/mmau)                      | Downstream     | 27       | Speech, Sound, Music | $A \rightarrow T$     |
| [Audiobench](https://github.com/AudioLLMs/AudioBench)                                 | Downstream     | 8        | Speech, Sound        | $A \rightarrow T$     |
| [AIR-Bench](https://github.com/OFA-Sys/AIR-Bench)                                    | Downstream     | 20       | Speech, Sound, Music | $A \rightarrow T$     |
| [SD-Eval](https://github.com/amphionspace/SD-Eval)                                       | Downstream     | 4        | Speech               | $A \rightarrow T$     |
| [SUPERB](https://huggingface.co/datasets/s3prl/superb)                                  | Downstream     | 10       | Speech               | $A \rightarrow T$     |
| [Dynamic-SUPERB](https://github.com/dynamic-superb/dynamic-superb)                          | Downstream     | 180      | Speech, Sound, Music | $A \rightarrow T$     |
| [SALMON](https://huggingface.co/datasets/slprl/SALMon)                                         | Downstream     | 8        | Speech               | $A \rightarrow -$     |
| [VoiceBench](https://github.com/matthewcym/voicebench)                                          | Downstream     | 8        | Speech               | $A \rightarrow A$     |
| [VoxEval](https://github.com/dreamtheater123/VoxEval)                                          | Downstream     | 56       | Speech               | $A \rightarrow A$     |


## Citation
```
@article{cui2024recent,
  title={Recent advances in speech language models: A survey},
  author={Cui, Wenqian and Yu, Dianzhi and Jiao, Xiaoqi and Meng, Ziqiao and Zhang, Guangyan and Wang, Qichao and Guo, Yiwen and King, Irwin},
  journal={arXiv preprint arXiv:2410.03751},
  year={2024}
}
```
