---
title: 为什么选择Cherry Studio
date: 2026-06-20
authors:
  - BaihowFF
tags:
  - AI
  - Cherry Studio
  - 智能体
  - 工具选择
---

# 为什么选择 Cherry Studio

大概今年春节前后，开始尝试使用智能体，从此 token 消耗量开始一路狂飙。

最初，我使用 Cherry Studio 只是当做能接入各种 LLM 模型的入口，方便聊天。能从硅基流动访问 GLM、Kimi、DeepSeek 这些模型，也能通过 DMXAPI 或者之前的 DeerAPI 访问 Claude 和 GPT，统一聊天入口而已。

而今年春节前后开始的小龙虾、Hermes 这些智能体的出现，我曾经也装过 OpenClaw、CodeX、OpenCode、AtomCode 这样一些智能体工具，最终还是选择了 Cherry Studio 这个看似冷门的工具。

首先，Cherry Studio 本来只是当做聊天助手，在 25 年选择入口工具的时候击败了 ChatBox 等工具，变成了我的常用 AI 入口。确实有一部分原因是因为使用惯性吧。

其次，Cherry Studio 的智能体实质上就是 Claude Code，这得益于今年 4 月 1 日那次 Claude Code 源码泄露事件。从那后大概半个月，国内的各种 xxxxCode 软件都突然变的好用了。所以从智能体本身来说，其实各种 xxxxCode 之间并没有本质差别。要各种技能，基本上 Cherry Studio 也都能装。

第三，Cherry Studio 确实是最方便配置不同渠道 API 的。我常用的模型有 GLM、DeepSeek、Kimi、Opus，提供商也有 4、5 家，Cherry Studio 在配置上最方便。

目前最为欠缺的能力是 Agent 调用 Agent 的能力。我知道在一个智能体里做出自动创建子智能体是一个方法，但各个智能体实际上是需要演进的，不是一成不变的。子智能体的演进并不方便，有时候上下文超了，还会覆盖掉不同的 md 文件段落，这就很蛋疼。希望未来什么时候 Cherry Studio 能支持各智能体之间调用吧，那样就会突然灵活起来。

目前，在 Cherry Studio 里，我常用的助手对话是 10 个，常用的智能体是 20 个，我的智能体都是拆开的。为不同的智能体配备了不同能力的 LLM。有的智能体在开发的时候会用 GLM 5.2 或者 DeepSeek pro 版本，在 python 和流程固定后，就改用 DeepSeek flash 重复执行了。

另外，我手动建立了本地 svn，并且不准智能体操作 svn，只允许操作 git。这样智能体用 git 做版本管理，我手动 svn 兜底。

好了，大概就是这样。
