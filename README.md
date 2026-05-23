# 论文题目 Thesis Title

《基于强化学习的人形机器人运动技能学习与泛化研究》

Research on Humanoid Robot Motion Skill Learning and Generalization Based on Reinforcement Learning


## 论文简介 Abstract

本项目围绕人形机器人运动技能学习问题，研究基于强化学习的整身动作跟踪与泛化方法。论文以“专家数据预处理 - 动作重定向 - 强化学习训练 - 泛化测试”为主线，构建了从人体动作数据到机器人可执行策略的完整技术流程。

研究目标是让人形机器人在仿真环境中学习多类参考动作，并在不同动作类型、扰动条件和跨场景设置下保持较好的跟踪精度、稳定性和泛化能力。

This project focuses on humanoid robot motion skill learning and studies a reinforcement-learning-based whole-body motion tracking and generalization framework. The thesis follows the technical pipeline of expert data preprocessing, motion retargeting, reinforcement learning training, and generalization evaluation, and builds a complete workflow from human motion data to executable robot policies.

The main objective is to enable a humanoid robot to learn multiple reference motions in simulation while maintaining good tracking accuracy, stability, and generalization performance under different motion categories, disturbances, and cross-scene settings.

## 主要内容 Main Contents

1. 基于公开人体运动数据构建专家数据处理流程。
2. 完成人体模型到目标机器人的关键点映射、体型拟合与动作重定向。
3. 在 Isaac Gym / MuJoCo 仿真环境中搭建整身动作跟踪任务。
4. 采用 PPO 与非对称 Actor-Critic 结构训练控制策略。
5. 设计参考状态初始化、终止课程学习和安全正则项以提升训练稳定性。
6. 通过主实验、可视化分析以及鲁棒性与泛化实验验证方法有效性。

1. Construct an expert motion data processing pipeline based on public human motion datasets.
2. Complete keypoint mapping, body shape fitting, and motion retargeting from the human model to the target robot.
3. Build a whole-body motion tracking task in Isaac Gym / MuJoCo simulation environments.
4. Train the control policy with PPO and an asymmetric Actor-Critic architecture.
5. Design reference state initialization, termination curriculum learning, and safety regularization to improve training stability.
6. Validate the effectiveness of the method through main experiments, qualitative visualization, robustness tests, and generalization evaluation.

## 论文结构 Thesis Structure

- 第 1 章：绪论与研究背景
- 第 2 章：相关规范、系统背景与技术路线
- 第 3 章：专家数据处理与动作重定向
- 第 4 章：基于强化学习的动作跟踪方法设计
- 第 5 章：实验设计与结果分析
- 第 6 章：总结与展望

- Chapter 1: Introduction and Research Background
- Chapter 2: Related Specifications, System Background, and Technical Route
- Chapter 3: Expert Data Processing and Motion Retargeting
- Chapter 4: Reinforcement-Learning-Based Motion Tracking Method
- Chapter 5: Experimental Design and Result Analysis
- Chapter 6: Conclusion and Future Work

## Project Structure

- `examples/hitbook/chinese/thesis.tex`
  Main thesis entry file.
- `examples/hitbook/chinese/front/`
  Front matter such as cover page and abstracts.
- `examples/hitbook/chinese/body/`
  Main chapter files.
- `examples/hitbook/chinese/back/`
  Back matter including acknowledgements, publications, and appendix-related content.
- `examples/hitbook/chinese/reference.bib`
  Bibliography database.
- `examples/hitbook/chinese/hithesisbook.cls`
  Thesis class file and formatting rules used by the current project.

## Build Instructions

Compile the thesis in the following directory:

```bash
cd examples/hitbook/chinese
latexmk -xelatex -interaction=nonstopmode thesis.tex
```

After compilation, the output file is:

- `examples/hitbook/chinese/thesis.pdf`
