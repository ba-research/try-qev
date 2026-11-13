# Qev 1.0: comparison with same-size decision models

Snapshot: 12 November 2026. Qev 1.0 results below are from our 2,352-item [OpenDecisions](https://huggingface.co/datasets/jgeuter/OpenDecisions) development validation run, not a fresh independent test. Capability averages the benchmark's intelligence and calibration scores; it is not accuracy. Other scores are reported by their authors or the benchmark authors using their own serving configurations. We have not independently rerun these competitors. Tables list identified comparators, not a complete ranking or proof of global state of the art. Different benchmarks cannot be subtracted.

## 0.8B

| Model | Base | OpenDecisions Capability | Comparison to Qev 1.0 0.8B |
| --- | --- | ---: | --- |
| [Qev 1.0 0.8B](https://huggingface.co/ba-research/Qev1.0-Qwen3.5-0.8B) | Qwen3.5-0.8B | 46.85 | Our development result |
| [Kev 0.8B](https://huggingface.co/jaredpalmer/kev-0.8b) | Qwen3.5-0.8B-Base | Not verified | 14,032 monthly downloads; same-suite gap unknown |
| [StartLux 1.1 0.8B Instant](https://huggingface.co/startlux-models/StartLux-Decision-v1.1-0.8B-Instant) | Qwen3.5-0.8B | Not verified | Gap unknown; same-suite run needed |
| [AA Decision 0.8B](https://huggingface.co/analogalok/Qwen3.5-0.8B-AA-Decision) | Qwen3.5-0.8B | Not verified | Gap unknown; card reports different benchmarks |
| [labqoat QEV 0.8B](https://huggingface.co/labqoat/qev-0.8b) | Qwen3.5-0.8B | Not verified | Different project; gap unknown |

## 2B

| Model | Base | OpenDecisions Capability | Comparison to Qev 1.0 2B |
| --- | --- | ---: | --- |
| [Qev 1.0 2B](https://huggingface.co/ba-research/Qev1.0-Qwen3.5-2B) | Qwen3.5-2B | 55.23 | Our development result |
| [Decider 2B](https://huggingface.co/Mapika/decider-2b) | Qwen3.5-2B-Base | Not verified | 7,391 monthly downloads; same-suite gap unknown |
| [StartLux 1.1 2B Instant](https://huggingface.co/startlux-models/StartLux-Decision-v1.1-2B-Instant) | Qwen3.5-2B | Not verified | Gap unknown; same-suite run needed |
| [joey-1](https://huggingface.co/baselabs/joey-1) | Qwen3.5-2B | Not verified | Gap unknown; same-suite run needed |
| [Jev-Style 2B Decision v3](https://huggingface.co/chaoliangUNSW/Jev-Style-2B-Decision-v3) | Qwen3.5-2B | Not verified | Gap unknown; same-suite run needed |

## 4B

| Model | Base | OpenDecisions Capability | Comparison to Qev 1.0 4B |
| --- | --- | ---: | --- |
| [StartLux 1.1 4B Instant](https://huggingface.co/startlux-models/StartLux-Decision-v1.1-4B-Instant) | Qwen3.5-4B | 82.2 | 16.22 points above Qev; 19.73% relative gap |
| [Kev 4B](https://huggingface.co/jaredpalmer/kev-4b) | Qwen3.5-4B-Base | Not verified | 12,499 monthly downloads; same-suite gap unknown |
| [Jeff 1.1 Qwen 4B](https://huggingface.co/jgeuter/Jeff-1.1-Qwen-27B) | Qwen3.5-4B | 79.3 | 13.32 points above Qev |
| [Wald 4B v2.0](https://huggingface.co/datasets/jgeuter/OpenDecisions/blob/main/README.md) | Qwen3.5-4B | 77.1 | 11.12 points above Qev; some questions use reasoning |
| [Torchcast decision 4B v1.1](https://huggingface.co/datasets/jgeuter/OpenDecisions/blob/main/README.md) | Qwen3.5-4B | 73.5 | 7.52 points above Qev |
| [decider 4B v2](https://huggingface.co/datasets/jgeuter/OpenDecisions/blob/main/README.md) | Qwen3.5-4B | 70.8 | 4.82 points above Qev |
| [Jeff 1.0 Qwen 4B](https://huggingface.co/jgeuter/Jeff-1.0-Qwen-4B) | Qwen3.5-4B | 68.0 | 2.02 points above Qev; model-card figure |
| [Qev 1.0 4B](https://huggingface.co/ba-research/Qev1.0-Qwen3.5-4B) | Qwen3.5-4B | 65.98 | Our development result |
| [nanohunch decider 4B](https://huggingface.co/ubermenchh/nanohunch-decider-4b) | Qwen3-4B | 57.1 | 8.88 points below Qev; four-seed mean, different Qwen generation |

The 82.2 and 79.3 results are reported in [Jeff 1.1's same-set evaluation table](https://huggingface.co/jgeuter/Jeff-1.1-Qwen-27B). The [OpenDecisions leaderboard](https://huggingface.co/datasets/jgeuter/OpenDecisions/blob/main/README.md) reports 67.7 for Jeff 1.0, versus 68.0 on its model card. Different service configurations can affect results; differences around two points should not be treated as decisive. Our 4B target against the identified 82.2 reference is at least **78.09 Capability** (95% of 82.2); Qev 1.0 does not meet it. This is a provisional validation target, not proof of generalization. We have no measured same-suite SOTA gap or numeric target for 0.8B or 2B yet.

Download counts are Hugging Face's rolling monthly counts observed 12 November 2026 for the linked original repositories, not deduplicated people, quality measurements or sums across quantizations. Kev and Decider are included because of their adoption and relevance; popularity itself does not establish they are the strongest on this benchmark.

We are pursuing fresh, leakage-screened paired evaluations and improved training at all three sizes. Existing Qev training source provenance, rights and independent generalization remain unresolved; see the individual model cards. We will update these tables when comparable, reproducible evidence is available.

The evaluation plan targets at least three typed-decision benchmarks: OpenDecisions, [JevBench's public 231-item subset](https://huggingface.co/datasets/kshitijthakkar/nirnaya-jevbench-public-eval-v1), and a third suite such as [DecisionBench](https://huggingface.co/datasets/Hanno-Labs/decision-bench), subject to confirming its terms and scoring. Qev and peer results on the latter two are **not yet measured** in this comparison; none of the OpenDecisions gaps above can be transferred to them. The public 231 subset is not the full sealed JevBench leaderboard.
