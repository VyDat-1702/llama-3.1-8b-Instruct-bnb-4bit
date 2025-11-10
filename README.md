# Llama 3 Vietnamese Multi-Task Model

[![License](https://img.shields.io/badge/License-Llama%203-blue.svg)](https://llama.meta.com/llama3/license/)
[![Model](https://img.shields.io/badge/🤗%20Model-VyDat/llama3--8b--multitask--10k-yellow)](https://huggingface.co/VyDat/llama3-8b-multitask-10k)
[![Base Model](https://img.shields.io/badge/Base-Llama%203.2%201B-green)](https://huggingface.co/unsloth/Llama-3.2-1B-Instruct)

A Vietnamese multi-task language model fine-tuned from Llama 3.2-1B-Instruct, specialized for general conversation and Vietnamese Sign Language (VSL) translation tasks.

## Key Features

- **Vietnamese Conversation**: Natural dialogue and question-answering in Vietnamese
- **Vi to VSL Translation**: Converts Vietnamese text into Vietnamese Sign Language structure
- **VSL to Vi Translation**: Converts VSL structure back into complete Vietnamese sentences

## Technical Architecture

- **Base Model**: unsloth/Llama-3.2-1B-Instruct
- **Fine-tuning Method**: PEFT with LoRA (Low-Rank Adaptation)
- **Framework**: Unsloth (optimized training pipeline)
- **LoRA Configuration**:
  - Rank (r): 64
  - Alpha: 128
  - Target Modules: q_proj, k_proj, v_proj, o_proj, gate_proj, up_proj, down_proj

## Training Details

- **Dataset Size**: 10,000 multi-task examples
- **Method**: Supervised fine-tuning with LoRA adapters
- **Hardware Requirements**: GPU with 8GB+ VRAM recommended

## Usage

This model is a PEFT adapter that needs to be loaded with the base model `unsloth/Llama-3.2-1B-Instruct`. For detailed usage instructions, please refer to the [Hugging Face Model Card](https://huggingface.co/VyDat/llama3-8b-multitask-10k).

## Repository Contents

- `adapter_config.json` - LoRA adapter configuration
- `adapter_model.safetensors` - Adapter weights
- `README.md` - This documentation

## Limitations

- Optimized primarily for Vietnamese language tasks
- VSL translation follows a specific structural format
- May require additional fine-tuning for domain-specific applications
- Best performance achieved with clear, well-structured prompts

## Contributing

Contributions are welcome! You can:

- Report bugs or issues
- Suggest improvements
- Submit pull requests

## License

This model is released under the same license as the Llama 3.2 base model. Please review [Llama 3 License](https://llama.meta.com/llama3/license/) for usage terms.

## Acknowledgments

- **Meta AI** for the Llama 3.2 base model
- **Unsloth AI** for the optimized training framework
- Vietnamese Sign Language community for linguistic insights

## Contact

For questions or collaboration opportunities, please open an issue in this repository.

---

**Note**: This model is designed for research and educational purposes. Always verify critical translations with professional VSL interpreters.
