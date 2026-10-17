---
layout: post
title: "多AI工具的skills同步"
date: 2026-09-04 00:00:00 +0800
tags: [AI]
description: "如果同时在用Codex、Workbody、Claude Code，如何实现 skills 同步的无缝体验？"
lang: zh-CN
---

如果同时在用Codex、Workbody、Claude Code，如何实现 skills 同步的无缝体验？

社区的朋友提到自己几套工具来回切，部分工具都要重新装一遍 skills，很麻烦。

就算一次性弄好了，但skills还会持续增减更新，怎么才能让几套 agent 共用同一套skills 呢？

我的经验是用软链接的方案比较合适，我也已经按此执行了将近一年，效果很好。

操作就三步。先在各个 agent 的系统目录之外，新建一个文件夹放skills。再把每个 agent 约定的 skills 目录，用软链接指到这个独立文件夹。以后所有 skills 只放这一个地方，改一次，几套 agent 读到同一个状态。

其中有个概念软链接，它就像电脑里的快捷方式，没有文件本体，只是个指针，告诉程序该去哪里找。

在我们的方案里，agent 调 skill 时先读到软链接，软链接再指回那个独立文件夹。

这个过程也不需要你操作，你把这个方案告诉 Agent，让他去执行就好。

所以入口看着是好几套目录，背后访问的其实是同一批文件。

最初发表于公众号「阿Ken聊AI商业」，2026-09-04。
