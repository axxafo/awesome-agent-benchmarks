![Stars](https://img.shields.io/github/stars/dataanswer/awesome-agent-benchmarks?style=social)
![License](https://img.shields.io/github/license/dataanswer/awesome-agent-benchmarks)

CN [中文](README_zh.md) | EN [English](README.md)

# 🧠 Awesome Agent Benchmarks

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

A curated collection of the world’s most advanced benchmark datasets for evaluating Large Language Model (LLM) Agents. Covers core capabilities including **tool use**, **multi-turn dialogue**, **code generation**, **planning & reasoning**, and **real-world task execution**—empowering researchers and developers to efficiently assess agent performance.

---

## ✨ Why This Collection?

As LLM Agent technology advances rapidly, standardized benchmarks have become the essential “ruler” for measuring real-world capabilities. However:

- Datasets are scattered across GitHub, Hugging Face, and paper appendices—hard to discover  
- Lack of unified taxonomy and key metric comparisons makes cross-evaluation difficult  
- New benchmarks emerge constantly, leading to outdated or incomplete lists  

**AgentBench Navigator** solves these problems by offering:
- Manually vetted, high-quality agent evaluation datasets  
- Structured categorization and metadata  
- Continuous updates to keep pace with the latest research  

Save hours of research time—get straight to what matters.

---

## 🔍 Datasets
 
> 💡 Explore the full list online → [AgentBench Navigator](https://www.dataanswer.top/)

### 🔍 GUI Agent

| Benchmark | Link | Year | Highlight | Data Size | Metric | Measurement | Platform |
| --- | --- | --- | --- | --- | --- | --- | --- |
| MiniWoB++ | https://github.com/Farama-Foundation/miniwob-plusplus | 2017 | Evaluates agents on basic web interactions like clicking, typing, and form navigation. | 100 web interaction tasks | Task Success Rate | Element Match | Web |
| RUSS | https://github.com/xnancy/russ | 2021 | Uses ThingTalk for mapping natural language to web actions, enabling precise web-based task execution in real HTML environments. | 741 instructions | Task Success Rate | Text Match, Element Match | Web |
| WebShop | https://webshop-pnlp.github.io | 2022 | Simulates e-commerce navigation with real-world products, challenging agents with instruction comprehension, multi-page navigation, and strategic exploration. | 12,087 instructions | Task Success Rate, Step Success Rate* | Text Match | Web |
| Mind2Web | https://github.com/OSU-NLP-Group/Mind2Web | 2023 | Tests adaptability on real-world, dynamic websites across domains. | 2,000 tasks | Step Success Rate, Task Success Rate | Element Match, Action Match | Web |
| Mind2Web-Live | https://huggingface.co/datasets/iMeanAI/Mind2Web-Live | 2024 | Provides intermediate action tracking for realistic task assessment, along with an updated Mind2Web-Live dataset and tools for annotation. | 542 tasks | Step Success Rate, Task Success Rate, Efficiency Score | Element Match, Text Match, trajectory length | Web |
| Mind2Web-Live-Abstracted | https://anonymous.4open.science/r/navigate | 2024 | Abstracts the descriptions by omitting task-specific details and user input information in Mind2Web-Live, which are more streamlined and less time-consuming to compose. | 104 samples | Task Success Rate, Efficiency Score | Text Match, Image Match, Element Match, Path Length | Web |
| WebArena | https://webarena.dev | 2023 | Simulates realistic, multi-tab browsing on Docker-hosted websites, focusing on complex, long-horizon tasks that mirror real online interactions. | 812 long-horizon tasks | Step Success Rate | Text Match | Web |
| VisualWebArena | https://jykh.com/vwa | 2024 | Assesses multimodal agents on visually grounded tasks, requiring both visual and textual interaction capabilities in web environments. | 910 tasks | Step Success Rate | Text Match, Image Match | Web |
| MT-Mind2Web | https://github.com/magicgh/self-map | 2024 | Introduces conversational web navigation with multi-turn interactions, supported by a specialized multi-turn web dataset. | 720 sessions / 3525 instructions | Step Success Rate, Turn Success Rate | Element Match, Action Match | Web |
| MMInA | https://mmina.cliangyu.com | 2024 | Tests multihop, multimodal tasks on real-world websites, requiring agents to handle cross-page information extraction and reasoning for complex tasks. | 1,050 tasks | Step Success Rate, Task Success Rate | Text Match, Element Match | Web |
| AutoWebBench | https://github.com/THUDM/AutoWebGLM | 2024 | Bilingual web browsing benchmark with 10,000 browsing traces, supporting evaluation across language-specific environments. | 10,000 traces | Step Success Rate, Efficiency Score | Element Match, Action Match, Time | Web |
| WorkArena | https://github.com/ServiceNow/WorkArena | 2024 | Focuses on real-world enterprise software interactions, targeting tasks frequently performed by knowledge workers. | 19,912 unique task instances | Task Success Rate, Efficiency Score, Completion under Policy, Turn Success Rate | Element Match, Text Match, Execution-based Validation | Web |
| VideoWebArena | https://github.com/liang0/videowebarena | 2024 | Focuses on long-context multimodal agents using video tutorials for task completion. | 74 videos (~4 hours), 2,021 tasks | Task Success Rate, Intermediate Intent Success Rate, Efficiency Scores | Element Match, State Information, Exact and Fuzzy Text Matches | Web |
| EnvDistraction | https://github.com/xbmxb/EnvDistraction | 2024 | Evaluates the "faithfulness" of multimodal GUI agents by assessing their susceptibility to environmental distractions, such as pop-ups, fake search results, or misleading recommendations. | 1,198 tasks | Task Success Rate | Text Match, Element Match, State Information | Web |
| WebVLN-v1 | https://github.com/WebVLN/WebVLN | 2024 | Combines navigation and question-answering on shopping sites, integrating visual and textual content for unified web interaction evaluation. | 8,990 paths and 14,825 QA pairs | Task Success Rate, Efficiency Score | Element Match, Path Length, Trajectory Length | Web |
| WEBLINX | https://mcgill-nlp.github.io/weblinx | 2024 | Focuses on conversational navigation, requiring agents to follow multi-turn user instructions in realistic, dialogue-based web tasks. | 100k interactions | Turn Success Rate | Text Match, Action Match | Web |
| ST-WebAgentBench | https://sites.google.com/view/st-webagentbench/home | 2024 | Evaluates policy-driven safety in web agents, using the Completion under Policy metric to ensure compliance in enterprise-like environments. | 235 tasks | Task Success Rate, Completion under Policy (CuP), Risk Ratio | Element Match, Action Match, Text Match | Web |
| CompWoB | https://github.com/google-research/google-research/tree/master/compositional_rl/compwob | 2023 | Tests agents on sequential, compositional tasks that require state management across multiple steps, simulating real-world automation scenarios. | 50 compositional tasks | Task Success Rate | Element Match | Web |
| TURKING BENCH | https://turkingbench.github.io | 2024 | Uses natural HTML tasks from crowdsourcing to assess interaction skills with real-world web layouts and elements. | 32.2K instances | Task Success Rate | Text Match, Element Match, Image Match | Web |
| VisualWebBench | https://visualwebbench.github.io | 2024 | Provides a fine-grained assessment of multimodal large language models (MLLMs) on web-specific tasks. | 1,534 instances from 139 real websites across 87 sub-domains | Task Success Rate, Turn Success Rate, Efficiency Score, Metrics | Text Match, Image Match, Element Match, Action Match | Web |
| WONDERBREAD | https://github.com/HazyResearch/wonderbread | 2024 | Focuses on business process management (BPM) tasks like documentation, knowledge transfer, and process improvement. | 2,928 human demonstrations across 598 distinct workflows | Task Success Rate, Step Success Rate, Efficiency Score, Completion under Policy | Text Match, Action Match, State Information | Web |
| WebOlympus | / | 2024 | An open platform for web agents that simplifies running demos, evaluations, and data collection for web agents on live websites. | 50 tasks | Task Success Rate, Step Success Rate | Action Match | Web |
| AndroidEnv | https://github.com/google-deepmind/android_env | 2021 | Provides an open-source platform based on the Android ecosystem with over 100 tasks across approximately 30 apps, focusing on reinforcement learning for various Android interactions. | 100+ tasks | NA | NA | Android |
| PIXELHELP | https://github.com/google-research/google-research/tree/master/seq2act | 2020 | Includes a corpus of natural language instructions paired with UI actions across four task categories, aiding in grounding language to UI interactions. | 187 multi-step instructions | Step Success Rate | Element Match, Action Match | Android |
| Mobile-Env | https://github.com/X-LANCE/Mobile-Env | 2024 | Comprehensive toolkit for Android GUI benchmarks to enable controlled evaluation of real-world app interactions. | 224 tasks | Task Success Rate, Step Success Rate | Text Match, Element Match, Image Match, State Information | Android |
| B-MOCA | https://b-moca.github.io | 2024 | Benchmarks mobile device control agents on realistic tasks, incorporating UI layout and language randomization to evaluate generalization capabilities. | 131 tasks | Task Success Rate | Element Match, State Information | Android |
| AndroidWorld | https://github.com/google-research/android_world | 2024 | Offers a dynamic Android environment, allowing for diverse natural language instruction testing. | 116 tasks | Task Success Rate | State Information | Android |
| Mobile-Eval | https://github.com/X-PLUG/MobileAgent | 2024 | Benchmark based on mainstream Android apps, designed to test common mobile interactions. | 30 instructions | Task Success Rate, Step Success Rate, Efficiency Score | Text Match, Path Length | Android |
| DroidTask | https://github.com/MobileLLM/AutoDroid | 2024 | Android Task Automation benchmark supports exploration and task recording in real apps with corresponding GUI action traces. | 158 tasks | Step Success Rate, Task Success Rate | Element Match, Action Match | Android |
| AITW | https://github.com/google-research/google-research/tree/master/android_in_the_wild | 2023 | A large-scale dataset partly inspired by PIXELHELP, covering diverse Android interactions. | 715,142 episodes | Task Success Rate, Step Success Rate | Action Match | Android |
| AndroidArena | https://github.com/AndroidArenaAgent/AndroidArena | 2024 | Focuses on daily cross-app and constrained tasks within the Android ecosystem, providing single-app and multi-app interaction scenarios. | 221 tasks | Task Success Rate, Step Success Rate, Efficiency Score | Action Match, Path Length | Android |
| ANDROIDLAB | https://github.com/THUDM/Android-Lab | 2024 | Provides a structured evaluation framework with 138 tasks across nine apps, supporting both text-only and multimodal agent evaluations on Android. | 138 tasks | Task Success Rate, Step Success Rate, Efficiency Score | Element Match, Image Match | Android |
| LlamaTouch | https://github.com/LlamaTouch/LlamaTouch | 2024 | Enables faithful and scalable evaluations for mobile UI task automation by matching task execution traces against annotated essential states. | 496 tasks covering 57 unique Android applications | Task Success Rate, Step Success Rate, Efficiency Score | Text Match, Action Match, State Information, Android Application Match | Mobile Android |
| MobileAgentBench | https://mobileagentbench.github.io | 2024 | Provides a fully autonomous evaluation process on real Android devices and flexibility in judging success conditions across multiple paths to completion. | 100 tasks across 10 open-source Android applications | Task Success Rate, Efficiency Score, Latency, Token Cost | State Information (UI State Matching) | Mobile Android |
| Mobile-Bench | https://github.com/XiaoMi/MobileBench | 2024 | Supports both UI and API-based actions in multi-app scenarios, testing agents on single and multi-task structures with a checkpoint-based evaluation approach. | 832 entries (200+ tasks) | Task Success Rate, Step Success Rate, Efficiency Score | Action Match, Path Length | Android |
| Mobile Safety Bench | https://mobilesafetybench.github.io | 2024 | Prioritizes safety evaluation in mobile control tasks, with distinct tasks focused on helpfulness, privacy, and legal compliance. | 100 tasks | Task Success Rate, Mitigation Risk Success | Action Match with Safety Considered, Element Match, State Information | Android |
| SPA-BENCH | https://spa-bench.github.io | 2024 | Extensive evaluation framework supporting single-app and cross-app tasks in English and Chinese, providing a plug-and-play structure for diverse task scenarios. | 340 tasks | Task Success Rate, Step Success Rate, Efficiency Score | Action Match, State Information, Time Spent, API Cost | Android |
| VisualAgent Bench | https://github.com/THUDM/VisualAgentBench | 2024 | First benchmark designed for visual foundation agents across GUI and multimodal tasks, focusing on vision-centric interactions in Android, web, and game environments. | 4,482 trajectories | Task Success Rate | Text Match | Web, Android, Game, Virtual Embodied |
| OSWorld | https://os-world.github.io | 2024 | Scalable, real computer environment for multimodal agents, supporting task setup, execution-based evaluation, and interactive learning across Ubuntu, Windows, and macOS. | 369 Ubuntu tasks, 43 Windows tasks | Task Success Rate | Execution-based State Information (such as internal file interpretation, permission management) | Linux, Windows, macOS, Web |
| Windows Agent Arena | https://microsoft.github.io/WindowsAgentArena | 2024 | Adaptation of OSWorld focusing exclusively on the Windows OS with diverse multi-step tasks, enabling agents to use a wide range of applications and tools. | 154 tasks | Task Success Rate | Same as OSWorld, with cloud parallelization | Windows |
| OmniACT | https://huggingface.co/datasets/Writer/omniact | 2024 | Assesses agents' capability to generate executable programs for computer tasks across desktop and web applications in various OS environments, prioritizing multimodal challenges. | 9,802 data points | Task Success Rate, Step Success Rate | Action Match | MacOS, Linux, Windows, Web |
| VideoGUI | https://showlab.github.io/videogui | 2024 | Focuses on vision-centric tasks from instructional videos, emphasizing action planning and precision in applications like Adobe Photoshop and Premiere Pro. | 178 tasks, 463 subtasks | Task Success Rate | State Information, Action Match | Windows, Web |
| Spider2-V | https://spider2-v.github.io | 2024 | Benchmarks agents across data science and engineering workflows in authentic enterprise software environments, covering tasks from data ingestion to visualization. | 494 tasks | Task Success Rate | Action Match, State Information | Linux |
| Act2Cap | https://showlab.github.io/GUI-Narrator | 2024 | Emphasizes GUI cursor narration using cursor-based prompts in video format, covering a variety of GUI interactions like clicks, typing, and dragging. | 4,189 samples | Step Success Rate | Element Match | Windows |
| OFFICEBENCH | https://github.com/zlwang-cs/OfficeBench | 2024 | Tests cross-application automation in office workflows with complex multi-step tasks across applications like Word and Excel, assessing operational integration in realistic scenarios. | 300 tasks | Task Success Rate | Action match, Text Match, State Information | Linux |
| AssistGUI | https://showlab.github.io/assistgui | 2024 | The first benchmark focused on task-oriented desktop GUI automation. | 100 tasks from 9 popular applications | Task Success Rate, Efficiency Score | Element Match, Action Match | Windows Platform |
| SPR Benchmark | / | 2024 | Evaluates GUI screen readers' ability to describe both content and layout information. | Includes 650 screenshots annotated with 1,500 target points and regions | Task Success Rate, Efficiency Score | Text Match, Element Match | Mobile, Web, and Operating Systems |
| AgentStudio | https://computer-agents.github.io/agent-studio | 2024 | Open toolkit for creating and benchmarking general-purpose virtual agents, supporting complex interactions across diverse software applications. | NA | Step Success Rate | Action Match, State Information and Image Match | Windows, Linux, macOS |
| CRAB | https://github.com/crab-benchmark | 2024 | Cross-environment benchmark evaluating agents across mobile and desktop devices, using a graph-based evaluation method to handle multiple correct paths and task flexibility. | 120 tasks | Step Success Rate, Efficiency Score | Action Match | Linux, Android |
| ScreenSpot | https://github.com/niucckevin/SeeClick | 2024 | Vision-based GUI benchmark with pre-trained GUI grounding, assessing agents' ability to interact with GUI elements across mobile, desktop, and web platforms using only screenshots. | 1,200 instructions | Step Success Rate | Action Match | iOS, Android, macOS, Windows, Web |

..............<br>

## 🤝 How to Contribute

We welcome all forms of contributions! Help make this list even better:

- **Add a new dataset**: Found a high-quality Agent benchmark not listed? Open an Issue or PR!
- **Fix inaccuracies**: Broken links? Outdated descriptions? Please correct them.
- **Improve metadata**: Add missing fields like task count, domain, or evaluation metrics.

Your contribution will help the entire AI agent community!

---

## 📄 License

- **Website code**: MIT License — free to use, modify, and distribute.  
- **Dataset metadata** (descriptions, categories, links): [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)  
  ✅ Commercial & non-commercial use allowed  
  ✅ Modification and redistribution allowed  
  ⚠️ **Attribution required**: Please credit the original author and link back to this repository.

© 2025 XuChao. Some rights reserved.

---

## 🙏 Acknowledgements

- Thanks to all open-source Agent benchmark teams and maintainers  
- Inspired by the [Awesome Lists](https://github.com/sindresorhus/awesome) series  
- Special thanks to early beta users for valuable feedback

---

## 📬 Contact

Have questions, collaboration ideas, or want to discuss agent evaluation? Reach out via:

- GitHub: [@dataanswer](https://github.com/dataanswer)  
- Email: [dataanswer@163.com](mailto:dataanswer@163.com)

> Let every agent capability evaluation be evidence-based.

Maintained by **DataAnswer (XuChao)** since 2025.
