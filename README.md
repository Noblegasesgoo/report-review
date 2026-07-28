# 报告解读

大模型技术报告的**通俗交互解读**合集：把长篇技术报告拆解为生活化比喻 + 可点击的动画演示，支持知识、技术平权。

## 在线访问

| 分类 | 内容 | 链接 |
|---|---|---|
| 🤖 kimi | 看懂 Kimi K3：2.8 万亿参数的开源模型是怎么炼成的 | [在线阅读](https://noblegasesgoo.github.io/report-review/kimi/) |

## 目录结构

```
├── kimi/            # Kimi 系列模型报告解读
│   └── index.html   # Kimi K3 技术报告交互解读（单文件，零依赖）
├── README.md
└── LICENSE          # MIT
```

## 当前收录

### Kimi K3 技术报告解读（`kimi/index.html`）

基于 Moonshot AI 官方《Kimi K3: Open Frontier Intelligence》47 页技术报告制作的单文件交互页面，内容包括：

- **数学基础 × 8 组交互动画**：词嵌入语义地图、注意力加权混合、Softmax 投票箱、SiTU-GLU 激活函数曲线、梯度爆炸模拟、MoE 路由数学、MXFP4 量化画质对比、Scaling Law 曲线
- **六大核心发明**：Stable LatentMoE（896 专家分诊台）、KDA + Gated MLA 混合注意力、注意力残差 AttnRes、MXFP4 原生量化、多教师 On-Policy 蒸馏、原生视觉 MoonViT-V2
- **幕后基建**：MoonEP / FlashKDA / AgentEnv / KDA 感知前缀缓存
- **成绩单与开源协议**：官方基准对比、成本效率分析、Kimi K3 License 条款解读

页面为纯 HTML/CSS/JS 单文件，无外部依赖，可直接用浏览器打开本地文件，或托管到任意静态服务器。

## 许可证

[MIT License](LICENSE) © Limin Zhao

页面内容基于各厂商公开发布的技术报告整理，通俗类比仅用于帮助理解，技术细节以原始报告为准。
