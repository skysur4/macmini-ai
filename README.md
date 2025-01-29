# macmini-ai
맥미니 ai 설정 절차

---
1️⃣ Best AI Model for Coding & Chat
For 16GB RAM (Balanced)
- Model: CodeLlama-13B-Instruct (Q4 GGUF)
- Use Case: More detailed code generation, explanations, and debugging.
- Runner: Ollama, GPT4All, or llama.cpp.
- Storage: ~8GB (Q4 quantized).

For 32GB RAM (Power User)
- Model: Deepseek-Coder-33B (Q4 GGUF)
- Use Case: Advanced code suggestions, AI pair programming.
- Runner: llama.cpp (Metal acceleration).
- Storage: ~16GB (Q4 quantized).
---
2️⃣ Best AI Runner for macOS (Optimized)
✅ Easiest Setup: Ollama (Auto-optimizes models).
✅ Most Customizable: llama.cpp (Best for performance tuning).
✅ Best GUI Option: GPT4All (Easy to use).

🔹 Install Ollama (Recommended)
```
brew install ollama
```

```
ollama run hf.co/bartowski/CodeLlama-13B-MORepair-GGUF:Q5_K_M
```

```
ollama run hf.co/bartowski/Yi-Coder-9B-Chat-GGUF::Q5_K_M
```
