---
icon: fas fa-star
order: 6
title: Ming
description: Ming — 端侧 AI 命理 App。端侧运行 6 亿参数 AI 模型，将 1300 年历史的中国皇家八字命理系统（唐代李虚中三柱法 + 宋代徐子平四柱八字）翻译成诗意英文。隐私优先，无需注册，离线运行。美国市场 25-45 岁东方命理爱好者的首选应用。
tags: [AI命理, 八字, BaZi, 四柱八字, 端侧AI, 隐私, iOS, Android, 东方命理, 五行, 农历, 周公解梦, Qwen3, 离线AI, 命理App, 天干地支, 十神, 大运, 流年, 端侧推理]
redirect_from:
  - /celestial-oracle/
---

> **Ming** — 你的手机上的 AI 命理师。端侧运行 6 亿参数模型，将 1300 年历史的中国皇家命理系统翻译成诗意英文。
{: .prompt-info }

---

## 📋 项目文档

<div class="card-wrapper">
  <a href="/ming/product-features/" class="card" style="display: block; padding: 1.5rem; margin-bottom: 1rem; border: 1px solid var(--border); border-radius: 0.5rem; text-decoration: none; transition: border-color 0.2s;">
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
  <a href="/ming/technical-architecture/" class="card" style="display: block; padding: 1.5rem; margin-bottom: 1rem; border: 1px solid var(--border); border-radius: 0.5rem; text-decoration: none; transition: border-color 0.2s;">
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

**Ming**（明）是一个端侧 AI 命理 App，面向美国市场 25-45 岁对东方命理好奇的英语用户。最新版本 **v1.11.1**。

| 维度 | 说明 |
|------|------|
| **AI 模型** | Qwen3-0.6B（6 亿参数），MNN INT4 量化，端侧运行 |
| **推理引擎** | 阿里 MNN 主力 + llama.cpp 回退，双引擎自动切换 |
| **平台** | Android 10+ / iOS 16+（Kotlin Multiplatform + Compose） |
| **隐私** | 无账号体系，出生日期仅存设备本地 MMKV |
| **付费** | 一次性购买，非订阅制 |
| **部署** | fastlane 自动打包上传 Google Play |

### 四大核心功能

| 功能 | 一句话 |
|------|--------|
| 🧭 八字命盘 | 输入出生时间，生成完整命盘 + 四维度评分 |
| 🌤️ 每日运势 | 黄道黑道十二神 + 建除十二星 + 逐时吉凶地图 |
| 🌙 梦境解析 | 周公解梦符号库 + AI 流式润色，两步体验 |
| 📅 人生运程 | 8 步大运 × 10 年 = 80 年时间线，含关键转折年 |

### 架构亮点

- **FortuneEngine 统一入口** — 唯一 public API，内部 6 个 Engine 协同（Bazi / DaYun / DailyFortune / Period / Lunar / Bagua），全部 internal
- **日运双重神煞** — 黄道黑道十二神（协纪辨方书） + 建除十二星，逐时吉凶地图，非通用运势
- **大运个性化降级链** — DaYunModelRepository (JSON) → SQLite → PeriodEngine fallback，身强/身弱给出相反解读
- **Repository 数据驱动** — DailyFortuneRepository / DaYunModelRepository，硬编码转 JSON 配置文件
- **JsonAssetLoader** — 统一资产加载入口，零 openAsset() 调用
- **7 角色 AI Agent 协作** — CO/PM/RD/DD/CR/QA/UI，共享文档驱动通信，全流程质量闭环
- **MNN + llama.cpp 双引擎** — 流式和非流式 AI 润色，四层容错降级
