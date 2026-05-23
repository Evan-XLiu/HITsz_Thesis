# 论文题目 Thesis Title

《基于强化学习的人形机器人运动技能学习与泛化研究》

Research on Humanoid Robot Motion Skill Learning and Generalization Based on Reinforcement Learning


## 论文简介 Abstract

本项目围绕人形机器人运动技能学习问题，研究基于强化学习的整身动作跟踪与泛化方法。论文以“专家数据预处理 - 动作重定向 - 强化学习动作跟踪 - 鲁棒性与泛化评估”为主线，构建了从人体运动数据到机器人可执行控制策略的完整技术流程。

论文首先基于 AMASS 等公开人体运动数据建立专家动作处理流程，通过 SMPL 运动解析、关键点拓扑映射、体型拟合、数据清洗与时序动作重定向，将人体动作序列转换为人形机器人可执行的参考轨迹；随后在 Isaac Gym / MuJoCo 仿真环境中构建整身动作跟踪任务，采用相位建模、非对称 Actor-Critic 与 PPO 优化框架训练控制策略，并结合参考状态初始化、终止课程学习和安全正则项提升训练稳定性与物理可行性。

研究目标是使人形机器人在高保真仿真环境中学习多类参考动作，并在不同动作类型、扰动条件与场景变化下保持较好的跟踪精度、稳定性、鲁棒性和泛化能力。

This project focuses on humanoid robot motion skill learning and studies a reinforcement-learning-based whole-body motion tracking and generalization framework. The thesis follows the pipeline of expert data preprocessing, motion retargeting, reinforcement-learning-based motion tracking, and robustness/generalization evaluation, building a complete workflow from human motion data to executable robot control policies.

It first constructs an expert motion processing pipeline based on public human motion datasets such as AMASS. Through SMPL motion parsing, keypoint topology mapping, body shape fitting, data cleaning, and temporal motion retargeting, human motion sequences are converted into executable reference trajectories for a humanoid robot. It then builds a whole-body motion tracking task in Isaac Gym / MuJoCo simulation environments, where phase modeling, an asymmetric Actor-Critic architecture, and PPO are used to train the control policy, together with reference state initialization, termination curriculum learning, and safety regularization to improve training stability and physical feasibility.

The main objective is to enable a humanoid robot to learn multiple reference motions in high-fidelity simulation while maintaining good tracking accuracy, stability, robustness, and generalization performance under different motion categories, disturbances, and scene variations.

## 主要内容 Main Contents

1. 梳理人形机器人敏捷控制、人体动作模仿、动作重定向与仿真鲁棒性等相关研究进展。
2. 基于 AMASS/SMPL 构建专家数据预处理流程，完成坐标规范化、关键点拓扑映射与体型拟合。
3. 设计面向人形机器人的两阶段时序动作重定向与基于仿真的专家数据清洗方法。
4. 在 Isaac Gym / MuJoCo 中构建整身动作跟踪任务，建立相位条件观测、低层 PD 控制与非对称 Actor-Critic 策略结构。
5. 采用 PPO 优化目标，并引入参考状态初始化、终止课程学习和安全正则项提升训练稳定性与物理可行性。
6. 通过主实验、基线对比、可视化分析以及鲁棒性与泛化测试验证所提方法的有效性。

1. Review related work on agile humanoid control, human motion imitation, motion retargeting, and robustness in simulation-based training.
2. Build an expert data preprocessing pipeline based on AMASS/SMPL, including coordinate normalization, keypoint topology mapping, and body shape fitting.
3. Design a two-stage temporal motion retargeting method and simulation-based expert data cleaning for humanoid robots.
4. Construct a whole-body motion tracking task in Isaac Gym / MuJoCo with phase-conditioned observations, low-level PD control, and an asymmetric Actor-Critic policy architecture.
5. Optimize the policy with PPO and introduce reference state initialization, termination curriculum learning, and safety regularization to improve training stability and physical feasibility.
6. Validate the method through main experiments, baseline comparisons, qualitative visualization, and robustness/generalization tests.

## 论文结构 Thesis Structure

- 第 1 章：绪论
- 第 2 章：相关研究综述
- 第 3 章：专家数据处理与动作重定向
- 第 4 章：基于强化学习的运动跟踪方法
- 第 5 章：实验设计与结果分析
- 第 6 章：总结与展望

- Chapter 1: Introduction
- Chapter 2: Related Work Review
- Chapter 3: Expert Data Preprocessing and Motion Retargeting
- Chapter 4: Reinforcement Learning Based Motion Tracking
- Chapter 5: Experimental Design and Result Analysis
- Chapter 6: Conclusion and Prospect

## Project Structure

- `examples/hitbook/chinese/thesis.tex`
  Main thesis entry file that organizes the front matter, six main chapters, bibliography, and back matter.
- `examples/hitbook/chinese/front/`
  Front matter including the cover configuration, thesis metadata, Chinese abstract, and English abstract.
- `examples/hitbook/chinese/body/`
  Main chapter files, including introduction, related work review, expert data preprocessing and motion retargeting, reinforcement-learning-based motion tracking, experiments, and conclusion.
- `examples/hitbook/chinese/back/`
  Back matter including publications, acknowledgements, authorization pages, and optional appendix-related content.
- `examples/hitbook/chinese/reference.bib`
  Bibliography database covering humanoid robotics, reinforcement learning, motion imitation, and simulation-related references.
- `examples/hitbook/chinese/hithesisbook.cls`
  Thesis class file and formatting rules used by the current project template.

## Build Instructions

Compile the thesis in the following directory:

```bash
cd examples/hitbook/chinese
latexmk -xelatex -interaction=nonstopmode thesis.tex
```

After compilation, the output file is:

- `examples/hitbook/chinese/thesis.pdf`
