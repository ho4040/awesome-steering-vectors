# Awesome Steering Vectors [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of steering vectors, control vectors, and activation engineering resources for LLMs.

Steering vectors modify LLM behavior by adding direction vectors to model activations during inference. This list collects pre-trained vectors, datasets, tools, and papers.

## Contents

- [Personality & Behavioral Traits](#personality--behavioral-traits)
- [Creative Writing Control](#creative-writing-control)
- [Safety & Alignment](#safety--alignment)
- [Thinking & Reasoning](#thinking--reasoning)
- [Refusal Direction & Abliteration](#refusal-direction--abliteration)
- [Domain-Specific Behavioral Steering](#domain-specific-behavioral-steering)
- [Introspection & Concept Vectors](#introspection--concept-vectors)
- [Datasets](#datasets)
- [Tools & Libraries](#tools--libraries)
- [Papers](#papers)

---

## Personality & Behavioral Traits

Vectors that steer personality dimensions (Big Five, Dark Tetrad, sycophancy, power-seeking, etc.)

| Repository | Models | Traits | Method | Format |
|---|---|---|---|---|
| [dalekwon/bipo-steering-vectors](https://huggingface.co/dalekwon/bipo-steering-vectors) | - | Agreeableness, Neuroticism, Paranoid, + Korean variants | BiPO | SafeTensors |
| [shiv96/steering-vectors](https://huggingface.co/datasets/shiv96/steering-vectors) | Llama-3.2-1B, Llama-3.1-8B | Harmfulness, power-seeking, coordinate AIs, corrigibility | PCA / Mean-diff / KPCA | Parquet |
| [shiv96/steering-vectors-caa-phi3.5-mini-it](https://huggingface.co/datasets/shiv96/steering-vectors-caa-phi3.5-mini-it) | Phi-3.5-Mini | Self-awareness, power-seeking | CAA | Parquet |
| [shiv96/steering-vectors-openended-llama3.2-1B-it](https://huggingface.co/datasets/shiv96/steering-vectors-openended-llama3.2-1B-it) | Llama-3.2-1B | Sycophancy | Activation mean-diff | Parquet |
| [shiv96/steering-vectors-openended-llama3.1-8B-it](https://huggingface.co/datasets/shiv96/steering-vectors-openended-llama3.1-8B-it) | Llama-3.1-8B | Sycophancy | Activation mean-diff | Parquet |
| [shiv96/steering-vectors-openended-qwen2.5-7b-it](https://huggingface.co/datasets/shiv96/steering-vectors-openended-qwen2.5-7b-it) | Qwen2.5-7B | Sycophancy | Activation mean-diff | Parquet |
| [shiv96/steering-vectors-openended-phi3.5-mini-it](https://huggingface.co/datasets/shiv96/steering-vectors-openended-phi3.5-mini-it) | Phi-3.5-Mini | Sycophancy | Activation mean-diff | Parquet |

## Creative Writing Control

Vectors for controlling writing style, tone, and narrative characteristics.

| Repository | Models | Traits | Format | Downloads |
|---|---|---|---|---|
| [jukofyork/creative-writing-control-vectors-v3.0](https://huggingface.co/jukofyork/creative-writing-control-vectors-v3.0) | 50+ models (Llama-3, Mistral, Gemma-2, Qwen, Mixtral, Yi, etc.) | Language (simple/ornate), Storytelling (explicit/descriptive), Character Focus (narration/dialogue), Empathy/Sociopathy, Honesty/Machiavellianism, Humility/Narcissism, Compassion/Sadism, Optimism/Nihilism | GGUF | 17.6k |
| [gghfez/GLM-5-control-vectors](https://huggingface.co/gghfez/GLM-5-control-vectors) | GLM-5 | Same 8 axes as jukofyork | GGUF | 582 |
| [gghfez/GLM-4.6-control-vectors](https://huggingface.co/gghfez/GLM-4.6-control-vectors) | GLM-4.6 | Same 8 axes | GGUF | 549 |
| [gghfez/Kimi-K2-Instruct-0905-control-vectors](https://huggingface.co/gghfez/Kimi-K2-Instruct-0905-control-vectors) | Kimi-K2 | Same 8 axes | GGUF | 387 |
| [gghfez/Qwen3.5-27b-control-vectors](https://huggingface.co/gghfez/Qwen3.5-27b-control-vectors) | Qwen3.5-27B | Same 8 axes | GGUF | 354 |
| [gghfez/Devstral-2-123B-Instruct-2512-control-vectors](https://huggingface.co/gghfez/Devstral-2-123B-Instruct-2512-control-vectors) | Devstral-2-123B | Same 8 axes | GGUF | 201 |
| [gghfez/Sorcerer_creative-writing-control-vectors](https://huggingface.co/gghfez/Sorcerer_creative-writing-control-vectors) | Sorcerer | Same 8 axes | GGUF | 165 |
| [gghfez/gemma-3-control-vectors](https://huggingface.co/gghfez/gemma-3-control-vectors) | Gemma-3 | Same 8 axes | GGUF | 88 |
| [trollkotze/miqu-control-vectors](https://huggingface.co/trollkotze/miqu-control-vectors) | Miqu-1-70B | Creative writing control | GGUF | 172 |
| [llmixer/ExllamaV2-Control-Vectors](https://huggingface.co/llmixer/ExllamaV2-Control-Vectors) | Any ExLlamaV2-compatible | Language, Optimism | ExLlamaV2 | - |

## Safety & Alignment

Vectors for controlling safety behaviors: refusal, instruction hierarchy, uncertainty, reward hacking.

| Repository | Models | Traits | Method | Format |
|---|---|---|---|---|
| [rotalabs/steering-vectors](https://huggingface.co/rotalabs/steering-vectors) | Qwen3-8B, Mistral-7B-v0.2, Gemma-2-9B-IT | Refusal, hierarchy, tool restraint, uncertainty | Activation steering | PyTorch (.pt) |
| [arianaazarbal/qwen3-8b-reward-hack-steering-vectors](https://huggingface.co/arianaazarbal/qwen3-8b-reward-hack-steering-vectors) | Qwen3-8B | Reward hacking reduction | Mean activation diff | PyTorch (.pt) |
| [auditing-agents/steering-vectors-llama70b](https://huggingface.co/datasets/auditing-agents/steering-vectors-llama70b) | Llama-70B | Safety auditing | - | - |

## Thinking & Reasoning

Vectors that modulate reasoning depth, accuracy, and thinking patterns.

| Repository | Models | Traits | Method | Format |
|---|---|---|---|---|
| [LoneResearch/thinking-steering-vectors](https://huggingface.co/datasets/LoneResearch/thinking-steering-vectors) | - | Thinking/reasoning behavior | Activation steering | - |
| [codelion/Qwen3-0.6B-pts-steering-vectors](https://huggingface.co/datasets/codelion/Qwen3-0.6B-pts-steering-vectors) | Qwen3-0.6B | Numerical accuracy, depth & thoroughness | Pivotal Token Search (PTS) | Parquet/JSON |
| [codelion/DeepSeek-R1-Distill-Qwen-1.5B-pts-steering-vectors](https://huggingface.co/datasets/codelion/DeepSeek-R1-Distill-Qwen-1.5B-pts-steering-vectors) | DeepSeek-R1-Distill-Qwen-1.5B | Reasoning improvement | PTS | Parquet/JSON |

**Related:** [LoneResearch/thinking-steering-visualizations](https://huggingface.co/datasets/LoneResearch/thinking-steering-visualizations), [thinking-steering-configs](https://huggingface.co/datasets/LoneResearch/thinking-steering-configs), [thinking-steering-generations](https://huggingface.co/datasets/LoneResearch/thinking-steering-generations), [thinking-steering-benchmarks](https://huggingface.co/datasets/LoneResearch/thinking-steering-benchmarks)

## Refusal Direction & Abliteration

Vectors and models with refusal directions identified or removed. These are research artifacts for studying safety mechanisms.

| Repository | Models | Method | Format | Downloads |
|---|---|---|---|---|
| [YunoAIdotcom/Qwen3-14B-RefusalDirection-ThinkingAware](https://huggingface.co/YunoAIdotcom/Qwen3-14B-RefusalDirection-ThinkingAware) | Qwen3-14B | Householder reflection, thinking-aware | SafeTensors | 60 |
| [thienkhoi01/qwen3-refusal-direction](https://huggingface.co/thienkhoi01/qwen3-refusal-direction) | Qwen3 | Refusal direction extraction | - | - |

**Notable abliterated models** (full models with refusal vectors removed):

| Repository | Base Model | Downloads |
|---|---|---|
| [huihui-ai/Qwen2.5-72B-Instruct-abliterated](https://huggingface.co/huihui-ai/Qwen2.5-72B-Instruct-abliterated) | Qwen2.5-72B | 165.7k |
| [mlabonne/gemma-3-12b-it-abliterated](https://huggingface.co/mlabonne/gemma-3-12b-it-abliterated) | Gemma-3-12B | 61.5k |
| [mlabonne/gemma-3-27b-it-abliterated-GGUF](https://huggingface.co/mlabonne/gemma-3-27b-it-abliterated-GGUF) | Gemma-3-27B | 30.9k |
| [huihui-ai/Huihui-Qwen3.5-27B-abliterated](https://huggingface.co/huihui-ai/Huihui-Qwen3.5-27B-abliterated) | Qwen3.5-27B | 36.8k |
| [huihui-ai/Huihui-Qwen3.5-35B-A3B-abliterated](https://huggingface.co/huihui-ai/Huihui-Qwen3.5-35B-A3B-abliterated) | Qwen3.5-35B-A3B | 34.4k |

## Domain-Specific Behavioral Steering

Vectors targeting specific professional domains.

### ModelOrganismsForEM

Organization focused on behavioral steering across medical, financial, and sports domains.

| Repository | Models | Domain |
|---|---|---|
| [ModelOrganismsForEM](https://huggingface.co/ModelOrganismsForEM) (org, ~38 repos) | Qwen2.5 (0.5B-32B), Llama-3.1-8B, Llama-3.2-1B | Bad medical advice, risky financial advice, extreme sports |

### darturi - MLP Sublayer Vectors

27 repos targeting specific MLP sublayers (gate_proj, up_proj, down_proj) derived from ModelOrganismsForEM:

| Repository | Models | Domain |
|---|---|---|
| [darturi](https://huggingface.co/darturi) (27 repos) | Qwen2.5-7B/14B, Llama-3.1-8B | Medical, financial, sports steering per MLP sublayer |

## Introspection & Concept Vectors

Vectors for abstract concept steering and introspection research.

| Repository | Models | Concepts | Method | Format |
|---|---|---|---|---|
| [elyhahami/llama-introspection-steering-vectors](https://huggingface.co/elyhahami/llama-introspection-steering-vectors) | Llama-3.1-8B | Dust, Satellites, Trumpets, Origami, Illusions, Fibonacci, Recursion, Betrayal, Appreciation, Shutdown | Activation steering | PyTorch (.pt) |

## Datasets

Datasets for training or generating steering vectors.

| Repository | Description | Size | Downloads |
|---|---|---|---|
| [LoneResearch/thinking-steering-vectors](https://huggingface.co/datasets/LoneResearch/thinking-steering-vectors) | Thinking/reasoning steering dataset | 2,048 rows | 2,050 |
| [Undi95/orthogonal-activation-steering-TOXIC](https://huggingface.co/datasets/Undi95/orthogonal-activation-steering-TOXIC) | Adversarial prompt/response pairs for toxicity steering | 7,381 rows | 96 |
| [codelion/Qwen3-0.6B-pts-steering-vectors](https://huggingface.co/datasets/codelion/Qwen3-0.6B-pts-steering-vectors) | PTS reasoning vectors for Qwen3-0.6B | - | 1,380 |

## Tools & Libraries

| Tool | Description | Link |
|---|---|---|
| [rotalabs-steer](https://pypi.org/project/rotalabs-steer/) | pip-installable library for applying steering vectors (Qwen3, Mistral, Gemma-2) | [HF](https://huggingface.co/rotalabs/steering-vectors) |
| [psyctl](https://github.com/ho4040/psyctl) | CLI tool for LLM personality steering using CAA and BiPO methods | [GitHub](https://github.com/ho4040/psyctl) |
| [llama.cpp](https://github.com/ggerganov/llama.cpp) | Supports GGUF control vectors natively via `--control-vector` flag | [GitHub](https://github.com/ggerganov/llama.cpp) |
| [repeng](https://github.com/vgel/repeng) | Representation engineering library for extracting and applying control vectors | [GitHub](https://github.com/vgel/repeng) |
| [ExLlamaV2](https://github.com/turboderp/exllamav2) | Supports control vectors via wrapper | [HF](https://huggingface.co/llmixer/ExllamaV2-Control-Vectors) |
| [OptiLLM](https://github.com/codelion/optillm) | Supports PTS steering vectors via `autothink` | [GitHub](https://github.com/codelion/optillm) |

## Papers

Foundational and related research papers on activation steering.

| Paper | Year | Key Contribution |
|---|---|---|
| [Steering Llama 2 via Contrastive Activation Addition](https://arxiv.org/abs/2312.06681) | 2023 | CAA - Contrastive Activation Addition method |
| [Personalized Steering via Bi-directional Preference Optimization](https://arxiv.org/abs/2406.00045) | 2024 | BiPO - Training-based steering vector extraction |
| [Representation Engineering](https://arxiv.org/abs/2310.01405) | 2023 | RepE - Reading and controlling LLM representations |
| [Refusal in Language Models Is Mediated by a Single Direction](https://arxiv.org/abs/2406.11717) | 2024 | Refusal direction identification and ablation |
| [Evaluating and Inducing Personality in Pre-trained Language Models](https://arxiv.org/abs/2206.07550) | 2022 | P2 - Personality prompts for LLMs |
| [Activation Addition: Steering Language Models Without Optimization](https://arxiv.org/abs/2308.10248) | 2023 | ActAdd - Algebraic activation steering |
| [Detecting the Disturbance: A Nuanced View of Introspective Abilities in LLMs](https://arxiv.org/abs/2512.12411) | 2025 | Introspection steering vectors |

---

## Contributing

Contributions are welcome! Please submit a pull request to add new steering vector resources.

### Guidelines

- Vectors must be publicly available on HuggingFace or GitHub
- Include the target model, traits/behaviors, extraction method, and format
- Provide a brief description of what the vectors do
- Prefer vectors with documentation and reproducible methods

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

This list is released under CC0. The individual resources linked have their own licenses.
