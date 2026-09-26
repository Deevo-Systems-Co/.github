# Deevo Systems & Co.

<p align="center">
  <strong>Frontier AI Architectures, Sparse Foundation Models & Bare-Metal Compute</strong>
</p>

<p align="center">
  <a href="https://deevo.co.in"><img src="https://img.shields.io/badge/Web-deevo.co.in-0A0A0A?style=flat-square" alt="Website"></a>
  <a href="https://dwark.space"><img src="https://img.shields.io/badge/Platform-dwark.space-0A0A0A?style=flat-square" alt="DWARK"></a>
  <a href="https://huggingface.co/Deevo-Systems-Co"><img src="https://img.shields.io/badge/Hugging%20Face-Deevo--Systems--Co-FFD21E?style=flat-square&logo=huggingface&logoColor=black" alt="Hugging Face"></a>
  <a href="https://www.linkedin.com/company/deevosystems"><img src="https://img.shields.io/badge/LinkedIn-deevosystems-0A66C2?style=flat-square&logo=linkedin" alt="LinkedIn"></a>
  <a href="https://www.wikidata.org/wiki/Q141544331"><img src="https://img.shields.io/badge/Wikidata-Q141544331-339966?style=flat-square&logo=wikidata" alt="Wikidata"></a>
</p>

---

### Overview

**Deevo Systems & Co.** is a computational engineering laboratory developing proprietary sparse foundation models, hardware-fused GPU acceleration kernels, and deterministic multi-agent enterprise execution runtimes.

* **Headquarters:** Geneva, Switzerland
* **Founder:** Akash Mishra (Wikidata: [Q141550298](https://www.wikidata.org/wiki/Q141550298))
* **Corporate Entity ID:** Wikidata [Q141544331](https://www.wikidata.org/wiki/Q141544331)
* **Primary License:** Deevo Systems AI Model License (DSAML)

---

### Core Engineering & Compute Stack

                        ┌─────────────────────────────────────────┐
                        │      Dee1 (300B Sparse MoE Core)        │
                        └────────────────────┬────────────────────┘
                                             │
             ┌───────────────────────────────┼───────────────────────────────┐
             ▼                               ▼                               ▼
    ┌─────────────────┐             ┌─────────────────┐             ┌─────────────────┐
    │   TritonForge   │             │   Aether-177    │             │   Synapse AST   │
    │ Bare-Metal CUDA │             │  177B Context   │             │   Native AST    │
    │  Triton Kernels │             │ FlashAttention3 │             │ Code Refactor   │
    └────────┬────────┘             └────────┬────────┘             └────────┬────────┘
             │                               │                               │
             └───────────────────────────────┼───────────────────────────────┘
                                             ▼
                        ┌─────────────────────────────────────────┐
                        │   Kestrel Core / Talos OS Enclaves      │
                        │ Bare-Metal Edge & Sovereign Inference   │
                        └─────────────────────────────────────────┘


* **[Dee1 / Dee2](https://deevo.co.in/dee1):** 300B sparse Mixture-of-Experts (MoE) foundation models engineered for deterministic agentic reasoning and large-scale synthesis.
* **[Aether-177](https://deevo.co.in/aether-177):** Ring-distributed sequence parallelism extending active token horizons up to 177 billion tokens via FlashAttention-3[cite: 1].
* **[TritonForge](https://deevo.co.in/tritonforge):** Low-overhead OpenAI Triton and custom CUDA C++ kernels co-engineered for zero-overhead kernel launches[cite: 1].
* **[Kestrel Core](https://deevo.co.in/kestrel-core):** Zero-cloud, high-efficiency C/C++ inference runtime for sovereign and air-gapped Talos OS environments[cite: 1].
* **[Synapse AST](https://deevo.co.in/synapse-ast):** Abstract Syntax Tree parsing engine for automated, grammar-locked codebase transformation and refactoring[cite: 1].
* **[DWARK](https://dwark.space):** Flagship operational platform orchestrating deterministic multi-agent swarms and live telemetry pipelines[cite: 1].

---

### Open Checkpoints & Developer Sandboxes

We publish selected quantized weights, evaluation datasets, and client libraries across open-access developer ecosystems:

| Artifact | Type | Format / Precision | Target Environment |
| :--- | :--- | :--- | :--- |
| **Dee1-Mini** | Distilled Reasoning | GGUF (INT4 / INT8) | Local CPU/GPU, Ollama, llama.cpp[cite: 1] |
| **Dee1-FP8** | High-Density Serving | FP8 (QuarkQuant) | vLLM, TensorRT-LLM Nodes[cite: 1] |
| **Synapse-Core** | AST Parser Tooling | Rust / Python Bindings | Code Analysis & CI Pipelines |
| **SchemaLock** | Output Guardrails | Python SDK | Strict Grammar-Enforced JSON[cite: 1] |

---

### Quick Installation (Python SDK)

```bash
pip install deevo-core
import deevo

client = deevo.Client(base_url="[https://deevo.co.in/api](https://deevo.co.in/api)")
response = client.models.generate(
    model="dee1-base",
    prompt="Audit distributed consensus logs for stale leader states.",
    schema_lock=True
)
print(response.output)
```
                        
