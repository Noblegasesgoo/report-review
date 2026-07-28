# 报告解读

大模型技术报告与论文的**通俗交互解读**合集：把长篇技术报告/论文拆解为生活化比喻 + 可点击的动画演示，支持知识、技术平权。

## 在线访问

| 分类 | 内容 | 链接 |
|---|---|---|
| 📑 技术报告 | 看懂 Kimi K3：2.8 万亿参数的开源模型是怎么炼成的 | [在线阅读](https://noblegasesgoo.github.io/report-review/reports/kimi-k3/) |
| 📄 论文 | 看懂 D-Score：一次前向传播，从大模型「心声」里听出幻觉 | [在线阅读](https://noblegasesgoo.github.io/report-review/papers/d-score/) |
| 📄 论文 | 看懂「规划物理学」：解剖智能体的长程规划能力如何长出、塑形、合体 | [在线阅读](https://noblegasesgoo.github.io/report-review/papers/agentic-distillation/) |
| 📄 论文 | 看懂奖励模型的「记性」：反事实记忆解剖 RLHF 考官的三大病灶 | [在线阅读](https://noblegasesgoo.github.io/report-review/papers/reward-model-memory/) |
| 📄 论文 | 看懂 PIVOT：一排 query 拼一次单，稀疏注意力索引提速 4.8× 而精度不掉 | [在线阅读](https://noblegasesgoo.github.io/report-review/papers/pivot-sparse-attention/) |

## 目录结构

按内容类型分类：厂商技术报告放 `reports/`，arXiv 等学术论文放 `papers/`，每篇解读一个子目录。

```
├── reports/                     # 厂商技术报告解读
│   └── kimi-k3/
│       └── index.html           # Kimi K3 技术报告交互解读（单文件，零依赖）
├── papers/                      # 学术论文解读
│   ├── d-score/
│   │   └── index.html           # D-Score 幻觉检测论文交互解读（单文件，零依赖）
│   ├── agentic-distillation/
│   │   └── index.html           # 长程规划「物理学」论文交互解读（单文件，零依赖）
│   ├── reward-model-memory/
│   │   └── index.html           # 奖励模型记忆机制论文交互解读（单文件，零依赖）
│   └── pivot-sparse-attention/
│       └── index.html           # PIVOT 稀疏注意力索引论文交互解读（单文件，零依赖）
├── README.md
└── LICENSE                      # MIT
```

## 当前收录

### Kimi K3 技术报告解读（`reports/kimi-k3/index.html`）

基于 Moonshot AI 官方《Kimi K3: Open Frontier Intelligence》47 页技术报告制作的单文件交互页面，内容包括：

- **数学基础 × 8 组交互动画**：词嵌入语义地图、注意力加权混合、Softmax 投票箱、SiTU-GLU 激活函数曲线、梯度爆炸模拟、MoE 路由数学、MXFP4 量化画质对比、Scaling Law 曲线
- **六大核心发明**：Stable LatentMoE（896 专家分诊台）、KDA + Gated MLA 混合注意力、注意力残差 AttnRes、MXFP4 原生量化、多教师 On-Policy 蒸馏、原生视觉 MoonViT-V2
- **幕后基建**：MoonEP / FlashKDA / AgentEnv / KDA 感知前缀缓存
- **成绩单与开源协议**：官方基准对比、成本效率分析、Kimi K3 License 条款解读

页面为纯 HTML/CSS/JS 单文件，无外部依赖，可直接用浏览器打开本地文件，或托管到任意静态服务器。

### D-Score 论文解读（`papers/d-score/index.html`）

基于 arXiv 论文《D-Score: A Spectral Hidden-State Signal for Hallucination Detection in Large Language Models》（arXiv:2607.24586，博洛尼亚大学）制作的单文件交互页面，内容包括：

- **数学基础 × 1 组交互动画**：隐藏状态、奇异值分解（SVD）与奇异值谱的「尖」与「平」（衰减滑杆）
- **核心方法 × 2 组交互动画**：正常 vs 幻觉文本的谱对比与 D-Score 实时计算（τ 滑杆 + 冲突方向演示）、判定阈值 D̄ 的松紧权衡（混淆计数实时更新）
- **实验结果**：FAVA-Annotation 与 RAGTruth 完整结果表（表 1–2）、AUROC 亮点条形图、子集分析（表 3–4）与参数鲁棒性（附录 C）
- **局限与意义**：白盒限制、内部可见幻觉、长度影响与校准建议，所有关键结论均挂 ↗ 原文出处

### 长程规划「物理学」论文解读（`papers/agentic-distillation/index.html`）

基于 arXiv 论文《The Physics of Multi-Turn Long-Horizon Planning: From Pre-training to Post-training via Single- and Multi-Teacher On-Policy Agentic Distillation》（arXiv:2607.24720，中科院自动化所）制作的单文件交互页面，内容包括：

- **概念基础**：可控合成环境 Planning Gym（炼金/养殖/装配三域）、规划模式 vs 规划知识、GRPO vs OPD
- **预训练三发现 × 3 组交互动画**：世界模型 CoT vs 直接作答对比演示、数据配比滑杆（pass@8 跳变真实数字）、误差复利曲线
- **后训练三区域**：RL 不必要/有效/不支持三区域交互网格（GRPO/OPD 切换）
- **多教师蒸馏**：MOPD 共享/部分共享/冲突三种模式的规划分布 morph 动画

### 奖励模型记忆机制论文解读（`papers/reward-model-memory/index.html`）

基于 arXiv 论文《What do Reward Models Memorize?》（arXiv:2607.24484，阿姆斯特丹大学 ILLC + Google DeepMind）制作的单文件交互页面，内容包括：

- **概念基础 × 2 组交互动画**：Bradley-Terry 偏好概率滑杆、反事实记忆 CM 计算五步流程演示
- **核心方法**：TM×TG 记忆地图语义散点图（SAE 特征区域联动解读）、84 维特征 + SHAP 归因
- **三大病灶**：记忆错配（背简单题不背难题）、数据集捷径（模型身份/招募波次）、启发式过度泛化（更长=更好/顺从=更好）
- **局限与意义**：判别式 RM 的偏置结论与三味「药方」

### PIVOT 稀疏注意力索引论文解读（`papers/pivot-sparse-attention/index.html`）

基于 arXiv 论文《PIVOT: Efficient Query-Group Indexing for Token-Level Sparse Attention》（arXiv:2607.24593，腾讯）制作的单文件交互页面，内容包括：

- **三个观察 × 1 组交互动画**：相邻 query top-k 高度重叠、组大小 vs top-k 并集滑杆（论文实测数据）
- **核心方法 × 1 组对比动画**：DSA 逐 query 扫描 / PIVOT-Reuse / PIVOT-Refine 三模式扫描计数对比
- **实验结果 × 1 组滑杆动画**：上下文 4K–256K 索引器加速比（图 4 全部 28 个实测数据点）、RULER 128K 精度对照
- **局限与意义**：免训练即插即用替换 DSA 索引器，索引提速约 4.8× 而精度不掉

## 许可证

[MIT License](LICENSE)

页面内容基于各厂商公开发布的技术报告与论文整理，通俗类比仅用于帮助理解，技术细节以原始报告/论文为准。
