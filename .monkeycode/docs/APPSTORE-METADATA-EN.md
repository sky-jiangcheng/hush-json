# App Store Connect 元数据(英文)— HushJSON: JSON Formatter

生成于 2026-09-30(对应 v1.5.84)。填入 ASC 时直接复制正文,勿带本说明头。

## Promotional Text(推广文本,限 170 字符,实际 154,可随时改、不需重新提审)

```
The private JSON toolkit: format, validate, minify and diff — all on your device. No uploads, no accounts, no tracking, works offline. Free & open source.
```

## Description(描述,限 4000 字符,实际 1689)

```
HushJSON is a fast, private JSON toolkit that runs entirely on your device. Format, minify, validate, escape, repair and diff JSON — with no uploads, no accounts and no tracking.

ALL PROCESSING STAYS LOCAL
No backend, no data collection, no sign-in. Everything you paste or open stays on your device, and the app works fully offline. Inspect API responses, config files, JWTs and log payloads — even the sensitive ones — with peace of mind.

EVERYTHING YOU NEED
• Format — 2-space indentation, syntax highlighting
• Interactive tree — expand and collapse any object or array
• Minify — compact single-line output
• Validate — live red / green feedback with precise error messages
• Auto-repair — completes missing brackets, fixes unquoted keys
• Escape / unescape — JSON string escaping
• Diff — structured recursive comparison by key, not by line; added, removed and changed values highlighted side by side
• List & detail — arrays open in a split view with item previews
• History — save results locally, reload instantly, pick two entries to compare
• Drag & drop and file open — load .json files in one step
• External keyboard — Cmd+Enter to format, Cmd+S to save, Cmd+D to download

DESIGNED FOR REAL WORK
Dark and light themes, line numbers, scroll sync, output search, and a mobile-first layout that works one-handed on iPhone and takes full advantage of iPad.

5 LANGUAGES
English, 中文, Español, Deutsch, 日本語 — switch any time in the app.

FREE & OPEN SOURCE
HushJSON is MIT-licensed open source. The web version (installable as an offline PWA) and desktop builds for macOS, Windows and Linux are on GitHub.

Privacy policy: https://sky-jiangcheng.github.io/hush-json/privacy.html
```

## What's New / Version Notes(1.5.84 提审用,覆盖 1.5.71 → 1.5.84,限 4000 字符,实际 1390)

```
Big stability and data-safety update. The app is now called HushJSON: JSON Formatter — same tool, same privacy: everything stays on your device.

DATA SAFETY
• Fixed two bugs that could silently lose saved history: top-level JSON strings (like "hello") no longer get corrupted when saved and reloaded, and a full storage no longer wipes your history — you now get a clear warning instead
• Saved entries are deduplicated, and deleting or selecting them works reliably

RELIABILITY
• Files exported from Windows tools (with a byte-order mark) now parse instead of being rejected
• The error view no longer gets stuck: fix your JSON and the formatted result comes right back, and error hints now follow your app language
• Dragging in files with an uppercase .JSON extension now works
• Clearing the editor before saving no longer overwrites the history entry you had loaded
• Diff no longer shows phantom changes or blank rows for keys like "toString"

SMOOTHER & MORE ACCESSIBLE
• Faster rendering of large JSON documents
• Pinch-to-zoom works again on iPhone and iPad
• Cleaner, distraction-free empty output panel
• Better fit for foldable iPhones and the latest iOS; now requires iOS 15 or later

SECURITY
• Hardened app isolation and dependency supply chain
• Privacy policy now available in-app and on the web

Thank you for using HushJSON — it stays free, open source, and 100% local.
```

### What's New 取舍备忘

- 只保留用户可感知项;CI 修复、Pages 部署、文档/改名工程细节(1.5.71/72/73/75/76/79/80/83)不进 What's New,但 1.5.82 品牌改名必须提(用户会看到图标标签变化)
- "silently lose saved history" 对应 1.5.81 两条数据安全缺陷,是本次最有分量的修复,放最前
- "requires iOS 15 or later" 对应 1.5.74 的 MinOS 提升,属用户需知的变化

## App Name(标题,限 30 字符,实际 24)

```
HushJSON: JSON Formatter
```

沿用 1.5.82 命名分层决策(品牌 + 品类,App Store 上架名不由仓库承载但 ASC 里应填这个)。Apple 对标题分词建索引:hushjson / json / formatter 三个 token 已覆盖最大搜索词。剩余 6 字符不值得塞丑陋后缀(如 `&Diff`,29 字符)——差异化关键词交给副标题。

## Subtitle(副标题,限 30 字符,实际 30)

```
Diff, validate, repair offline
```

