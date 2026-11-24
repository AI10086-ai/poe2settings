# AdSense 整改变更清单 — 2026-11-24

站点：https://poe2settings.com
范围：清除全站无出处的精确性能数字与绝对化表述，不新增页面、不改 URL、不动广告后台。

## 一、首页（index.html）定点整改

| 编号 | 位置 | 原文摘要 | 改后摘要 |
| --- | --- | --- | --- |
| A1 | §07 Nvidia Reflex（正文 + i18n 中英文） | "Measured improvement: an average of 18ms ... on an RTX 4070." | 改为社区口径："Community reports commonly show a noticeable system-latency reduction ... this site has not run a controlled benchmark to confirm a specific figure." |
| A2 | §02 Global Illumination（正文 + i18n 中英文） | "GI alone can consume 4-5ms ... you reclaim 3-4ms of frame budget." | 改为定性："it is the first setting worth lowering" / "you free up meaningful frame budget." |
| A3 | §02 Nvidia Reflex 提示（正文 + i18n 中英文） | "reducing system latency by up to 38% in GPU-bound scenarios." | "reducing system latency in GPU-bound scenarios (community-reported gains vary widely by hardware and scene)." |
| A4 | §05 Sound Settings（正文 + i18n 中英文） | "reclaim 5-8% CPU throughput" | "can free up CPU headroom" |
| A5 | §06 Builds | "Starter Builds (0.5.5)" / "tested on the 0.5.0 passive tree ... for 0.5.5" | "(0.5.5f)" / "were tested on the 0.5.x passive tree ... for 0.5.5f" |
| A6 | §02 Texture Streaming | "This completely eliminates the teleport-and-freeze problem" | "This can help reduce the teleport-and-freeze problem" |

同一类问题在首页的其他位置一并处理：

- HowTo JSON-LD：移除 "reclaim 3-4ms" 与 "up to 18ms"，改为定性描述。
- 中文翻译串同步修改，避免切换语言后旧数字重新出现。
- "Completely" 用于描述网络节流的表述改为中性动词。

保留不动（带免责声明，属于允许保留的社区数据）：§02 Community-Reported Gains 区块的 +45% / −18 ms / −4 ms 三组数字及其脚注。

## 二、全站指南排查（guides/）

共检查 38 篇指南 + 索引页。修改 32 篇，6 篇确认无问题。

### 2.1 逐页变更

| 文件 | 变更内容 |
| --- | --- |
| poe2-0-5-0-performance-guide.html | GI 4-5ms、阴影 2ms、反射 1.5ms 改为定性描述；"10 proven stutter fixes" → community-tested |
| poe2-0-5-0-stuttering-fix.html | 标题/H1/OG/JSON-LD 的 "Proven Solutions / Proven Fixes" → "Community-Tested" |
| poe2-0-5-0b-hotfix.html | "11 proven solutions" → "11 community-tested solutions" |
| poe2-0-5-5-forbidden-rites.html | "GI on Low reclaims 3–4 ms" → "frees up frame budget" |
| poe2-1-0-full-release-december.html | "we've documented stable 60 FPS" → "our GTX 1060 guide targets stable 60 FPS"；原有"extrapolation, not benchmarks"免责声明保留 |
| poe2-best-endgame-settings.html | GI 4-6ms、阴影 2ms、反射 1.5ms 改为定性（"Effectively unnoticeable"） |
| poe2-competitive-settings.html | "GI is a frame-time hog (4-5ms)" → "major frame-time cost"；"eliminates frame-buffer input lag" → "reduces" |
| poe2-cpu-bottleneck-fix.html | OG 描述中的 "Proven fixes" → "Community-tested fixes" |
| poe2-crashing-fix.html | 标题/H1/OG/JSON-LD 的 "Proven Fixes" → "Community-Tested"；DDU "completely remove" → "remove" |
| poe2-driver-settings.html | "eliminates a major source of stutter" → "can remove"；"never recompile" → "rarely recompile" |
| poe2-dx12-vs-vulkan.html | "in our testing" → "according to community comparisons"；"difference is under 1ms" → "difference is small" |
| poe2-input-lag-fix.html | 标题/H1/OG 的 "7 Proven Fixes" → "7 Community-Tested Fixes" |
| poe2-network-settings.html | "zero desync" → "minimal desync" |
| poe2-ram-requirements.html | "We tested the same system ..." → "Community-reported comparisons ... (illustrative, not a controlled test)" |
| poe2-settings-gtx-1060.html | 反射 1.5ms 改为定性；新增页末社区数据说明 |
| poe2-settings-gtx-1660.html | GI 4-5ms、阴影 2ms 改为定性；新增页末说明 |
| poe2-settings-rtx-3050.html | 阴影 2ms、Reflex 10ms 改为定性；新增页末说明 |
| poe2-settings-rtx-3060.html | 阴影 2ms、Reflex 15ms 改为定性；"eliminates the most common stutter trigger" → "can reduce"；新增页末说明 |
| poe2-settings-rtx-3070.html | GI 3-4ms、阴影 1.5ms、Reflex 18ms 改为定性；"Tested values" → "Recommended values"；新增页末说明 |
| poe2-settings-rtx-3080.html | GI 3ms、Reflex 12-15ms、阴影 1.5ms 改为定性；删除正文中 "144 FPS / 110+ FPS" 的配置效果断言；新增页末说明 |
| poe2-settings-rtx-4060.html | 阴影 2ms、Reflex 15ms 改为定性；新增页末说明 |
| poe2-settings-rtx-4070.html | "keeping system latency under 25 ms" → "low"；"Tested values" → "Recommended values"；新增页末说明 |
| poe2-settings-rtx-4080.html | "adds ~8-12 ms of latency" → "noticeable latency"；"seamless" → "noticeably smoother"；"Tested values" → "Recommended values"；新增页末说明 |
| poe2-settings-rtx-4090.html | "input latency below 15 ms" → "low"；"maintains over 130 FPS" → "high frame rates"；"completely invisible" → "effectively invisible"；新增页末说明 |
| poe2-settings-rx-6800-xt.html | GI 3ms、阴影 0.8ms、反射 1ms、Anti-Lag 12ms 改为定性；新增页末说明 |
| poe2-settings-rx-7600.html | GI 3.5ms 改为定性；新增页末说明 |
| poe2-settings-rx-7800xt.html | GI 4ms、阴影 2ms 改为定性；新增页末说明 |
| poe2-settings-rx-7900xtx.html | GI 5-6ms 改为定性；"completely eliminates texture pop-in" → "can greatly reduce"；"will never hit VRAM" → "unlikely to"；新增页末说明 |
| poe2-ssd-vs-hdd.html | "proven reliability" → "solid reliability"；新增页末数据说明 |
| poe2-steam-deck-settings.html | 新增页末社区数据说明（原有 Verified 更新块保留） |
| poe2-town-fps-fix.html | JSON-LD 中 "Proven fixes" → "Community-tested fixes" |
| poe2-windows-11-optimization.html | "completely disables network throttling" → "disables" |

