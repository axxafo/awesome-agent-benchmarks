![Stars](https://img.shields.io/github/stars/dataanswer/awesome-agent-benchmarks?style=social)
![License](https://img.shields.io/github/license/dataanswer/awesome-agent-benchmarks)

CN [中文](README_zh.md) | EN [English](README.md)

# 🧠 awesome-agent-benchmarks

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

> **一站式发现全球最前沿的大模型 Agent 评测基准（Benchmark）**  
> 精选覆盖 **工具调用、多轮对话、代码生成、规划推理、真实世界任务** 等核心能力的数据集，助力研究者与开发者高效评估智能体性能。

---

## ✨ 为什么需要这个合集？

随着 LLM Agent 技术迅猛发展，评测基准（Benchmark）已成为衡量其真实能力的“标尺”。然而：
- 数据集散落在 GitHub、Hugging Face、论文附录中，**查找困难**
- 缺乏统一分类与关键指标对比，**难以横向评估**
- 新数据集层出不穷，**信息滞后严重**

**AgentBench Navigator 正是为解决这些问题而生** —— 我们为你**人工筛选、结构化整理、持续更新**全球高质量 Agent 评测数据集，省去你数小时的调研时间。

---

## 🔍 已收录代表性数据集

### 🔍 比如, GUI Agent

| 评测集 | 链接 | 发布时间 | 亮点 | 数据规模 | 指标 | 评估内容 | 平台 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| MiniWoB++ | https://github.com/Farama-Foundation/miniwob-plusplus | 2017 | 评估代理在基本网页交互（如点击、输入和表单导航）方面的能力。 | 100 web interaction tasks | 任务成功率 | Element Match | Web |
| RUSS | https://github.com/xnancy/russ | 2021 | 使用ThingTalk将自然语言映射到网页操作，实现真实HTML环境中的精确网页任务执行。 | 741 instructions | 任务成功率 | Text Match, Element Match | Web |
| WebShop | https://webshop-pnlp.github.io | 2022 | 使用真实产品模拟电子商务导航，挑战代理在指令理解、多页面导航和策略探索方面的能力。 | 12,087 instructions | 任务成功率, 步骤成功率* | Text Match | Web |
| Mind2Web | https://github.com/OSU-NLP-Group/Mind2Web | 2023 | 测试在跨领域的真实动态网站上的适应性。 | 2,000 tasks | 步骤成功率, 任务成功率 | Element Match, Action Match | Web |
| Mind2Web-Live | https://huggingface.co/datasets/iMeanAI/Mind2Web-Live | 2024 | 提供中间动作跟踪以进行真实任务评估，同时提供更新的Mind2Web-Live数据集和标注工具。 | 542 tasks | 步骤成功率, 任务成功率, 效率得分 | Element Match, Text Match, trajectory length | Web |
| Mind2Web-Live-Abstracted | https://anonymous.4open.science/r/navigate | 2024 | 通过省略Mind2Web-Live中的任务特定细节和用户输入信息来抽象描述，使其更加简洁且撰写耗时更少。 | 104 samples | 任务成功率, 效率得分 | Text Match, Image Match, Element Match, Path Length | Web |
| WebArena | https://webarena.dev | 2023 | 在Docker托管的网站上模拟真实的多标签浏览，专注于复杂的长期任务，模拟真实的在线交互。 | 812 long-horizon tasks | 步骤成功率 | Text Match | Web |
| VisualWebArena | https://jykh.com/vwa | 2024 | 评估多模态代理在视觉基础任务上的表现，要求在网页环境中具备视觉和文本交互能力。 | 910 tasks | 步骤成功率 | Text Match, Image Match | Web |
| MT-Mind2Web | https://github.com/magicgh/self-map | 2024 | 引入带有多轮交互的会话式网页导航，由专门的多轮网页数据集支持。 | 720 sessions / 3525 instructions | 步骤成功率, 轮次成功率 | Element Match, Action Match | Web |
| MMInA | https://mmina.cliangyu.com | 2024 | 在真实网站上测试多跳、多模态任务，要求代理处理跨页面信息提取和复杂任务的推理。 | 1,050 tasks | 步骤成功率, 任务成功率 | Text Match, Element Match | Web |
| AutoWebBench | https://github.com/THUDM/AutoWebGLM | 2024 | 包含10,000条浏览轨迹的双语网页浏览基准，支持跨语言特定环境的评估。 | 10,000 traces | 步骤成功率, 效率得分 | Element Match, Action Match, Time | Web |
| WorkArena | https://github.com/ServiceNow/WorkArena | 2024 | 专注于真实企业软件交互，针对知识工作者经常执行的任务。 | 19,912 unique task instances | 任务成功率, 效率得分, 策略下完成度, 轮次成功率 | Element Match, Text Match, Execution-based Validation | Web |
| VideoWebArena | https://github.com/liang0/videowebarena | 2024 | 专注于使用视频教程完成任务的长上下文多模态代理。 | 74 videos (~4 hours), 2,021 tasks | 任务成功率, 中间意图成功率, 效率得分s | Element Match, State Information, Exact and Fuzzy Text Matches | Web |
| EnvDistraction | https://github.com/xbmxb/EnvDistraction | 2024 | 通过评估多模态GUI代理对环境干扰（如弹窗、虚假搜索结果或误导性推荐）的敏感性来评估其'忠实度'。 | 1,198 tasks | 任务成功率 | Text Match, Element Match, State Information | Web |
| WebVLN-v1 | https://github.com/WebVLN/WebVLN | 2024 | 结合购物网站上的导航和问答，整合视觉和文本内容进行统一的网页交互评估。 | 8,990 paths and 14,825 QA pairs | 任务成功率, 效率得分 | Element Match, Path Length, Trajectory Length | Web |
| WEBLINX | https://mcgill-nlp.github.io/weblinx | 2024 | 专注于会话导航，要求代理在真实的对话式网页任务中遵循多轮用户指令。 | 100k interactions | 轮次成功率 | Text Match, Action Match | Web |
| ST-WebAgentBench | https://sites.google.com/view/st-webagentbench/home | 2024 | 评估网页代理中的策略驱动安全，使用策略下完成度指标确保在企业类环境中的合规性。 | 235 tasks | 任务成功率, 策略下完成度 (CuP), 风险比率 | Element Match, Action Match, Text Match | Web |
| CompWoB | https://github.com/google-research/google-research/tree/master/compositional_rl/compwob | 2023 | 测试代理在需要跨多个步骤进行状态管理的顺序组合任务上的表现，模拟真实世界的自动化场景。 | 50 compositional tasks | 任务成功率 | Element Match | Web |
| TURKING BENCH | https://turkingbench.github.io | 2024 | 使用来自众包的自然HTML任务评估与真实网页布局和元素的交互技能。 | 32.2K instances | 任务成功率 | Text Match, Element Match, Image Match | Web |
| VisualWebBench | https://visualwebbench.github.io | 2024 | 提供对多模态大型语言模型（MLLMs）在网页特定任务上的细粒度评估。 | 1,534 instances from 139 real websites across 87 sub-domains | 任务成功率, 轮次成功率, 效率得分, Metrics | Text Match, Image Match, Element Match, Action Match | Web |
| WONDERBREAD | https://github.com/HazyResearch/wonderbread | 2024 | 专注于业务流程管理（BPM）任务，如文档编制、知识转移和流程改进。 | 2,928 human demonstrations across 598 distinct workflows | 任务成功率, 步骤成功率, 效率得分, 策略下完成度 | Text Match, Action Match, State Information | Web |
| WebOlympus | / | 2024 | 一个为网页代理提供的开放平台，简化了在实时网站上运行演示、评估和数据收集的过程。 | 50 tasks | 任务成功率, 步骤成功率 | Action Match | Web |
| AndroidEnv | https://github.com/google-deepmind/android_env | 2021 | 提供基于Android生态系统的开源平台，包含约30个应用程序的100多个任务，专注于各种Android交互的强化学习。 | 100+ tasks | 不适用 | NA | Android |
| PIXELHELP | https://github.com/google-research/google-research/tree/master/seq2act | 2020 | 包含自然语言指令语料库，与四个任务类别中的UI操作配对，有助于将语言与UI交互联系起来。 | 187 multi-step instructions | 步骤成功率 | Element Match, Action Match | Android |
| Mobile-Env | https://github.com/X-LANCE/Mobile-Env | 2024 | 用于Android GUI基准测试的综合工具包，可对真实应用程序交互进行受控评估。 | 224 tasks | 任务成功率, 步骤成功率 | Text Match, Element Match, Image Match, State Information | Android |
| B-MOCA | https://b-moca.github.io | 2024 | 在真实任务上基准测试移动设备控制代理，结合UI布局和语言随机化来评估泛化能力。 | 131 tasks | 任务成功率 | Element Match, State Information | Android |
| AndroidWorld | https://github.com/google-research/android_world | 2024 | 提供动态Android环境，允许进行多样化的自然语言指令测试。 | 116 tasks | 任务成功率 | State Information | Android |
| Mobile-Eval | https://github.com/X-PLUG/MobileAgent | 2024 | 基于主流Android应用的基准，旨在测试常见的移动交互。 | 30 instructions | 任务成功率, 步骤成功率, 效率得分 | Text Match, Path Length | Android |
| DroidTask | https://github.com/MobileLLM/AutoDroid | 2024 | Android任务自动化基准支持在真实应用中进行探索和任务记录，并带有相应的GUI动作轨迹。 | 158 tasks | 步骤成功率, 任务成功率 | Element Match, Action Match | Android |
| AITW | https://github.com/google-research/google-research/tree/master/android_in_the_wild | 2023 | 一个大规模数据集，部分灵感来自PIXELHELP，涵盖各种Android交互。 | 715,142 episodes | 任务成功率, 步骤成功率 | Action Match | Android |
| AndroidArena | https://github.com/AndroidArenaAgent/AndroidArena | 2024 | 专注于Android生态系统中的日常跨应用和受限任务，提供单应用和多应用交互场景。 | 221 tasks | 任务成功率, 步骤成功率, 效率得分 | Action Match, Path Length | Android |
| ANDROIDLAB | https://github.com/THUDM/Android-Lab | 2024 | 提供结构化评估框架，包含9个应用程序的138个任务，支持Android上的纯文本和多模态代理评估。 | 138 tasks | 任务成功率, 步骤成功率, 效率得分 | Element Match, Image Match | Android |
| LlamaTouch | https://github.com/LlamaTouch/LlamaTouch | 2024 | 通过将任务执行轨迹与注释的基本状态进行匹配，实现对移动UI任务自动化的忠实且可扩展的评估。 | 496 tasks covering 57 unique Android applications | 任务成功率, 步骤成功率, 效率得分 | Text Match, Action Match, State Information, Android Application Match | Mobile Android |
| MobileAgentBench | https://mobileagentbench.github.io | 2024 | 在真实Android设备上提供完全自主的评估过程，并在判断多路径完成的成功条件方面具有灵活性。 | 100 tasks across 10 open-source Android applications | 任务成功率, 效率得分, Latency, Token Cost | State Information (UI State Matching) | Mobile Android |
| Mobile-Bench | https://github.com/XiaoMi/MobileBench | 2024 | 在多应用场景中支持UI和基于API的操作，使用基于检查点的评估方法测试代理在单任务和多任务结构上的表现。 | 832 entries (200+ tasks) | 任务成功率, 步骤成功率, 效率得分 | Action Match, Path Length | Android |
| Mobile Safety Bench | https://mobilesafetybench.github.io | 2024 | 优先考虑移动控制任务中的安全评估，具有专注于有用性、隐私和法律合规性的不同任务。 | 100 tasks | 任务成功率, Mitigation Risk Success | Action Match with Safety Considered, Element Match, State Information | Android |
| SPA-BENCH | https://spa-bench.github.io | 2024 | 广泛的评估框架，支持英语和中文的单应用和跨应用任务，为各种任务场景提供即插即用结构。 | 340 tasks | 任务成功率, 步骤成功率, 效率得分 | Action Match, State Information, Time Spent, API Cost | Android |
| VisualAgent Bench | https://github.com/THUDM/VisualAgentBench | 2024 | 第一个为跨GUI和多模态任务的视觉基础代理设计的基准，专注于Android、网页和游戏环境中的视觉中心交互。 | 4,482 trajectories | 任务成功率 | Text Match | Web, Android, Game, Virtual Embodied |
| OSWorld | https://os-world.github.io | 2024 | 为多模态代理提供可扩展的真实计算机环境，支持跨Ubuntu、Windows和macOS的任务设置、基于执行的评估和交互式学习。 | 369 Ubuntu tasks, 43 Windows tasks | 任务成功率 | Execution-based State Information (such as internal file interpretation, permission management) | Linux, Windows, macOS, Web |
| Windows Agent Arena | https://microsoft.github.io/WindowsAgentArena | 2024 | OSWorld的改编版，专注于Windows操作系统，包含多样化的多步骤任务，使代理能够使用广泛的应用程序和工具。 | 154 tasks | 任务成功率 | Same as OSWorld, with cloud parallelization | Windows |
| OmniACT | https://huggingface.co/datasets/Writer/omniact | 2024 | 评估代理在各种操作系统环境中为桌面和网页应用程序生成可执行程序的能力，优先考虑多模态挑战。 | 9,802 data points | 任务成功率, 步骤成功率 | Action Match | MacOS, Linux, Windows, Web |
| VideoGUI | https://showlab.github.io/videogui | 2024 | 专注于教学视频中的视觉中心任务，强调在Adobe Photoshop和Premiere Pro等应用中的动作规划和精确度。 | 178 tasks, 463 subtasks | 任务成功率 | State Information, Action Match | Windows, Web |
| Spider2-V | https://spider2-v.github.io | 2024 | 在真实的企业软件环境中对数据科学和工程工作流程中的代理进行基准测试，涵盖从数据摄取到可视化的任务。 | 494 tasks | 任务成功率 | Action Match, State Information | Linux |
| Act2Cap | https://showlab.github.io/GUI-Narrator | 2024 | 强调使用视频格式的基于光标的提示进行GUI光标叙述，涵盖各种GUI交互，如点击、输入和拖动。 | 4,189 samples | 步骤成功率 | Element Match | Windows |
| OFFICEBENCH | https://github.com/zlwang-cs/OfficeBench | 2024 | 在Word和Excel等应用程序的复杂多步骤任务中测试办公工作流中的跨应用程序自动化，评估真实场景中的操作集成。 | 300 tasks | 任务成功率 | Action match, Text Match, State Information | Linux |
| AssistGUI | https://showlab.github.io/assistgui | 2024 | 第一个专注于面向任务的桌面GUI自动化的基准。 | 100 tasks from 9 popular applications | 任务成功率, 效率得分 | Element Match, Action Match | Windows Platform |
| SPR Benchmark | / | 2024 | 评估GUI屏幕阅读器描述内容和布局信息的能力。 | Includes 650 screenshots annotated with 1,500 target points and regions | 任务成功率, 效率得分 | Text Match, Element Match | Mobile, Web, and Operating Systems |
| AgentStudio | https://computer-agents.github.io/agent-studio | 2024 | 用于创建和基准测试通用虚拟代理的开放工具包，支持跨各种软件应用程序的复杂交互。 | NA | 步骤成功率 | Action Match, State Information and Image Match | Windows, Linux, macOS |
| CRAB | https://github.com/crab-benchmark | 2024 | 跨环境基准，评估移动和桌面设备上的代理，使用基于图形的评估方法处理多条正确路径和任务灵活性。 | 120 tasks | 步骤成功率, 效率得分 | Action Match | Linux, Android |
| ScreenSpot | https://github.com/niucckevin/SeeClick | 2024 | 带有预训练GUI基础的基于视觉的GUI基准，评估代理仅使用截图与移动、桌面和网页平台上的GUI元素交互的能力。 | 1,200 instructions | 步骤成功率 | Action Match | iOS, Android, macOS, Windows, Web |

......<br>


> 💡 **为了方便大家查找，我们提供了一个完整列表在线访问 → [agentbench-navigator](https://www.dataanswer.top/)**

![输入图片说明](1352c909dc64782718978692a2dd6dd0.png)

![输入图片说明](288337624c96a46638a3429855f79c31.png)

---


## 🤝 如何贡献？

我们欢迎任何形式的贡献！你的参与能让这个awesome-agent-benchmarks更强大：

- **新增数据集**：发现未收录的优质 Agent Benchmark？提交 Issue 或 PR！
- **修正信息**：链接失效？描述有误？欢迎修复。

---

## 📄 许可证

本项目的网站代码采用 MIT License —— 自由使用、修改、分发。

本项目的数据集元信息内容（如描述、分类、链接）采用 CC BY 4.0 许可：

- ✅ 允许商业与非商业使用
- ✅ 允许修改与再分发
- ⚠️ 必须注明原作者及来源链接

© 2025 XuChao. 保留部分权利。

---

## 🙏 致谢

- 感谢所有开源 Agent Benchmark 的研究团队与维护者
- 灵感来源于 Awesome Lists 系列项目
- 特别鸣谢早期测试用户提供的宝贵反馈

---

## 📬 联系我们

如果你有任何问题、合作建议或想交流 Agent 评测心得，欢迎通过以下方式联系：

- Github: [@dataanswer](https://github.com/dataanswer)
- 邮箱: [dataanswer@163.com](dataanswer@163.com)

> 让每一次 Agent 能力评估，都有据可依。

---

> 本项目由 **DataAnswer XuChao** 维护，始于 2025 年。
