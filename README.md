<img src="https://hilpisch.com/tpq_logo_bic.png" alt="TPQ Logo" width="350" align="right" />

<br clear="right" />

# colab — GPU-Powered Notebooks

A collection of Google Colab use cases: free (or low-cost) GPU workflows, local LLM inference, training snippets, and more.

&copy; Dr. Yves J. Hilpisch (The AI Engineer)<br>AI-Powered by Different LLMs.

<img src="https://hilpisch.com/colab_viz_small.png" alt="GPU-powered Google Colab learning path" width="70%" />

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

### Section 1 — GPU-Powered ML, Data, and Quant Finance

- `01_hardware_accelerated_ml.ipynb` — Dramatic GPU speed-ups: Random Forest, K-Means, matrix multiplication, and MLP training (CPU vs T4 GPU).
- `02_gpu_dataframes_cudf.ipynb` — GPU-accelerated pandas workflows with RAPIDS cuDF: groupby, merge, rolling window, and string filtering on synthetic data.
- `03_gpu_monte_carlo_finance.ipynb` — Monte Carlo option pricing, barrier options, and Greeks on CPU vs GPU.
- `04_gpu_monte_carlo_calibration.ipynb` — GPU-accelerated Monte Carlo calibration for synthetic option prices.

### Section 2 — Deep Learning and Generative AI on Colab

- `05_cnn_image_classification.ipynb` — Train a small CNN on Fashion-MNIST with CPU vs GPU timing.
- `06_transformer_timeseries.ipynb` — Train a small Transformer for one-step-ahead synthetic time-series forecasting.
- `07_local_llm_colab_gpu.ipynb` — Download a small open-weight LLM and chat with it on a free T4 GPU.
- `08_stable_diffusion_gpu.ipynb` — Text-to-image generation with Stable Diffusion on a free T4 GPU.

### Section 3 — AI Engineering Workflows

- `09_yoctoGPT_walden_char.ipynb` — Clone yoctoGPT, download Thoreau's *Walden*, and train a tiny character-level GPT.
- `10_lora_finetuning.ipynb` — Adapt a small LLM with LoRA fine-tuning on a free T4 GPU.
- `11_rag_faiss.ipynb` — Build a retrieval-augmented generation workflow with embeddings and FAISS.
- `12_coding_llm_cli.ipynb` — Serve `qwen2.5-coder:7b` with Ollama, expose the OpenAI-compatible API via `cloudflared`, and use it with curl, the OpenAI Python client, and aider.

## About The Python Quants

[The Python Quants GmbH](https://tpq.io) provides code-first online training in Python, data science, artificial intelligence, quantitative finance, algorithmic trading, and crypto technologies.

Our connected training landscape includes:

* **The Data Scientist** ([thedatascientist.dev](https://thedatascientist.dev)): Python, data science, machine learning, and portfolio projects.
* **Certificate in Python for Finance** ([cpf.tpq.io](https://cpf.tpq.io)): quant finance, financial data science, asset management, algorithmic trading, derivatives analytics, and AI for finance.
* **The AI Engineer** ([theaiengineer.dev](https://theaiengineer.dev)): production-grade AI engineering, LLM applications, agents, automation, and deployment.
* **The Crypto Engineer** ([thecryptoengineer.dev](https://thecryptoengineer.dev)): Bitcoin, blockchain, crypto technologies, digital assets, and decentralized finance.

We continuously integrate modern tools and technologies, from Python and open-source data science libraries to GPUs, CUDA, cloud platforms, GenAI, local LLMs, AI agents, and advanced quantitative workflows.

We use and leverage Google Colab throughout our programs to make modern compute workflows directly executable in the browser.

This repository reflects our mission: to make modern ML, AI, and quant finance workflows practical, executable, and accessible.

## Disclaimer

This repository and its contents are provided solely for illustration and educational purposes. The Python Quants GmbH is not affiliated with, endorsed by, or sponsored by Google, and receives no compensation from Google for creating or sharing this content. No guarantees or representations of any kind are given, express or implied, including but not limited to fitness for a particular purpose or non-infringement, to the extent permitted by law. Use at your own risk.
