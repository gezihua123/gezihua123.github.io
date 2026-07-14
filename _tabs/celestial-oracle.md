---
icon: fas fa-star
order: 6
title: Celestial Oracle
---

> **Celestial Oracle** — 你的手机上的 AI 命理师。端侧运行 6 亿参数模型，将 1300 年历史的中国皇家命理系统翻译成诗意英文。
{: .prompt-info }

---

## 📋 项目文档

<div class="card-wrapper">
  <a href="/celestial-oracle/product-features/" class="card" style="display: block; padding: 1.5rem; margin-bottom: 1rem; border: 1px solid var(--border); border-radius: 0.5rem; text-decoration: none; transition: border-color 0.2s;">
    <div style="display: flex; align-items: center; gap: 1rem;">
      <div style="font-size: 2rem;">📋</div>
      <div>
        <div style="font-weight: 700; font-size: 1.1rem; color: var(--heading);">产品功能文档</div>
        <div style="font-size: 0.9rem; color: var(--text-muted); margin-top: 0.25rem;">四大核心功能、体验设计、隐私与付费模式、使用场景</div>
      </div>
    </div>
  </a>
</div>

<div class="card-wrapper">
  <a href="/celestial-oracle/technical-architecture/" class="card" style="display: block; padding: 1.5rem; margin-bottom: 1rem; border: 1px solid var(--border); border-radius: 0.5rem; text-decoration: none; transition: border-color 0.2s;">
    <div style="display: flex; align-items: center; gap: 1rem;">
      <div style="font-size: 2rem;">🔧</div>
      <div>
        <div style="font-weight: 700; font-size: 1.1rem; color: var(--heading);">技术架构文档</div>
        <div style="font-size: 0.9rem; color: var(--text-muted); margin-top: 0.25rem;">AI Agent 协作系统、端侧推理引擎、命理计算引擎、技术栈全览</div>
      </div>
    </div>
  </a>
</div>

---

## 🚀 项目概览

**Celestial Oracle** 是一个端侧 AI 命理 App，面向美国市场 25-45 岁对东方命理好奇的英语用户：

| 维度 | 说明 |
|------|------|
| **AI 模型** | Qwen3-0.6B（6 亿参数），端侧运行 |
| **推理引擎** | 阿里 MNN + llama.cpp 双引擎 |
| **平台** | Android + iOS（Kotlin Multiplatform） |
| **隐私** | 无账号，出生日期不上传服务器 |
| **付费** | 一次性购买，非订阅制 |

### 四大核心功能

| 功能 | 一句话 |
|------|--------|
| 🧭 八字命盘 | 输入出生时间，生成完整命盘 |
| 🌤️ 每日运势 | 结合命盘 + 黄历，计算今日宜忌 |
| 🌙 梦境解析 | 周公解梦 + AI 润色，两步体验 |
| 📅 人生运程 | 8 步大运，80 年人生时间线 |

### 开发架构亮点

开发侧采用 **7 角色 AI Agent 多角色协作系统**（CO/PM/RD/DD/CR/QA/UI），通过共享文档驱动通信，实现从需求到交付的完整质量闭环。

产品侧端侧推理引擎采用 **MNN 主力 + llama.cpp 回退** 双引擎设计，支持流式和非流式 AI 润色，四层容错降级确保用户始终看到结果。
