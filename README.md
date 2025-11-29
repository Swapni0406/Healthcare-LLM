# Healthcare LLM Fine-Tuning (LoRA + HuggingFace)

Starter repository for fine-tuning an LLM for healthcare Q&A using PEFT/LoRA and serving via FastAPI.

## Structure
- data/: example train/test JSONL files
- scripts/finetune.py: training script
- api/app.py: FastAPI server for inference
- models/: model output (gitignored)
- requirements.txt

## Quickstart
1. Create a virtual env and install deps:
   ```bash
   pip install -r requirements.txt
   ```
2. Edit scripts/finetune.py or set env vars BASE_MODEL, BATCH, EPOCHS.
3. Train:
   ```bash
   python scripts/finetune.py
   ```
4. Serve:
   ```bash
   export MODEL_DIR=models/healthcare-llm
   uvicorn api.app:app --host 0.0.0.0 --port 8000
   ```


