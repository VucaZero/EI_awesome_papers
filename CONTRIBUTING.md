# Contributing

本仓库采用小组协作维护方式，所有新增内容应尽量保证可检索、可复用、可追溯。

## Workflow

```bash
git clone https://github.com/VucaZero/EI_awesome_papers.git
cd EI_awesome_papers
git checkout -b yourname/topic-name
```

完成修改后：

```bash
git add .
git commit -m "docs: add note for paper title"
git push -u origin yourname/topic-name
```

随后在 GitHub 发起 Pull Request。

## Paper Note Rules

- 单篇论文笔记放入 `papers/` 下最匹配的方向目录。
- 综述、tutorial、position paper 放入 `papers/surveys/`。
- 主题总结、路线图、方法对比放入 `topics/`。
- 数据集、benchmark、代码项目等资源放入 `resources/`。
- 新增论文笔记后同步更新 `indexes/paper-index.csv`。

## File Naming

单篇笔记统一使用：

```text
yyyy-venue-topic-short-title.md
```

字段说明：

- `yyyy`：论文年份
- `venue`：会议、期刊或来源，例如 `cvpr`、`iclr`、`arxiv`
- `topic`：主题关键词，例如 `vln`、`objectnav`、`episodic-memory`
- `short-title`：论文标题简写，使用小写英文与连字符

## Review Checklist

- 基本信息是否完整：标题、作者、年份、venue、链接。
- 一句话总结是否清楚说明问题、方法和结果。
- 方法部分是否写清输入、输出、核心模块和训练策略。
- 实验部分是否记录数据集、benchmark、metric 和关键结论。
- 是否写出对组内研究的启发。
- 是否更新相关 index。

