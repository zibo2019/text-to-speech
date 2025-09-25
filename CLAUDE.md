# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个文本朗读工具(Text-to-Speech)项目，是一个纯前端的单页面Web应用。该工具能够将输入的文本转换为语音，并支持Markdown格式的智能清理。

## 技术架构

### 核心技术栈
- **前端**：纯 HTML + Vanilla JavaScript
- **样式**：Tailwind CSS (通过CDN引入)
- **图标**：Font Awesome (通过CDN引入)
- **语音合成**：浏览器原生 Speech Synthesis API
- **部署**：单文件应用，可直接在浏览器中打开

### 项目结构
```
text-to-speech/
├── index.html           # 主应用文件（包含HTML、CSS、JS）
├── system-prompt.md     # AI系统提示词和开发规范
├── 博客文章.md          # 项目介绍和特性说明文档
└── .claude/             # Claude Code配置目录
```

## 开发指南

### 无构建流程
- 这是一个零构建工具的项目，所有代码都在 `index.html` 中
- 直接在浏览器中打开 `index.html` 即可运行
- 修改代码后，刷新页面即可看到更改

### 代码组织
- HTML结构采用语义化标签和响应式布局
- CSS完全基于Tailwind CSS类名，无自定义CSS
- JavaScript代码内嵌在HTML文件末尾的 `<script>` 标签中
- 使用原生JavaScript，无外部依赖库

### 核心功能模块
1. **语音控制** - 基于Web Speech API的语音合成功能
2. **Markdown清理** - 自动清理Markdown格式符号的文本预处理
3. **UI交互** - 包括参数调节、按钮控制、快捷键支持
4. **剪贴板集成** - 支持一键粘贴和粘贴并朗读功能

### 开发规范
- 遵循项目的深色主题和Bento风格设计
- 保持响应式设计，确保移动端兼容性
- 使用语义化HTML结构
- 所有样式必须使用Tailwind CSS类名
- 保持代码在单个HTML文件中的组织性

### 测试
- 在多个现代浏览器中测试语音功能
- 验证移动端和桌面端的响应式表现
- 测试不同语音引擎的兼容性

### 功能特性
- 支持多种语音引擎和语言
- 可调节语速、音调、音量参数
- 智能Markdown格式清理
- 快捷键支持（Ctrl + Enter）
- 剪贴板集成功能
- 实时状态反馈

## 部署说明

由于这是一个纯静态的单页面应用：
- 可以直接部署到任何静态网站托管服务
- 支持本地直接运行（双击HTML文件）
- 无需服务器端配置或数据库