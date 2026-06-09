# colab — GPU-Powered Notebooks

A collection of Google Colab use cases: free (or low-cost) GPU workflows, local LLM inference, training snippets, and more.

<img src="https://theaiengineer.dev/tae_logo_gw_flatter.png" alt="TAE Logo" width="350" />

&copy; Dr. Yves J. Hilpisch (The AI Engineer)<br>AI-Powered by Different LLMs.

## Structure

| Path | Description |
|------|-------------|
| `notebooks/` | Ready-to-run Colab notebooks |
| `notebooks/colab_gpus.md` | GPU reference and comparison table |

## Quick Start

1. Open any notebook in `notebooks/` with **Open in Colab**.
2. Select a GPU runtime: `Runtime → Change runtime type → T4 GPU`.
3. Run cells top-to-bottom.

## Notebooks

- `00_hardware_accelerated_ml.ipynb` — Dramatic GPU speed-ups: Random Forest, K-Means, matrix multiplication, and MLP training (CPU vs T4 GPU).
- `01_local_llm_colab_gpu.ipynb` — Download a small open-weight LLM (e.g. Qwen2.5-1.5B) and chat with it on a free T4 GPU.
- `02_stable_diffusion_gpu.ipynb` — Text-to-image generation with Stable Diffusion on a free T4 GPU, including step-count ablation and negative prompts.
- `03_gpu_dataframes_cudf.ipynb` — GPU-accelerated pandas workflows with RAPIDS cuDF: groupby, merge, rolling window, and string filtering on synthetic data.

## Disclaimer

This repository and its contents are provided solely for illustration and educational purposes. No guarantees or representations of any kind are given, express or implied, including but not limited to fitness for a particular purpose or non-infringement, to the extent permitted by law. Use at your own risk.
