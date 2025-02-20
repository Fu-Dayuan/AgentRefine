
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
The performance comparison of AgentRefine and other methods across different families and sizes.The underlined text indicates that the training data is sampled in the same environment as the task and is considered as held-in evaluation.

<table>
<thead>
<tr>
 <th align="center" rowspan="2">Method</th> <th align="center" colspan="2">Alfworld</th> <th align="center" colspan="2">BabyAI</th><th align="center" colspan="2">SciWorld</th><th align="center" colspan="2">PDDL</th><th align="center" colspan="2">Jericho</th>
</tr>
<tr>
  <th>Success</th><th>Progress</th><th>Success</th><th>Progress</th><th>Success</th><th>Progress</th><th>Success</th><th>Progress</th><th>Success</th><th>Progress</th>
</tr>
</thead>
<tbody><tr>
<td align="center" colspan="11"><strong>GPT Series</strong></td>
</tr>
<tr>
  <td>GPT-4o</td><td>66.4</td><td>79.9</td><td>48.2</td><td>64.1</td><td>40</td><td>76.9</td><td>61.7</td><td>69.8</td><td>10.0</td><td>34.0</td>
</tr>
<tr>
  <td>GPT-4o-mini</td><td>37.3</td><td>65.0</td><td>36.6</td><td>51.9</td><td>23.3</td><td>49.8</td><td>25.0</td><td>49.1</td><td>10.0</td><td>28.5</td>
</tr>
<tr>
<td align="center" colspan="11"><strong>LLaMA-3-8B Series</strong></td>
</tr>
<tr>
  <td>LLaMA-3-8B-Instruct</td><td>22.4</td><td>46.1</td><td>45.5</td><td>56.5</td><td>7.8</td><td>41.1</td><td>10.0</td><td>38.4</td><td>0.0</td><td>24.3</td>
</tr>
<tr>
  <td>AgentGen</td><td>29.1</td><td>47.6</td><td>20.5</td><td>35.0</td><td>-</td><td>-</td><td>11.7</td><td>23.0</td><td>-</td><td>-</td>
</tr>
<tr>
  <td>AgentGym</td><td><ins>61.9</ins></td><td><ins>76.9</ins></td><td><ins>47.3</ins></td><td><ins>61.4</ins></td><td><ins>18.9</ins></td><td><ins>47.5</ins></td><td>1.7</td><td>16.6</td><td>0.0</td><td>12.9</td>
</tr>
<tr>
  <td>Agent-FLAN</td><td><ins>67.2</ins></td><td><ins>79.7</ins></td><td>25.0</td><td>35.3</td><td>1.1</td><td>10.9</td><td>8.3</td><td>25.5</td><td>0.0</td><td>10.1</td>
</tr>
<tr>
  <td>AgentRefine</td><td>44.8</td><td>63.8</td><td>37.5</td><td>50.4</td><td>14.4</td><td>42.6</td><td>16.6</td><td>37.8</td><td>10.0</td><td>32.3</td>
</tr>
<tr>
<td align="center" colspan="11"><strong>Mistral Series</strong></td>
</tr>
<tr>
  <td>Mistral-7B-Instruct-v0.3</td><td>12.4</td><td>35.9</td><td>36.6</td><td>45.8</td><td>6.7</td><td>24.7</td><td>13.3</td><td>27.8</td><td>0.0</td><td>17.3</td>
</tr>
<tr>
  <td>AgentGym</td><td><ins>76.9</ins></td><td><ins>86.7</ins></td><td><ins>40.2</ins></td><td><ins>56.3</ins></td><td><ins>15.6</ins></td><td><ins>48.3</ins></td><td>1.7</td><td>7.3</td><td>0.0</td><td>13.0</td>
</tr>
<tr>
  <td>Agent-FLAN</td><td><ins>77.6</ins></td><td><ins>87.6</ins></td><td>15.2</td><td>21.0</td><td>0</td><td>6.7</td><td>0</td><td>3.2</td><td>0.0</td><td>0.7</td>
</tr>
<tr>
  <td>AgentRefine</td><td>51.4</td><td>68.8</td><td>25.9</td><td>42.4</td><td>4.4</td><td>22.4</td><td>11.7</td><td>32.8</td><td>5.0</td><td>28.8</td>
</tr>
<tr>
<td align="center" colspan="11"><strong>LLaMA-3-70B Series</strong></td>
</tr>
<tr>
  <td>LLaMA-3-70B-Instruct</td><td>67.2</td><td>75.2</td><td>48.2</td><td>61.8</td><td>42.2</td><td>75.4</td><td>55.0</td><td>79.8</td><td>25.0</td><td>46.4</td>
</tr>
<tr>
  <td>Agent-FLAN</td><td><ins>80.5</ins></td><td><ins>86.8</ins></td><td>32.1</td><td>41.2</td><td>5.5</td><td>16.4</td><td>25.0</td><td>53.7</td><td>0.0</td><td>13.6</td>
</tr>
<tr>
  <td>AgentRefine</td><td>67.2</td><td>72.1</td><td>44.6</td><td>59.7</td><td>17.7</td><td>46.4</td><td>38.3</td><td>58.6</td><td>15.0</td><td>37.2</td>
</tr>
</tbody></table>

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
