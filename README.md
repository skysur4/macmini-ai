# macmini-ai
맥미니 ai 설정 절차


1️⃣ Best AI Model for Coding & Chat
---
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


2️⃣ Best AI Runner for macOS (Optimized)
---
✅ Easiest Setup: Ollama (Auto-optimizes models).  
✅ Most Customizable: llama.cpp (Best for performance tuning).  
✅ Best GUI Option: GPT4All (Easy to use).  


3️⃣ Install
---
Ollama
```
brew install ollama
```
React/Vue specialized
```
ollama run hf.co/bartowski/starcoder2-15b-instruct-v0.1-GGUF:Q5_K_M
```
JAVA specialized
```
ollama run hf.co/bartowski/DeepSeek-Coder-V2-Lite-Instruct-GGUF:Q5_K_M
```
All-round
```
ollama run hf.co/TheBloke/CodeLlama-13B-Instruct-GGUF:Q5_K_M
```
Candidate (tesT)
```
ollama run hf.co/bartowski/Yi-Coder-9B-Chat-GGUF::Q5_K_M
```
---
Web UI
```
pip install open-webui
open-webui serve
```
---
Nginx
```
brew install nginx
Edit /usr/local/etc/nginx/nginx.conf:
```
Nginx config
```
server {
    listen 80;
    server_name ai.cooltime.io;

    location / {
        proxy_pass http://localhost:8000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }
}
```
Nginx reload
```
sudo nginx -s reload
```

4️⃣ Update
---
Brew
```
brew update
```
Python
```
brew upgrade python
```
Web UI
```
pip install --upgrade open-webui
```
