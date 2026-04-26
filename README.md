# EI Awesome Papers

具身智能方向论文、资源、主题总结与实验入口的协作仓库。

本仓库重点服务小组日常读论文、做方向梳理、追踪 benchmark 与沉淀可复用资料。当前主要关注 embodied navigation、memory navigation、active inference，以及与这些方向相关的数据集、仿真平台、开源项目和综述。

## Repository Structure

```text
EI_awesome_paper/
├── README.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── CHANGELOG.md
├── LICENSE
├── papers/
│   ├── embodied-navigation/
│   ├── memory-navigation/
│   ├── active-inference/
│   └── surveys/
├── topics/
├── resources/
├── templates/
└── indexes/
```

## Main Areas

| Area | Description |
| --- | --- |
| `papers/embodied-navigation/` | VLN、ObjectNav、PointNav、map-based navigation、uncertainty-aware navigation |
| `papers/memory-navigation/` | episodic memory、semantic memory、working memory、cognitive map、memory-augmented policy |
| `papers/active-inference/` | free energy principle、active perception、uncertainty minimization |
| `papers/surveys/` | survey、tutorial、position paper 与方向综述 |
| `topics/` | 主题总结、路线对比、阶段性组内分析 |
| `resources/` | 数据集、benchmark、开源项目、工具、作者与实验室资源 |
| `templates/` | 论文笔记、综述笔记、项目资源、数据集、主题总结模板 |
| `indexes/` | 机器可读或人工可读的论文、代码、数据集索引 |

## Naming Convention

单篇论文笔记命名：

```text
yyyy-venue-topic-short-title.md
```

示例：

```text
2024-cvpr-vln-mapgpt.md
2025-iclr-memory-navigation-episodic-transformer.md
2023-neurips-active-inference-free-energy-planning.md
```

## How to Contribute

1. 从 `main` 创建个人分支。
2. 在 `templates/` 中选择合适模板。
3. 把论文笔记放到对应 `papers/` 子目录。
4. 如果是主题整理，放到 `topics/`。
5. 同步更新 `indexes/paper-index.csv` 或相关资源索引。
6. 提交 Pull Request。

详细规范见 [CONTRIBUTING.md](./CONTRIBUTING.md)。

## Key Indexes

- [Paper Index](./indexes/paper-index.csv)
- [Topic Index](./indexes/topic-index.md)
- [Code Index](./indexes/code-index.md)
- [Dataset Index](./indexes/dataset-index.md)
- [Reading List](./resources/reading-list.md)

