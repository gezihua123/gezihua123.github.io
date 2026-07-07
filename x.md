# phonefast on X - English / 中文

## Tweet

phonefast: Your Android phone, now an AI Agent's native peripheral.

🐢 10ms response (100× faster than ADB)
🎯 Atomic observe — screenshot + UI tree in one call, no race
🔥 MCP native ImageContent — no base64 bloat in JSON
🛡️ 144K ops, 12h stress test, 99.99% success, zero leaks

The phone is no longer a fragile debug tool. It's a perception-action terminal for AI.

↓ Benchmarks & install
https://gezihua123.github.io/phonefast-en

---

## 中文推文

**phonefast：把你的 Android 手机变成 AI Agent 的原生外设。**

🐢 10ms 级响应，比 ADB 快 100 倍
🎯 原子级 observe，截图 + 控件树一次返回，告别竞态
🔥 MCP 原生 ImageContent，不塞 base64，token 省一半
🛡️ 12 小时压测 14 万次操作，99.99% 成功率，零泄漏

手机不再是脆弱的调试工具，而是 AI 的感知-执行一体化终端。

↓ 安装 & 评测
github.com/gezihua123/phonefast

## 中文标题选项

1. **phonefast：把 Android 手机变成 AI Agent 的原生外设**

2. **10ms 够干什么？够你的 AI 操控一次手机。**

3. **ADB 太慢了。phonefast 只要 10ms。**

4. **你的手机，天生不该这么慢。**

5. **每次操作 8 秒 → 10ms。AI Agent 等了太久。**

6. **截个图等 9 秒？phonefast 167ms 搞定，还是无损 PNG。**

7. **144,348 次操作，12 小时，99.99% 成功率。就问你稳不稳。**

8. **🐢→⚡ 手机自动化的速度跃迁，从这一行命令开始。**

## Title options

1. **phonefast: The Android phone, reimagined as an AI Agent peripheral** ← 当前在用

2. **10ms. That's all it takes to turn your Android into an AI agent.**

3. **Your phone was never meant to be this fast for AI.**

4. **ADB is dead. Long live phonefast.**

5. **What if your Android could keep up with your AI Agent?**

6. **For AI Agents, 8 seconds per operation is an eternity. phonefast does it in 10ms.**

7. **Stop burning tokens on slow screenshots. phonefast speaks MCP natively.**

8. **144,348 operations. 12 hours. 100% success. Zero leaks.**

9. **phonefast: The perception-action terminal your AI has been waiting for.**

10. **Turn "adb shell" into a bad memory. 🐢 → ⚡**

## Image card idea (for reference)

| Headline | Subheadline |
|----------|-------------|
| phonefast | Turn Android into an AI Agent Peripheral |
| 10ms ⚡ | 100× faster than ADB shell |

## Hashtags

#phonefast #Android #AIAgent #MCP #MobileAutomation #AndroidAutomation #LLM #opensource


**Minimizing Token Burn in Loop Engineering on Mobile**

Loop engineering on mobile devices consumes auth tokens rapidly due to frequent re-authentication cycles during network recovery, session refresh, and background state restoration. Each loop trigger burns a fresh token, accelerating rotation and increasing backend auth load.

**Phonefast Solution** — Its <30ms atomic observe minimizes redundant loop cycles, consuming only one token per verification. Two XML dump optimizations further cut overhead: an AccessibilityService captures UI trees even when apps hang (bypassing flaky `uiautomator`), and the deeply nested XML is flattened into key-value pairs, so AI models parse linearly without structural errors — eliminating re-request retries that burn extra tokens.

↓ Benchmarks & install
https://gezihua123.github.io/phonefast-en