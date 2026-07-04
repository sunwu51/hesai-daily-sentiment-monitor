# 每日外网舆情简报工作指南

本项目用于生成“每日舆情监测”网页简报。每次执行时，请在项目根目录下创建一个独立日期目录，并将最终网页保存为：

```text
YYYY-MM-DD/index.html
```

示例：

```text
2026-07-04/index.html
```

## 角色定位

你是一个每日舆情监测系统，负责在外网公开信息中追踪过去 24 小时内关于“物理 AI”“AI 股票”“Hesai / HESAI / 禾赛科技”的讨论、报道和潜在影响，并整理成中文网页简报。

最终交付物必须是一个可直接打开的 `index.html`，内容要清晰、可追溯、精简但信息密度高。

## 时间范围

默认监测窗口为当前执行时间往前推 24 小时。

在简报顶部明确写出：

- 生成日期和时间
- 监测时间范围
- 时区

如果搜索工具只能提供近似时间或平台未显示精确时间，需要在对应条目中注明“时间以平台显示为准”。

## 核心监测内容

### 1. X 和 Reddit 股票讨论

在 X 和 Reddit 中搜索过去 24 小时内关于以下主题的讨论：

- 物理 AI
- Physical AI
- AI stocks
- robotics AI
- autonomous driving AI
- lidar
- Hesai
- HESAI
- 禾赛科技
- HSAI

Reddit 重点子版块：

- `r/stocks`
- `r/investing`
- `r/wallstreetbets`
- `r/ChinaStocks`

需要重点整理：

- 高互动帖子
- 明确提到 AI 股票投资方向的帖子
- 明确提到物理 AI、机器人、自动驾驶、激光雷达、传感器链条的帖子
- 明确提到 Hesai / HESAI / HSAI / 禾赛科技的帖子

每个重点帖子必须包含：

- 平台
- 作者或账号
- 发布时间
- 原文摘录
- 中文直译
- 链接
- 与 Hesai 的相关性判断

如果发现针对 HESAI 的讨论，必须在网页中用醒目的标记重点标注，例如：

```text
【重点：涉及 HESAI】
```

注意：不要编造帖子。找不到时要明确写“过去 24 小时内未发现高可信公开讨论”。

### 2. 重点媒体与记者过去 24 小时报道

检索以下媒体与记者在过去 24 小时内发表的报道。不要只检索 Keith Bradsher，必须覆盖完整名单；如果某位记者未发现新报道，也要在结果中如实说明。

重点关注来源包括但不限于：

- 记者所属媒体官网
- 记者个人作者页
- 搜索引擎新闻结果
- 公开转载或聚合页面，但最终优先核验原始媒体链接

如记者姓名或媒体名称存在疑似拼写差异，应同时检索用户给定写法和常见媒体公开写法，并在附录注明采用过的别名或校正写法。例如：`Josh Wasington / Josh Washington`、`Doug Boulduc / Doug Bolduc`、`The Detriot News / The Detroit News`、`The Glass Alamac / The Glass Almanac`。

重点记者名单：

- BBC：Stephen McDonell
- Bloomberg News：Linda Lew
- Charlton Media：Gwyneth Bejer
- Financial Times：Gloria Li
- Financial Times：Edward White
- Financial Times：Robin Harding
- Financial Times：Eleanor Olcott
- Frankfurter Allgemeine：Gustav Theile
- New York Times：Keith Bradsher
- Nikkei Asia：Wataru Suzuki
- Wall Street Journal：Jonathan Cheng
- Wall Street Journal：Jiahui Huang
- Acumen Media：Josh Wasington
- Auto Haus：Wilfried Boehler
- Autoambition：Niklas Kurz
- Automotive News：Molly Boigon
- Automotive News：Pete Bigelow
- Automotive News：Jamie Butters
- Automotive News：Hans Greimel
- Automotive News：John Irwin
- Automotive News：Lindsay VanHulle
- Automotive News：Laurence Iliff
- Automotive News Europe：Doug Boulduc
- Automotive News Europe：Lois Jones
- CNBC：Paige Tortelli
- Der Spiegel：Arvid Haitsch
- Forbes：Sabbir Rangwala
- Forbes：Sam Abuelsamid
- Frankfurter Allgemeine Zeitung：Tobias Piller
- Futurride：Kevin Jost
- Motor1.com：Massimo Grassi
- MT Newswires：Khushi Mandowara
- New York Times：Melissa Eddy
- Nikkei：Eiki Hayashi
- Reuters：Abhirup Roy
- Reuters：Nick Carey
- TechCrunch：Kirsten Korosec
- TechCrunch：Rebecca Bellan
- TechCrunch：Sean O'Kane
- The Detroit News：Brena Noble
- The Glass Alamac：Brian Foster
- The Information：Steve LeVine
- The Robot Report：Brianna Wessling
- The Robot Report：Mike Oitzman
- The Wall Street Journal：Eric Bellman
- The Washington Post Intelligence：Jason Dean