选词原则:Apple 会把标题 + 副标题 + 关键词字段的 token 合并索引,副标题**不重复**标题已有 token(formatter 会被词干还原到 format)。本串引入 4 个零重复的高意图词:diff(差异化功能,搜 "json diff" 靠标题 JSON + 副标题 diff 组合命中)、validate、repair(对应自动修复功能)、offline(高意图搜索词 + 隐私卖点)。备选:

- `Beautify, diff, repair offline`(30)——beautify 也是高频搜索词,可替换 validate
- `Private. Offline. No uploads.`(29)——品牌感最强但搜索词覆盖最弱

---

# Mac App Store 版本(MAS,com.jsonbeautify.desktop.appstore)

2026-09-30 生成,对应 v1.5.84。字段上限与 iOS 相同;Mac 视角重写:去 iPhone/iPad 专属卖点(Foldable/pinch-to-zoom/one-handed),换 Finder 拖拽与键盘流。

## App Name(26/30)

**⚠️ 与 iOS 版不可重名**——iOS 与 Mac 是 ASC 两条独立 app 记录,App Name 全商店唯一,iOS 已占用 `HushJSON: JSON Formatter`。Mac 名在 iOS 基础上加非 Apple 商标的中性后缀区分,`JSON Formatter` 品类短语保持完整不断裂(精确匹配 "json formatter" 搜索)。

```
HushJSON: JSON Formatter X
```

**"X" 取舍理由**:中性单字符后缀,Xcode / macOS / iOS X 命名体系常见,不暗示付费(规避 Guideline 2.3.1 misleading metadata 风险,"Pro" / "Plus" 因此被排除)。与 iOS 名称共享 "HushJSON: JSON Formatter" 全 token,**新增 `X` 单一 token** 形成差异化;用户搜 "HushJSON: JSON Formatter" 时 iOS + Mac 双结果都命中。留 4 字符预算,后续可微调(如改 "X" 为更具体词)。

**绝对不要再用 `Mac` 后缀**——见末尾 `## 5.2.5 拒绝经验(2026-10-06)`。括号 `(Mac)`、前置 `Mac:`、后置 `: Mac` 全部被 Apple 拒绝过。前次候选 `HushJSON Studio: JSON Formatter` 是 31 字符(超 30 上限 1 字符),不可用。

> 备注:若未来想让两个平台共用同一名称,做法是把 iOS 与 macOS 挂到**同一条 app 记录**下(Apple 的 Things 3 / Fantastical 即此结构),而不是两条记录各占一名。属 ASC 结构决策,此处按两条记录现状处理。

> **bundle 对齐**:`bundle.macOS.bundleName` 已同步为 `HushJSON: JSON Formatter X`(满足 Guideline 2.3.8:App Store 名称与安装后名称一致)。

## Subtitle(30/30)

```
Diff, validate, repair offline
```

与 iOS 共用:桌面上 offline 同样是差异化卖点(对比 Electron 类联网工具),且 token 零重复原则不变。

## Promotional Text(145/170)

```
The private JSON toolkit for your Mac: format, validate, minify and diff — all offline. No uploads, no accounts, no tracking. Free & open source.
```

## Description(1626/4000)

```
HushJSON is a fast, private JSON toolkit that runs entirely on your Mac. Format, minify, validate, escape, repair and diff JSON — with no uploads, no accounts and no tracking.

ALL PROCESSING STAYS LOCAL
No backend, no data collection, no sign-in. Everything you paste or open stays on your Mac, and the app works fully offline. Inspect API responses, config files, JWTs and log payloads — even the sensitive ones — with peace of mind.

EVERYTHING YOU NEED
• Format — 2-space indentation, syntax highlighting
• Interactive tree — expand and collapse any object or array
• Minify — compact single-line output
• Validate — live red / green feedback with precise error messages
• Auto-repair — completes missing brackets, fixes unquoted keys
• Escape / unescape — JSON string escaping
• Diff — structured recursive comparison by key, not by line; added, removed and changed values highlighted side by side
• List & detail — arrays open in a split view with item previews
• History — save results locally, reload instantly, pick two entries to compare
• Drag & drop — drop .json files from Finder to load them instantly
• Keyboard shortcuts — Cmd+Enter to format, Cmd+S to save, Cmd+D to download

DESIGNED FOR REAL WORK
Dark and light themes, line numbers, scroll sync, and output search — a distraction-free workspace that stays out of your way.

5 LANGUAGES
English, 中文, Español, Deutsch, 日本語 — switch any time in the app.

FREE & OPEN SOURCE
HushJSON is MIT-licensed open source, also available for iPhone, iPad and on the web as an offline-capable PWA.

Privacy policy: https://sky-jiangcheng.github.io/hush-json/privacy.html
```

