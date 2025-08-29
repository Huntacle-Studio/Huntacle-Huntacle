# Huntacle (猎杀时刻)

[![Unity Version](https://img.shields.io/badge/Unity-2022.3%2B-blueviolet.svg)](https://unity.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Steam-lightgrey.svg)]()

**Huntacle** (**猎杀时刻**) 是一款风格化、快节奏的**不对称竞技PvP游戏**。玩家在一场场30秒的极限回合中，在“追逐者”与“躲避者”的身份间不断切换，通过动态加点和地形策略智取对手，体验心跳加速的猎杀时刻。

> **中文 | [English](README_EN.md)** (WIP)

---

## ✨ 游戏特色

- **30秒极限攻防**: 极短的回合制对决，每秒钟都充满紧张与策略。
- **身份实时切换**: 每回合结束后，猎人与猎物的身份互换，带来丰富的策略变化。
- **动态属性系统**: 每回合分配属性点，自定义角色的**爆发力、体力、身长**等属性。属性间相互制约，决策至关重要！
- **可视化成长**: 属性加点会实时影响角色体型（肌肉膨胀、身高变化），策略选择一目了然。
- **策略性地形**: 地图中设有多种可交互元素（单杠、斜坡、掩体），利用地形是生存和追猎的关键。
- **精准操作手感**: 基于体力管理的操作体系，包含加速奔跑、滑铲、飞扑等动作，手感爽快且富有深度。

## 🎮 玩法概述

在一场比赛中，两名玩家将进行多轮对决。每轮开始时，系统会随机指定一名玩家为 **“追逐者”**，另一名为 **“躲避者”**。

- **追逐者** 的目标：在30秒内触碰到躲避者。
- **躲避者** 的目标：成功存活20秒或直至回合结束。

每回合结束后，双方身份互换，并根据胜负得分。率先获得**6分**并领先对手**至少2分**的玩家赢得最终胜利！

每回合开始前，玩家可以获得属性点，用于强化自身能力，塑造独一无二的追猎风格。

## 🛠️ 技术架构

本项目使用 **Unity 2022.3 LTS** 开发。

| 模块             | 技术选型                                                     |
| :--------------- | :----------------------------------------------------------- |
| **网络同步**     | **[Mirror Networking](https://mirror-networking.com/)** (P2P 房主主机模式) |
| **音频管理**     | **Unity AudioSource** (暂定)                                 |
| **输入管理**     | **Unity Input System**                                       |
| **Steam集成**    | **[Facepunch Steamworks](https://github.com/Facepunch/Facepunch.Steamworks)** 或 **Steamworks.NET** |
| **代码架构**     | 面向数据设计（DOD）与状态机（State Machine）结合             |

## 📁 项目结构

Huntacle/
├── Assets/
│ ├── Scripts/ # 主要游戏逻辑脚本
│ │ ├── Core/ # 游戏状态机、网络管理器、事件系统
│ │ ├── Characters/ # 角色控制器、状态、属性系统
│ │ ├── UI/ # 用户界面逻辑
│ │ └── Utilities/ # 通用工具类、扩展方法
│ ├── Art/ # 美术资源 (模型、纹理、动画)
│ ├── Audio/ # 音效与音乐资源
│ ├── Prefabs/ # 预制体
│ └── Scenes/ # 游戏场景
├── Packages/ # Unity包管理
├── ProjectSettings/ # Unity项目设置
└── README.md # 项目说明文件


## 🚀 如何开始（开发）

1.  **克隆项目**
    ```bash
    git clone https://github.com/your-username/Huntacle.git
    ```
2.  **使用Unity Hub打开项目**
    - 确保安装 **Unity 2022.3 LTS** 或更高版本。
3.  **导入必要包**
    - 项目打开后，Unity可能会自动导入在`Packages/manifest.json`中定义的包（如Mirror）。如果没有，请通过Package Manager手动安装。
4.  **打开主场景**
    - 在 `Assets/Scenes/` 目录下打开 `Main.unity` 或类似的主场景。
5.  **开始运行！**
    - 点击Unity编辑器的播放按钮，即可在本地运行游戏。

### 网络测试
要测试多人游戏，请：
1.  **构建并运行**：通过 `File -> Build and Run` 构建一个独立客户端。
2.  **在编辑器中运行**：保持编辑器运行作为主机（Host）。
3.  **连接**：在构建的客户端中输入 `localhost` 或本地IP地址进行连接。

## 🤝 如何贡献

我们欢迎任何形式的贡献！如果你有兴趣为Huntacle添砖加瓦，请遵循以下流程：

1.  Fork 本仓库。
2.  创建一个新的特性分支 (`git checkout -b feature/AmazingFeature`)。
3.  提交你的更改 (`git commit -m 'Add some AmazingFeature'`)。
4.  推送到分支 (`git push origin feature/AmazingFeature`)。
5.  打开一个 Pull Request。

请确保你的代码遵循项目的代码风格。

## 📄 许可证

本项目采用 **MIT 许可证** - 查看 [LICENSE](LICENSE) 文件了解详情。

## 👨‍💻 开发团队

**Huntacle** 由一支充满热情的三人独立游戏团队开发。

- **[成员A名]** - 程序 & 设计
- **[成员B名]** - 程序 & 策划
- **[成员C名]** - 美术 & 设计

## 📞 联系我们

- **GitHub Issues**: [提交Bug或功能建议](https://github.com/your-username/Huntacle/issues)
- **邮箱**: your-team-email@example.com
- **IndieDev 社区**: 我们也在 [某个游戏开发论坛] 活跃！

---

> **免责声明**: 本项目是粉丝创作作品。Huntacle是我们的项目名称，与任何现有公司或游戏无关。
