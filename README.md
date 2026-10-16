<h1 align="center">Md Romyull Islam</h1>
<p align="center"><b>CS PhD candidate at Kennesaw State University (May 2027)</b><br>
I build efficient LLM inference systems for phones, edge devices and CXL hybrid memory.</p>

<p align="center">
  <a href="https://romyullislam.fyi"><img src="https://img.shields.io/badge/Website-romyullislam.fyi-0A66C2?style=flat-square&logo=googlechrome&logoColor=white" alt="Website"></a>
  <a href="https://scholar.google.com/citations?user=DhGIUA8AAAAJ&hl=en"><img src="https://img.shields.io/badge/Google%20Scholar-Publications-4285F4?style=flat-square&logo=googlescholar&logoColor=white" alt="Google Scholar"></a>
  <a href="https://www.linkedin.com/in/romyull-islam/"><img src="https://img.shields.io/badge/LinkedIn-romyull--islam-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

My research makes large language models run efficiently where memory, energy and heat are scarce:

- **On-device LLM inference.** KV-cache management that keeps a model within a phone's memory, energy and thermal budget ([μKV](https://github.com/Romyull-Islam/EndurKV), my dissertation topic). Measurement studies of small language and vision-language models on Jetson Orin and Raspberry Pi (IEEE IPCCC 2024, IEEE MASS 2025).
- **Memory systems for LLMs.** Splitting fast memory between model weights and prefetching on hybrid DRAM-NAND CXL devices ([SemSched](https://github.com/Romyull-Islam/SemSched)). Activation sparsity and delta prefetching to cut weight traffic (IPCCC 2024, Euro-Par 2025, ICPP 2026).
- **Efficient fine-tuning.** Data-free per-layer precision allocation for quantized LoRA ([AQLoRA](https://github.com/Romyull-Islam/AQLoRA)).

I build each idea into a real engine (llama.cpp) or a calibrated simulator, and measure it on Snapdragon phones, NVIDIA GPUs and edge boards. I have 12 peer-reviewed papers, 4 of them first-authored.

## Featured projects

| Project | What it is |
|---|---|
| [**μKV** (EndurKV)](https://github.com/Romyull-Islam/EndurKV) | KV-cache eviction with in-place compaction inside llama.cpp for LLM inference on a phone. 4.8x faster decode, 62% less energy and a 13x smaller cache on a Snapdragon 8 Elite Gen 5. C++, Android, Vulkan |
| [**SemSched**](https://github.com/Romyull-Islam/SemSched) | Trades memory capacity for prefetch bandwidth in LLM inference on hybrid DRAM-NAND CXL devices. Leads four published offloading policies in all twelve configurations, on a simulator calibrated against gem5, DRAMsim3 and LLMCompass. Python |
| [**AQLoRA**](https://github.com/Romyull-Islam/AQLoRA) | Zero-search per-layer precision allocation for quantized LoRA fine-tuning, set by one data-free CPU pass. Trains 11.1% faster than tuned QLoRA across six models from 1.4B to 14B. [arXiv:2608.23816](https://arxiv.org/abs/2608.23816). PyTorch, PEFT, bitsandbytes |
| [**SLMs on the edge**](https://github.com/Romyull-Islam/SLM) | Data and scripts for the IEEE IPCCC 2024 paper on the performance of small language models on Raspberry Pi, Jetson Orin and Mac mini. |
| [**VLM benchmarking**](https://github.com/Romyull-Islam/VLM-Benchmarking) | Accuracy, time and energy benchmarking of small vision-language models on Jetson AGX Orin, built on VLMEvalKit. |
| [**Build, Train, Deploy**](https://github.com/Romyull-Islam/llm_booklet) | An open five-week LLM course in PyTorch: a transformer from scratch, mixture-of-experts, LoRA fine-tuning, tool-using agents with MCP, and RAG. |
| [**MoE predictive prefetch**](https://github.com/Romyull-Islam/cxl-moe-predictive-prefetch) | Predicts which experts a mixture-of-experts LLM will activate a few layers ahead and prefetches them. Gives a 3.0–3.6x simulated per-token speedup on Mixtral, DeepSeek-MoE and Qwen-MoE. PyTorch |

## Selected publications

- **NeuroPrefetcher**: Storage-Aware Sparse LLM Inference via Delta Prefetching. *ICPP 2026* (to appear)
- **Characterizing and Understanding Energy Footprint and Efficiency of Small Language Model on Edges**. *IEEE MASS 2025* (first author)
- **A Sparsity Predicting Approach for Large Language Models via Activation Pattern Clustering**. *Euro-Par 2025*
- **Characterizing and Understanding the Performance of Small Language Models on Edge Devices**. *IEEE IPCCC 2024* (first author)

The full list is on [Google Scholar](https://scholar.google.com/citations?user=DhGIUA8AAAAJ&hl=en).

## Toolbox

C, C++, Python, CUDA · PyTorch, Hugging Face Transformers and PEFT, llama.cpp, vLLM · Android NDK, Vulkan · gem5, DRAMsim3 · Linux, Git, Docker