## What's New(1314/4000,覆盖 1.5.71 → 1.5.84)

```
Big stability and data-safety update. The app is now called HushJSON: JSON Formatter — same tool, same privacy: everything stays on your Mac.

DATA SAFETY
• Fixed two bugs that could silently lose saved history: top-level JSON strings (like "hello") no longer get corrupted when saved and reloaded, and a full storage no longer wipes your history — you now get a clear warning instead
• Saved entries are deduplicated, and deleting or selecting them works reliably

RELIABILITY
• Files exported from Windows tools (with a byte-order mark) now parse instead of being rejected
• The error view no longer gets stuck: fix your JSON and the formatted result comes right back, and error hints now follow your app language
• Dragging in files with an uppercase .JSON extension now works
• Clearing the editor before saving no longer overwrites the history entry you had loaded
• Diff no longer shows phantom changes or blank rows for keys like "toString"

SMOOTHER EVERY DAY
• Faster rendering of large JSON documents
• Cleaner, distraction-free empty output panel
• Full keyboard workflow: Cmd+Enter to format, Cmd+S to save, Cmd+D to download

SECURITY
• Hardened app isolation and dependency supply chain
• Privacy policy now available in-app

Thank you for using HushJSON — it stays free, open source, and 100% local.
```

### MAS 与 iOS 版差异备忘

- "on your device" → "on your Mac"(本地感更具体);促销文本加 "for your Mac"
- 描述:拖拽场景改 Finder;键盘快捷键为原生硬件键盘;iPad/one-handed 段替换为 "DESIGNED FOR REAL WORK" 工作流段
- 描述末尾提 iOS/web 版(Apple 允许跨平台提及,属常见做法;不提价格与购买方式即可)
- What's New:删 foldable / pinch-to-zoom / MinOS 15(均为 iOS 专属事实);键盘行改原生;未提 macOS 最低版本(CHANGELOG 无 macOS MinOS 变更记录,不虚构)

## 待补元数据(下次生成)

- Keywords(100 字符,逗号分隔,**不与标题/副标题重复**——重复即浪费)
- 截图文案

## 要点备忘

- 隐私政策 URL 为 ASC 必填项,即上文明文写出的 `/hush-json/privacy.html`(1.5.82 改名时修正过的地址)
- 描述首段 76 字符是折叠线前可见的钩子,主打 "private / on your device"
- 事实来源:README.md 的特性表与隐私章(未夸大:自动修复、结构化 diff、历史对比、5 语言均为已实现功能)
- 待补元数据(下次可生成):Subtitle(30 字符)、Keywords(100 字符)、What's New 版本说明

## 5.2.5 拒绝经验(2026-10-06,1.5.82 提审)

**事件**:Mac App Store 1.5.82 提审,ASC App Name 为 `HushJSON Mac: JSON Formatter`,被 Apple 以 Guideline 5.2.5 – Legal – Intellectual Property 拒绝。

**Apple 拒绝原文**:
> The app's metadata includes content that is similar to designs or terms used for Apple products and services and may cause confusion for users. Specifically, your metadata includes:
> - Terms for Mac in the app name in an inappropriate manner.

**教训(写给未来自己)**:

1. **Mac App Store 的 App Name 里绝对不能出现 `Mac` 字样**——不管什么位置(`Mac:` 前置、`: Mac` 后置、`(Mac)` 括号)都不行。Apple 的官方口径是 *"Indicating Mac compatibility in the app name is not necessary for the Mac App Store"*(用户从 Mac App Store 徽章就能看出平台)。
2. 也不要在 App Name 里出现其他 Apple 商标:`iPhone` / `iPad` / `Apple Watch` / `Apple TV` / `MacBook` / `iMac` / `Vision Pro` / `Siri` / `iCloud` / `FaceTime` / `iMessage` / `App Store` 等。
3. **合规位置**:`Mac` 可以出现在 Description / What's New / Promotional Text / Subtitle / Keywords / Screenshots 里,只要不暗示 Apple 出品或关联。"for your Mac"、"on your Mac"、"Cmd+Enter" 这种用法 Apple 明确允许。
4. **同条记录的解决方案**:如果未来想让 iOS 与 Mac 共用同一个 App Name,需要把两个平台挂到**同一条 app 记录**下(Things 3 / Fantastical 模式),而不是各占一条 App Name。

**已修复**:1.5.85 提审时 Mac App Name 改为 `HushJSON: JSON Formatter X`(26 字符,在 30 上限内),`bundle.macOS.bundleName` 同步更新。前次候选 `HushJSON Studio: JSON Formatter` 是 31 字符超限,已弃用。

