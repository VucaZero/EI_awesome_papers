# TAXONOMY

本文档用于统一当前小组在具身智能方向上的任务分类、环境资源、数据集与常用实验指标。

说明：

- 本表偏向“读论文与搭实验”所需的工作知识，而不是百科全书式罗列。
- 链接优先使用官方主页、官方文档或官方代码仓库。
- 若资源页面发生迁移，请优先更新为新的官方入口。

## 1. 主题缩写

| 缩写 | 全称 | 关注重点 | 典型内容 |
| --- | --- | --- | --- |
| `VLA` | Vision-Language-Action | 多模态大模型到策略执行 | 开放词汇操作、基础策略、机器人 agent |
| `VLN` | Vision-and-Language Navigation | 指令导航、探索、地图构建 | R2R、RxR、长期规划 |
| `EQA` | Embodied Question Answering | 主动感知与问答 | 任务驱动探索、信息采样 |
| `MANI` | Manipulation | 机械臂/移动操作 | 抓取、放置、装配、长程操作 |
| `AFF` | Affordance | 可供性建模、技能 grounding | skill discovery、动作可行性 |
| `WM` | World Model | 预测、规划、想象与模拟 | latent dynamics、planning、rollout |
| `BENCH` | Benchmark | 平台、基准、系统化评测 | simulator、leaderboard、评测体系 |
| `SURV` | Survey | 综述、tutorial、perspective | 方向梳理、开放问题、roadmap |

## 2. 任务视角

