
 # <div align="center"> <img src="./picture/refine.png" width="5%">  AgentRefine: Enhancing Agent Generalization through Refinement Tuning<div>



<div align="center">
  <a><img alt="Static Badge" src="https://img.shields.io/badge/made_with-Python-blue"></a>
  <a href="https://arxiv.org/pdf/2501.01702" target="_blank"><img src=https://img.shields.io/badge/arXiv-b5212f.svg?logo=arxiv></a>
</div>

## 💥 News
- [01/2025] 🔥 Our paper has been accepted by **ICLR 2025**. 

- [01/2025] 🔥 We will release our model, inference code in one month! 



## 💡 Overview
We introduce **AgentRefine**, an agent synthesis framework that enables models to learn from observations within trajectories to correct their own errors. **AgentRefine** significantly outperforms state-of-the-art agent tuning works in terms of generalization capabilities across diverse agent tasks. Our findings establish a relationship between agent generalization and self-improvement, offering a new paradigm for future research.

<img src="./picture/AgentRefine.png">


## ✈️ Training Data

We provided our training data in HuggingFace

[AgentRefine-gpt4o-32000](https://huggingface.co/datasets/fudayuan/AgentRefine-gpt4o-32000) 

[AgentRefine-gpt4o-64000](https://huggingface.co/datasets/fudayuan/AgentRefine-gpt4o-64000) 

[AgentRefine-deepseek-4000](https://huggingface.co/datasets/fudayuan/AgentRefine-deepseek-4000)

⭐ **We will also provide inference code and model soon! Thanks for waiting!**

## 📊 Results



## 📖 Citation 
Please kindly cite our paper if it helps your research:
```bibtex
@inproceedings{fu2025agentrefine,
  title={AgentRefine: Enhancing Agent Generalization through Refinement Tuning},
  author={Dayuan Fu and Keqing He and Yejie Wang and Wentao Hong and Zhuoma GongQue and Weihao Zeng and Wei Wang and Jingang Wang and Xunliang Cai and Weiran Xu},
  booktitle={The Thirteenth International Conference on Learning Representations},
  year={2025},
  url={https://openreview.net/forum?id=FDimWzmcWn}
}
```
