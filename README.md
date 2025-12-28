# LLaMA Finance Alignment (QLoRA + DPO)

This project demonstrates end-to-end domain adaptation and preference alignment of **LLaMA-3.1-8B** for finance and investing tasks.

## Pipeline
1. Base model: LLaMA-3.1-8B-Instruct (4-bit, Unsloth)
2. Domain SFT via QLoRA (finance concepts, quant reasoning)
3. Preference data generation using controlled prompts + external judge
4. DPO alignment with frozen reference
5. Rigorous 3-way evaluation (Original vs QLoRA vs DPO)

## Key Results
- QLoRA improves domain accuracy and structure
- DPO shifts preferences toward concision and correctness
- Evaluation framing materially affects winners

## Contents
- `generate_dpo_data.py` – preference data generation
- `train_dpo.py` – DPO alignment
- `eval_3way.py` – rigorous evaluation
- `requirements.txt`

## Notes
Model weights are not included. Scripts assume local or HF adapters.

## Author
Kevin Li