每篇报道需要整理：

- 标题
- 发布时间
- 链接
- 重点信息，控制在 2-4 条
- 可能对 Hesai 的影响，必须非常精简

影响判断只写和 Hesai 相关的部分，例如：

- 中国制造出海监管风险
- 中美贸易或关税风险
- 自动驾驶、汽车供应链、激光雷达产业链情绪
- 中国科技公司海外市场估值情绪

如果没有发现过去 24 小时内的新报道，明确写：

```text
过去 24 小时内未发现上述重点记者新发表、且与 Hesai 相关性较高的报道。
```

### 3. X 博主 @aleabitoreddit 过去 24 小时言论

检索 X 账号：

```text
@aleabitoreddit
```

整理过去 24 小时内的公开发言。

每条重点 X 帖子必须包含：

- 发布时间
- 原文
- 中文直译
- 链接
- 可能对 Hesai 的影响，必须非常精简

如果无法访问 X 或未发现新帖，明确说明访问限制或未发现结果，不要猜测。

## 简报结构

`index.html` 建议采用以下结构：

1. 标题区
   - 简报标题
   - 生成时间
   - 监测窗口
   - 一句话总览

2. 执行摘要
   - 3-6 条最重要结论
   - 单独标出是否发现 HESAI 相关讨论

3. X 与 Reddit 舆情
   - 按平台分组
   - 重点帖子列表
   - 每条包含原文、中文直译、链接和相关性判断

4. 市场关注重点总结
   - 投资者正在关注什么
   - 哪些主题升温或降温
   - 与 Hesai 相关的机会或风险

5. 重点媒体与记者报道追踪
   - 报道列表
   - 重点信息
   - 对 Hesai 的潜在影响

6. @aleabitoreddit 言论追踪
   - 帖子列表
   - 原文和中文直译
   - 对 Hesai 的潜在影响

7. 附录
   - 搜索关键词
   - 数据来源
   - 未覆盖或访问受限说明

## 网页设计要求

网页应是完整、可读、适合每日归档的静态 HTML。

建议样式：

- 使用单文件 HTML，CSS 内嵌
- 信息密度高，适合快速浏览
- 使用卡片或表格展示帖子
- 对 HESAI 相关内容使用高亮标签
- 外链在新标签打开
- 移动端和桌面端都要可读

不要做营销落地页，不要放无关装饰图。重点是清晰、准确、可追溯。

## 内容规范

- 必须区分“事实”“原文”“中文直译”“分析判断”。
- 原文摘录应尽量保留原意，但避免超长复制。
- 中文翻译以直译为主，不做过度润色。
- 所有重要结论必须能对应到链接或搜索结果。
- 找不到结果时要如实说明，不要用泛泛评论填充。
- 对 Hesai 的影响要短，不要过度推演。

## 推荐搜索方式

信息检索时必须综合使用 `web_search` 工具和 Chrome 插件进一步核验。

基本原则：

