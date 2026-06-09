# Google Colab GPU Reference

GPU options available on Google Colab as of June 2026.

## Overview

| GPU | Architecture | VRAM | bf16 | FP8 | Colab Tier | Approx. \$/hr |
|-----|-------------|------|------|-----|-----------|---------------|
| **T4** | Turing | 15 GB | No | No | Free | \$0.12 |
| **L4** | Ada Lovelace | 22.5 GB | Yes | No | Pro | \$0.17 |
| **A100** | Ampere | 40 / 80 GB | Yes | No | Pro+ | \$0.54–0.75 |
| **G4** (RTX PRO 6000) | Blackwell | 96 GB | Yes | Yes | Pro+ | \$0.87 |
| **H100** | Hopper | 80 GB | Yes | Yes | Pro+ | ~\$1.50+ |

## Key Differences for Local LLM Inference

### bf16 vs fp16

The T4 lacks hardware bf16 support and falls back to fp16. bf16 has a wider
dynamic range (same exponent bits as fp32) which makes inference more stable,
especially for larger models. All other Colab GPUs support bf16 natively.

### VRAM and Model Size

| VRAM | Native bf16 model size | 4-bit quantised model size | Example models |
|------|------------------------|---------------------------|----------------|
| 15 GB (T4) | ~3–4 GB comfortably | ~7–8 GB | Qwen2.5-1.5B, Gemma-2-2B, Phi-4-mini |
| 22.5 GB (L4) | ~5–6 GB | ~12–14 GB | Qwen2.5-7B, Llama-3.1-8B |
| 40 GB (A100) | ~10–12 GB | ~25–30 GB | Qwen2.5-32B, Mixtral-8x7B |
| 80–96 GB (H100/G4) | ~20–25 GB | ~50–60 GB | Llama-3.3-70B, DeepSeek-R1-32B |

Larger VRAM allows bigger models, longer context windows, and higher batch
sizes — all of which improve answer quality and throughput.

### FlashAttention

PyTorch's `scaled_dot_product_attention` automatically selects the best
available backend. FlashAttention 2 is available on Ampere+ (A100, H100, L4)
and significantly speeds up long-context inference.

## Disclaimer

**Pricing, availability, and GPU options change frequently.** The figures above
are approximate snapshots and may not reflect current rates or your region.
Always verify directly in your Colab session via the "View resources" panel or
by running `nvidia-smi`. The authors assume no responsibility for incurred
costs.