| 任务类别 | 常见输入 | 常见输出 | 关键挑战 | 代表资源 |
| --- | --- | --- | --- | --- |
| 指令导航 | 视觉观测 + 文本指令 | 离散/连续导航动作 | 长时序信用分配、环境泛化、语言 grounding | [Habitat](https://aihabitat.org/), [R2R](https://github.com/peteanderson80/Matterport3DSimulator), [RxR](https://github.com/google-research-datasets/RxR) |
| 具身问答 | 场景观测 + 问题 | 答案 + 探索轨迹 | 主动信息收集、任务相关感知 | [EQA v1](https://embodiedqa.org/), [AI2-THOR](https://ai2thor.allenai.org/) |
| 机械臂操作 | RGB/RGB-D/语言/状态 | 抓取、放置、轨迹控制 | 接触建模、长程操作、泛化到新物体 | [ManiSkill](https://maniskill.ai/), [RLBench](https://github.com/stepjam/RLBench) |
| 移动操作 | 导航观测 + 操作目标 | 复合动作序列 | 导航与操作耦合、任务分解 | [BEHAVIOR](https://behavior.stanford.edu/), [RoboCasa](https://robocasa.ai/) |
| VLA / 通用 agent | 图像/视频/文本/状态 | 动作 token 或控制命令 | 数据异构、行为对齐、闭环鲁棒性 | [OpenVLA](https://openvla.github.io/), [RT-2](https://robotics-transformer2.github.io/) |
| 世界模型与规划 | 轨迹、历史观测、动作 | 下一状态预测、value、plan | 可解释性、长时预测误差累积 | [Dreamer](https://danijar.com/project/dreamer/), [MuJoCo](https://mujoco.org/) |

## 3. 常见仿真环境与平台

| 平台 | 定位 | 适合任务 | 特点 | 官方链接 |
| --- | --- | --- | --- | --- |
| Habitat | 大规模 3D 场景仿真 | VLN、探索、EQA | 场景资源丰富，导航社区使用广 | [aihabitat.org](https://aihabitat.org/) |
| AI2-THOR | 交互式室内环境 | EQA、任务执行、交互推理 | 面向对象交互，入门较快 | [ai2thor.allenai.org](https://ai2thor.allenai.org/) |
| ManiSkill | 高性能操作仿真 | 机械臂操作、skill learning | 操作 benchmark 完整，训练效率高 | [maniskill.ai](https://maniskill.ai/) |
| Isaac Sim | 工业级机器人仿真 | 操作、感知、合成数据 | 与 NVIDIA 生态结合紧密 | [NVIDIA Isaac Sim](https://developer.nvidia.com/isaac/sim) |
| OmniGibson / iGibson | 交互式家居环境 | 移动操作、具身任务 | 适合复杂日常家务任务 | [OmniGibson](https://behavior.stanford.edu/omnigibson/), [iGibson](https://svl.stanford.edu/igibson/) |
| RoboCasa | 家居操作基准 | 移动操作、长程任务 | 面向家居 manipulation 的系统 benchmark | [robocasa.ai](https://robocasa.ai/) |
| MuJoCo | 通用物理仿真 | 控制、世界模型、强化学习 | 物理控制基准经典平台 | [mujoco.org](https://mujoco.org/) |
| RLBench | 视觉操作 benchmark | imitation / manipulation | 任务集合清晰，适合演示学习 | [RLBench GitHub](https://github.com/stepjam/RLBench) |

## 4. 场景与任务数据集

| 数据集 / 基准 | 类型 | 典型任务 | 说明 | 官方链接 |
| --- | --- | --- | --- | --- |
| Matterport3D | 真实室内场景 | VLN、3D 场景理解 | VLN 社区核心底座之一 | [matterport3d](https://niessner.github.io/Matterport/) |
| HM3D | 大规模室内场景 | 导航、探索、泛化评测 | Habitat 常用高质量场景集 | [HM3D](https://aihabitat.org/datasets/hm3d/) |
| R2R | 文本导航 | VLN | Room-to-Room 经典指令导航数据集 | [R2R Simulator Repo](https://github.com/peteanderson80/Matterport3DSimulator) |
| RxR | 多语言导航 | VLN、多语言 grounding | 指令更长、更细粒度 | [RxR](https://github.com/google-research-datasets/RxR) |
| ALFRED | 家居任务执行 | 指令执行、移动操作 | 强调长程决策与对象交互 | [askforalfred.com](https://askforalfred.com/) |
| BEHAVIOR-1K | 家庭活动任务 | 移动操作、复杂日常任务 | 大量日常行为与任务定义 | [BEHAVIOR](https://behavior.stanford.edu/) |
| ProcTHOR | 程序生成场景 | 泛化、数据生成 | 适合大量训练场景生成 | [ProcTHOR](https://procthor.allenai.org/) |
| Ego4D | 第一视角视频 | 技能学习、视频理解、规划 | 对具身视频建模有参考价值 | [ego4d-data.org](https://ego4d-data.org/) |

## 5. 实验常用指标

| 指标 | 常见任务 | 含义 | 备注 |
| --- | --- | --- | --- |
| `SR` | 导航、操作 | Success Rate，成功率 | 最基础指标 |
| `SPL` | 导航 | Success weighted by Path Length | 同时考虑成功与路径效率 |
| `nDTW` / `SDTW` | 指令导航 | 轨迹与参考轨迹相似度 | 常见于 VLN |
| `TL` | 导航 | Trajectory Length | 常与 `SR`、`SPL` 配合看 |
| `NE` | 导航 | Navigation Error | 目标点偏差距离 |
| `GC` / `PC` | 操作 | Grasp / Place Completion | 抓取、放置完成度 |
| `Return` | RL / world model | 累积回报 | 对 reward 设计敏感 |
| `Success@K` | 检索、候选规划 | Top-K 成功率 | 常见于规划或检索模块 |
| `Latency` | 系统类工作 | 推理时延 | 部署相关工作必须记录 |
| `Tokens / Steps` | VLA / agent | 推理或执行成本 | 适合做效率对比 |
| `Human Preference` | agent、开放任务 | 人类偏好评分 | 需明确标注评测协议 |
| `Calibration` | VLM / agent | 置信度与正确性匹配程度 | 有助于分析失败模式 |

## 6. 论文阅读时建议重点记录的信息

- 任务设定与问题定义是否清晰
- 训练数据来源与规模
- 动作空间是离散、连续还是 token 化
- 是否使用 world model / planner / memory / retrieval
- 实验平台、场景、数据集与评测协议
- 与组内当前方向最相关的模块和可复用思想

## 7. 常用资源入口

| 资源类型 | 名称 | 链接 |
| --- | --- | --- |
| 具身仿真平台 | Habitat | https://aihabitat.org/ |
| 家居交互平台 | AI2-THOR | https://ai2thor.allenai.org/ |
| 操作基准 | ManiSkill | https://maniskill.ai/ |
| 机器人仿真 | Isaac Sim | https://developer.nvidia.com/isaac/sim |
| 家务任务生态 | BEHAVIOR / OmniGibson | https://behavior.stanford.edu/ |
| 家居操作 benchmark | RoboCasa | https://robocasa.ai/ |
| 物理控制平台 | MuJoCo | https://mujoco.org/ |

## 8. 后续维护原则

- 新增主题缩写时，先补充本文件，再新建目录。
- 对同名 benchmark、数据集、环境，统一使用官方名称，不随论文简称。
- 如果某篇论文提出新的指标定义，应在笔记中写出公式或评测协议差异。
