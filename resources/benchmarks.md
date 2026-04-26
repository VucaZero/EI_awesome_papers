# Benchmarks

| Category | Name | Alias | Used For | Description | Official Link | GitHub / Code Link | Related Dataset / Platform | Notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Task Tag | PointNav | Point-goal Navigation | Navigation task | 点目标导航 | - | - | Habitat-Lab; Gibson; HM3D; MP3D | 基础导航任务 |
| Task Tag | ObjectNav | Object-goal Navigation | Navigation task | 类别目标导航 | - | - | Habitat-Lab; HM3D; MP3D; RoboTHOR | Embodied AI 常用任务 |
| Task Tag | VLN | Vision-and-Language Navigation | Navigation task | 语言指令导航 | - | - | R2R; RxR; REVERIE; VLN-CE | 与语言理解强相关 |
| Task Tag | VLN-CE | Continuous VLN | Navigation task | 连续环境 VLN | https://jacobkrantz.github.io/vlnce/ | https://github.com/jacobkrantz/VLN-CE | Habitat-Lab; Matterport3D | 连续动作空间设置 |
| Task Dataset | PointNav-Habitat | Habitat PointNav | Navigation benchmark | Habitat 点目标导航 benchmark | https://aihabitat.org/challenge/2020/ | https://github.com/facebookresearch/habitat-lab | Gibson; MP3D; HM3D | 可由不同场景生成 |
| Task Dataset | ObjectNav-Habitat | Habitat ObjectNav | Navigation benchmark | Habitat 类别目标导航 benchmark | https://aihabitat.org/challenge/2020/ | https://github.com/facebookresearch/habitat-lab | HM3D; MP3D | Habitat Challenge 常用 |

## Common Metrics

| Metric | Used For | Meaning | Notes |
| --- | --- | --- | --- |
| `SR` | Navigation / manipulation | Success Rate | 最基础成功率 |
| `SPL` | Navigation | Success weighted by Path Length | 同时考虑成功与路径效率 |
| `nDTW` | VLN | Trajectory similarity | 适合比较轨迹贴近程度 |
| `SDTW` | VLN | Success weighted nDTW | 结合成功与轨迹相似度 |
| `NE` | Navigation | Navigation Error | 终点到目标点距离 |
| `TL` | Navigation | Trajectory Length | 轨迹长度 |

