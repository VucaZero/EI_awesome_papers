# EI Group Paper

面向具身智能科研小组的论文阅读、笔记沉淀与主题梳理仓库。

本仓库用于统一管理：

- 日常论文精读笔记
- 某一主题方向的阶段性综述与整理
- 统一的笔记模板与命名规范
- 具身智能任务、环境、数据集、指标的共享知识库

## 1. 仓库范围

当前重点覆盖但不限于以下方向：

- `VLA`：Vision-Language-Action，大模型驱动的感知到动作系统
- `VLN`：Vision-and-Language Navigation，指令导航与主动探索
- `EQA`：Embodied Question Answering，具身问答与主动感知
- `MANI`：Manipulation / Mobile Manipulation，操作与移动操作
- `AFF`：Affordance / Skill Grounding，可供性、技能发现与 grounding
- `WM`：World Model / Planning，世界模型、规划与预测
- `BENCH`：Benchmark / System / Platform，基准、系统、平台与实验框架
- `SURV`：Survey / Tutorial / Position Paper，综述与路线图

更细的任务、仿真环境、数据集与常用实验指标见 [TAXONOMY.md](./TAXONOMY.md)。

## 2. 目录结构

```text
EI_group_paper/
├── README.md
├── TAXONOMY.md
├── TEMPLATES.md
├── .gitignore
└── awesome_papers/
    ├── README.md
    ├── VLA/
    ├── VLN/
    ├── EQA/
    ├── MANI/
    ├── AFF/
    ├── WM/
    ├── BENCH/
    └── SURV/
```

## 3. 协作者如何提交笔记

### 3.1 推荐协作方式

默认远程仓库：

`https://github.com/VucaZero/EI-group-paper.git`

推荐使用 `Pull Request` 流程：

1. 克隆仓库到本地
2. 创建个人工作分支
3. 按模板撰写笔记并放入对应主题目录
4. 提交 commit 并推送分支
5. 发起 PR，等待组内 review 后合并到 `main`

### 3.2 本机使用 Git 的最小流程

首次使用：

```bash
git clone \
  https://github.com/VucaZero/EI-group-paper.git

cd EI-group-paper

git checkout \
  -b yourname/topic-brief
```

完成笔记后：

```bash
git add \
  awesome_papers/VLA/paper_notes/paper__VLA__2025__zhou__openvla.md

git commit \
  -m "docs: add VLA note for OpenVLA"

git push \
  -u origin \
  yourname/topic-brief
```

如果你拥有直接写权限，也建议优先走分支提交，而不是直接推 `main`。

## 4. 笔记提交规范

- 所有新增笔记必须遵循 [TEMPLATES.md](./TEMPLATES.md) 中的模板之一。
- 所有文件必须放在正确的主题目录下。
- 主题综述、阶段性总结、系统分析类内容放在各主题目录下的 `topic_summaries/`。
- 单篇论文精读笔记放在各主题目录下的 `paper_notes/`。
- 文件名请使用全小写英文与下划线，避免空格与中文文件名。

## 5. Review 关注点

组内 review 主要看以下几点：

- 论文任务设定是否描述准确
- 方法核心假设是否抓住
- 实验设置与指标是否记录完整
- 局限性与未来可做空间是否分析到位
- 和小组当前研究方向的关系是否明确

## 6. 维护建议

- 每周至少做一次主题目录整理，避免重复笔记和链接失效。
- 对同一篇论文，如果已有笔记，后续补充应优先更新原文件，而不是重复新建。
- 对一个方向连续阅读 5 篇以上后，建议追加一篇 `analysis__*.md` 或 `survey__*.md` 作为阶段总结。

## 7. 当前仓库状态

- 已初始化为 Git 仓库骨架
- 预留了与 GitHub 远程仓库 `origin` 的连接位置
- 后续可直接补充内容、提交、推送
