# CS146S 学习笔记与课程材料

这是我学习 Stanford University 课程 **CS146S: The Modern Software Developer** 时整理的个人仓库，主要保存课程资料、示例代码、中文注释和学习笔记。

- 课程官网：[themodernsoftware.dev](https://themodernsoftware.dev/)
- 学期：Stanford University, Fall 2026
- 仓库性质：非官方个人学习记录

## 当前内容

### 01 - The Internals of Coding Agents

第一讲通过一个约 200 行的 Python 示例展示 coding agent 的基本结构：模型读取对话上下文、请求调用工具、宿主程序执行本地操作，再将工具结果返回给模型。

- [课程幻灯片](01%20-%20The%20Internals%20of%20Coding%20Agents/slides/Lecture%209_22_26.pptx)
- [带中文注释的示例代码](01%20-%20The%20Internals%20of%20Coding%20Agents/code/coding_agent_from_scratch.py)
- [中文代码阅读笔记](01%20-%20The%20Internals%20of%20Coding%20Agents/coding_agent_from_scratch_notes.md)

代码阅读笔记解释了工具注册、文本工具调用协议、双层 agent 循环、消息流，以及该教学实现与生产级 coding agent 之间的差距。

## 目录结构

```text
.
├── README.md
└── 01 - The Internals of Coding Agents/
    ├── coding_agent_from_scratch_notes.md
    ├── code/
    │   └── coding_agent_from_scratch.py
    └── slides/
        └── Lecture 9_22_26.pptx
```

## 运行示例代码

示例需要 Python 3.12 或更新版本，并依赖 `openai` 和 `python-dotenv`：

```bash
python3 -m pip install openai python-dotenv
```

在本地 `.env` 中配置 API Key（该文件已被 `.gitignore` 排除）：

```dotenv
OPENAI_API_KEY=your_api_key_here
```

然后从仓库根目录运行：

```bash
python3 "01 - The Internals of Coding Agents/code/coding_agent_from_scratch.py"
```

源码中的模型名称需要与账户实际可用的模型保持一致。更多实现说明和安全注意事项见对应的[代码阅读笔记](01%20-%20The%20Internals%20of%20Coding%20Agents/coding_agent_from_scratch_notes.md)。

## 来源与版权说明

- 课程、幻灯片及课堂材料来自 [CS146S: The Modern Software Developer](https://themodernsoftware.dev/)。
- coding agent 示例基于课程讲师 Mihail Eric 发布的文章 [The Emperor Has No Clothes: How to Code Claude Code in 200 Lines of Code](https://www.mihaileric.com/The-Emperor-Has-No-Clothes/)。
- 原始课件、示例代码及课程材料的版权归课程方和各自作者所有。
- 中文注释和学习笔记是个人学习过程中的理解与整理，仅供学习参考；课程内容与要求应以课程方发布的信息为准。

由于仓库同时包含第三方课程材料，目前不附加覆盖整个仓库的统一开源许可证。
