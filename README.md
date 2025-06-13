<div align="center">   
  
# Motion-R1: Chain-of-Thought Reasoning and Reinforcement Learning for Human Motion Generation

</div>

## [Project Page](https://motion-r1.github.io/) | [Paper](https://arxiv.org/abs/2506.10353)

# News
- **[2025/6/12]** Repository Initialization.

## Abstract
Recent advances in large language models, especially in natural language understanding and reasoning, have opened new possibilities for text-to-motion generation. Although existing approaches have made notable progress in semantic alignment and motion synthesis, they often rely on end-to-end mapping strategies that fail to capture deep linguistic structures and logical reasoning. Consequently, generated motions tend to lack controllability, consistency, and diversity. To address these limitations, we propose \textbf{Motion-R1}, a unified motion-language modeling framework that integrates a Chain-of-Thought mechanism. By explicitly decomposing complex textual instructions into logically structured action paths, Motion-R1 provides high-level semantic guidance for motion generation, significantly enhancing the model's ability to interpret and execute multi-step, long-horizon, and compositionally rich commands. To train our model, we adopt Group Relative Policy Optimization, a reinforcement learning algorithm designed for large models, which leverages motion quality feedback to optimize reasoning chains and motion synthesis jointly. Extensive experiments across multiple benchmark datasets demonstrate that Motion-R1 achieves competitive or superior performance compared to state-of-the-art methods, particularly in scenarios requiring nuanced semantic understanding and long-term temporal coherence. The code, model and data will be publicly available.

![teaser](./assets/motionr1-main.pdf)
## Method Overview

The framework consists of two stages: (1) MotionCoT Data Engine uses DeepSeek-R1 to generate CoT-style motion planning traces in <think>, <output>, and <Motion> format to fine-tune an LLM; (2) GRPO-based training ranks grouped outputs by format, motion, and semantic rewards to optimize the LLM via reinforcement learning.


![pipeline](./assets/motionr1-pipeline.pdf)


## BibTeX

```bibtex
@misc{ouyang2025motionr1chainofthoughtreasoningreinforcement,
      title={Motion-R1: Chain-of-Thought Reasoning and Reinforcement Learning for Human Motion Generation}, 
      author={Runqi Ouyang and Haoyun Li and Zhenyuan Zhang and Xiaofeng Wang and Zheng Zhu and Guan Huang and Xingang Wang},
      year={2025},
      eprint={2506.10353},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2506.10353}, 
}