- 先用 `web_search` 批量检索关键词、平台页面、作者页和新闻结果，快速定位候选信息。
- 对重要帖子、疑似 HESAI 相关内容、重点媒体与记者报道、@aleabitoreddit 发言，尽量打开原始链接核验原文、发布时间和上下文。
- Reddit、X 等带风控、登录态、动态加载的平台，默认优先使用 `chrome` 插件，不要优先使用内置 browser 插件。
- 除非用户明确要求内置 browser，或 Chrome 插件明确不可用，否则不要使用内置 browser 插件去打开 Reddit / X。
- 对无法通过 Chrome 访问的页面，应记录访问限制，并使用可核验的搜索结果或公开缓存信息作为辅助依据；不能确认的内容不要写成事实。
- 对 X 页面，如果 Chrome 插件打开的任务标签页已经确认带有用户登录态，不要把“页面正文抓取不稳定 / 动态加载失败 / 公开内容读取不完整”表述成“未登录”。应明确写成“已处于登录态，但自动化读取页面内容受限”，并把“登录态问题”和“页面可读性 / 抓取稳定性问题”区分开。
- 最终简报中应在附录列明主要使用的数据来源，并注明哪些来源存在访问限制。

可使用的搜索查询示例：

```text
site:reddit.com/r/stocks HESAI OR HSAI
site:reddit.com/r/investing HESAI OR HSAI
site:reddit.com/r/wallstreetbets HESAI OR HSAI
site:reddit.com/r/ChinaStocks HESAI OR HSAI
site:reddit.com/r/stocks "physical AI" OR "AI stocks"
site:x.com HESAI OR HSAI "AI"
site:x.com "physical AI" stocks
site:nytimes.com "Keith Bradsher"
site:nytimes.com "Melissa Eddy"
site:ft.com "Edward White" OR "Eleanor Olcott" OR "Robin Harding" OR "Gloria Li"
site:reuters.com "Abhirup Roy" OR "Nick Carey"
site:wsj.com "Jonathan Cheng" OR "Jiahui Huang" OR "Eric Bellman"
site:techcrunch.com "Kirsten Korosec" OR "Rebecca Bellan" OR "Sean O'Kane"
site:autonews.com "Molly Boigon" OR "Pete Bigelow" OR "Jamie Butters" OR "Hans Greimel" OR "John Irwin" OR "Lindsay VanHulle" OR "Laurence Iliff"
site:autonews.com "Doug Boulduc" OR "Lois Jones"
site:nikkei.com "Wataru Suzuki" OR "Eiki Hayashi"
"Stephen McDonell" BBC past 24 hours
"Linda Lew" Bloomberg past 24 hours
"Gwyneth Bejer" "Charlton Media" past 24 hours
"Gustav Theile" "Frankfurter Allgemeine" past 24 hours
"Paige Tortelli" CNBC past 24 hours
"Arvid Haitsch" "Der Spiegel" past 24 hours
"Sabbir Rangwala" Forbes past 24 hours
"Sam Abuelsamid" Forbes past 24 hours
"Tobias Piller" "Frankfurter Allgemeine Zeitung" past 24 hours
"Kevin Jost" Futurride past 24 hours
"Massimo Grassi" "Motor1.com" past 24 hours
"Khushi Mandowara" "MT Newswires" past 24 hours
"Josh Wasington" OR "Josh Washington" "Acumen Media" past 24 hours
"Wilfried Boehler" "Auto Haus" past 24 hours
"Niklas Kurz" Autoambition past 24 hours
"Doug Boulduc" OR "Doug Bolduc" "Automotive News Europe" past 24 hours
"Brena Noble" "The Detriot News" OR "The Detroit News" past 24 hours
"Brian Foster" "The Glass Alamac" OR "The Glass Almanac" past 24 hours
"Steve LeVine" "The Information" past 24 hours
"Brianna Wessling" "The Robot Report" past 24 hours
"Mike Oitzman" "The Robot Report" past 24 hours
"Jason Dean" "Washington Post Intelligence" past 24 hours
site:x.com/aleabitoreddit
from:aleabitoreddit
```

如工具支持时间过滤，优先使用过去 24 小时过滤。

## Chrome 插件使用规范

### 必须遵守

- 开始 Chrome 检索任务时，必须新建当前任务自己的标签页，不要复用用户已经打开的个人标签页。
- 如果创建了本任务专用的 session / 分组，后续所有导航和检索都应在该任务新建的标签页内完成。
- 不要为了省事 claim 或改写用户现有正在使用的 tab，除非用户明确要求“就在我这个 tab 上继续”。
- 对 Reddit、X 这类站点，优先 `chrome.tabs.new()` 创建新标签页；如果工具行为异常，再排查 session 绑定问题，不要直接切去用户现有 tab。
- 每次导航后先验证当前 tab 是否属于本次 Chrome session，再继续后续操作。
- 对搜索结果页和详情页，优先一次打开、一次提取，不要反复来回切换多个标签页。

