# MLX-LM-LoRA Example Notebooks

[![MLX](https://img.shields.io/badge/MLX-Apple%20Silicon-orange.svg)](https://github.com/ml-explore/mlx)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Official example notebooks for [MLX-LM-LoRA](https://github.com/Goekdeniz-Guelmez/mlx-lm-lora) - a powerful library for efficient LLM training on Apple Silicon.

## 🚀 Overview

This repository contains real-world, production-ready examples demonstrating how to use **MLX-LM-LoRA** for various training scenarios on Apple Silicon Macs. Each notebook is a complete, step-by-step tutorial that you can run directly on your Mac.

### Why MLX-LM-LoRA?

- ⚡ **Ultra-efficient**: Train 4B+ parameter models on 16GB RAM
- 🎯 **Long context**: Support for 32K+ token sequences
- 🔧 **LoRA optimized**: Memory-efficient fine-tuning with Low-Rank Adaptation
- 💾 **Quantization**: 4-bit, 6-bit, and 8-bit quantization support
- 🍎 **Apple Silicon native**: Optimized for M1/M2/M3/M4 chips

## 📚 Example Notebooks

### 1. Fine-Tuning (SFT)
Located in `finetuning/`

Learn how to fine-tune large language models using Supervised Fine-Tuning (SFT):
- **Qwen3_4B_Instruct.ipynb**: Complete tutorial for instruction fine-tuning
  - Dataset preparation and formatting
  - LoRA configuration and optimization
  - Training with long context (32K+ tokens)
  - Model evaluation and comparison
  - Saving and sharing on Hugging Face Hub

### 2. Preference Optimization
Located in `preference/`

Coming soon! Examples including:
- Direct Preference Optimization (DPO)
- RLHF with human preferences
- Reward model training
- Policy optimization

### 3. Reinforcement Learning
Located in `rl/`

Coming soon! Examples including:
- Proximal Policy Optimization (PPO)
- Reward-based training
- Multi-turn dialogue optimization
- Task-specific RL fine-tuning

## 🛠️ Installation

### Prerequisites
- Apple Silicon Mac (M1/M2/M3/M4 series)
- macOS 13.0 or later
- Python 3.8+
- At least 16GB unified memory (24GB+ recommended for larger models)

### Setup

1. Clone this repository:
```bash
git clone https://github.com/Goekdeniz-Guelmez/mlx-lm-lora-example-notebooks.git
cd mlx-lm-lora-example-notebooks
```

2. Install MLX-LM-LoRA:
```bash
pip install -U mlx-lm-lora
```

3. Open the notebook you want to try:
```bash
jupyter notebook finetuning/Qwen3_4B_Instruct.ipynb
```

Or use VS Code with the Jupyter extension for the best experience!

## 🎯 Quick Start

1. **Choose your use case**: Pick a notebook from the categories above
2. **Follow the tutorial**: Each notebook has detailed explanations for every step
3. **Customize**: Adjust hyperparameters for your specific needs
4. **Train**: Run the cells and watch your model improve!
5. **Share**: Upload your fine-tuned adapters to Hugging Face Hub

## 📊 Performance Tips

### Memory Optimization
- Adjust `batch_size` based on your available RAM
- Use `gradient_accumulation_steps` to simulate larger batches
- Enable `grad_checkpoint` for training with ultra-long contexts
- Use 4-bit quantization for maximum memory efficiency

### Speed Optimization
- Increase `seq_step_size` if you have more memory
- Use larger `batch_size` on M2/M3 Ultra systems
- Adjust `num_layers` in LoRA config to train fewer layers

### Quality Optimization
- Increase LoRA `rank` for more expressive adaptations
- Train for more epochs on larger datasets
- Use higher precision (6-bit or 8-bit) if memory allows
- Fine-tune validation strategy for your specific task

## 🤝 Contributing

We welcome contributions! If you have interesting examples or improvements:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-example`)
3. Commit your changes (`git commit -m 'Add amazing example'`)
4. Push to the branch (`git push origin feature/amazing-example`)
5. Open a Pull Request

## 📖 Resources

- **MLX-LM-LoRA Library**: [github.com/Goekdeniz-Guelmez/mlx-lm-lora](https://github.com/Goekdeniz-Guelmez/mlx-lm-lora)
- **MLX Framework**: [github.com/ml-explore/mlx](https://github.com/ml-explore/mlx)
- **Documentation**: Check individual notebook files for detailed explanations

## 🌟 Featured Examples

### Training a 4B Model with 32K Context on 16GB RAM
See `finetuning/Qwen3_4B_Instruct.ipynb` for a complete example of:
- Loading and quantizing Qwen3-4B-Instruct
- Preparing instruction datasets
- Training with LoRA on long contexts
- Evaluating improvements
- Sharing your adapter

**Typical training time**: 10-30 minutes on M2 Pro/Max

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Apple MLX team for the amazing framework
- Hugging Face for model hosting and datasets
- The open-source AI community for continuous inspiration

---

**Ready to start training?** Pick a notebook and dive in! 🚀

For questions or issues, please open an issue on [GitHub](https://github.com/Goekdeniz-Guelmez/mlx-lm-lora-example-notebooks/issues).