### 2.2 已查、无问题（未改动）

| 文件 | 结论 |
| --- | --- |
| poe2-beginner-builds.html | 已查，无无出处数字；"completely reworked passive tree" 属补丁事实描述 |
| poe2-controls-guide.html | 已查，无性能数字断言 |
| poe2-gsync-freesync.html | 已查，无性能数字断言 |
| poe2-loot-filter-guide.html | 已查，无性能数字断言 |
| poe2-mac-settings.html | 已查，仅设置建议，无实测帧数 |
| poe2-performance-graph-guide.html | 已查，6.9ms/16.7ms 为帧时间换算公式，非效果断言 |
| guides/index.html | 已查，仅卡片摘要，无数字断言 |
| about.html / privacy.html / disclaimer.html / 404.html | 已查，无问题 |

## 三、待决事项（只登记，未改）

1. **内容偏薄的指南（18 篇，正文少于 600 词）**：
   - 407 词：poe2-settings-rtx-4060
   - 423：poe2-controls-guide
   - 455：poe2-settings-gtx-1060
   - 464：poe2-gsync-freesync
   - 466：poe2-settings-rtx-3070
   - 478：poe2-settings-rtx-3080
   - 487：poe2-settings-rx-6800-xt
   - 504：poe2-settings-rtx-4080
   - 506：poe2-settings-rtx-3060
   - 515：poe2-settings-rtx-4070
   - 537：poe2-settings-rtx-3050
   - 550：poe2-windows-11-optimization
   - 553：poe2-settings-rx-7600
   - 561：poe2-dx12-vs-vulkan
   - 573：poe2-settings-rx-7800xt
   - 582：poe2-settings-rx-7900xtx
   - 594：poe2-performance-graph-guide
   - 596：poe2-settings-rtx-4090
   建议下一轮用真实实测内容扩写，不要用模板填充。
2. **正文中的历史版本引用**：多数指南正文写 "in 0.5.0"，属于该指南的写作版本背景，未改成 0.5.5f（改了会变成虚假声明）。指南标题/H1 中的版本号按约定未动。
3. **Benchmark 小节内的 FPS/百分比**：保留，因为已有 "Illustrative figures from community-reported runs..." 免责说明。
4. **`production_Config.ini` 键名**：不在本轮范围，等待真实客户端核对（见独立任务）。

## 四、验收结果

| 检查 | 结果 |
| --- | --- |
| `grep "18ms\|38%\|4-5ms\|3-4ms\|5-8%\|0.5.0 passive" index.html` | 无匹配（保留的收益区为 "-18 ms" 形式） |
| 站内链接完整性 | broken = 0 |
| JSON-LD 合法性 | invalid = 0 |
| Tailwind CDN 引用 | 0 |
| 带 `.html` 的站内链接 | 0 |
| 占位/未完成文本（coming soon / TODO / TBD / lorem） | 0 |
| 390px 移动端横向溢出 | 无 |

所有改动页面的 `sitemap.xml` lastmod 已更新为 `2026-11-24`。