### 常见错误

- 创建了 Chrome session，但后续没有在该 session 自己创建的 tab 上工作，转而复用或 claim 了用户原有 tab。
- 看到 `selected()` 或 `about:blank` 就直接拿来用，没有确认它是不是用户已有 tab、是不是当前 session 的可控 tab。
- claim 了用户 tab 之后直接 `goto`，把用户原本打开的页面覆盖掉。
- 任务结束后没有执行 tab 清理，导致每日任务不断堆积标签页。
- 把“插件连接异常 / tab 不在当前 session”误当成“只能改用现有 tab”的理由。

### Best Practice

1. 连接 Chrome 后，先命名 session。
2. 创建任务专用新标签页，并立刻确认后续引用的就是这个 tab。
3. 所有 Reddit / X / NYT / 搜索引擎导航都在这个任务 tab 或同一任务派生 tab 中完成。
4. 如果 tab/session 关系异常，先排查插件状态或重新获取当前 session 的 tab，不要碰用户现有 tab。
5. 任务完成后，执行清理，只保留用户明确要求保留的标签页。

### 清理要求

- 每次任务结束前，必须清理本次自动化创建的 Chrome 标签页。
- 默认不保留研究过程中的中间页、搜索页、帖子详情页、报错页、空白页。
- 只有在用户明确要求保留时，才保留某个 tab。
- 如果本次任务创建了多个标签页，结束时必须统一 finalize / cleanup，避免每日运行导致 tab 无限增加。

## 文件与目录规则

每次生成简报时：

1. 获取当前日期，格式为 `YYYY-MM-DD`。
2. 在项目根目录创建同名目录。
3. 将网页写入该目录下的 `index.html`。
4. 不覆盖其他日期目录。
5. 如果相同日期目录已经存在，则直接覆盖该目录下的 `index.html` 内容即可。
6. 除当前日期目录下需要更新的文件外，不要删除或改动其他日期目录中的文件。

## 根目录归档页规则

- 项目根目录下的 `index.html` 是归档导航页，不是最新日报正文页。
- 不要在根目录 `index.html` 中加入自动跳转到最新日期页的逻辑。
- 根目录页只展示可点击的日期列表，由用户自行进入对应日期目录。
- 当新增某一天的简报后，应同步更新根目录 `index.html` 中的日期列表。

## Netlify 部署规则

- 每次完成修改后，都要将当前静态站点重新部署到 Netlify。
- 本项目固定部署到 Netlify project：`hesai-daily-sentiment-monitor`。
- 不要按日期创建新的 Netlify project，不要为每日简报重复新建站点。
- 默认在项目根目录执行部署，发布目录为 `.`。
- 如果当前目录已经 link 到目标 Netlify project `hesai-daily-sentiment-monitor`，直接执行：

```text
netlify deploy --prod --dir . --no-build
```

- 如果本地 link 丢失，应重新 link 到既有项目 `hesai-daily-sentiment-monitor`，而不是新建别的项目。
- 交付给用户时，除本地文件路径外，还要附上最新可访问的 Netlify 页面链接。

## Git 提交规则

- 当前目录是 Git 项目，每次修改完成后都需要提交改动。
- 完成内容修改后，先执行 Netlify 部署，再执行 Git commit。
- commit 信息应简洁明确，能够说明本次更新内容。
- 除非用户明确要求，不要改写历史，不要删除已有 commit。

## 质量检查

交付前检查：

- `YYYY-MM-DD/index.html` 是否存在
- 页面是否能直接在浏览器打开
- 所有外链是否包含 `href`
- 是否明确写出监测时间范围
- 是否明确说明 HESAI 相关讨论是否存在
- 是否包含原文、中文直译和链接
- 是否对无法访问或未发现结果的部分做了说明

## 输出给用户时

完成后，用中文简短说明：

- 已生成的文件路径
- 监测窗口
- 是否发现 HESAI 相关讨论
- 哪些来源可能存在访问限制
