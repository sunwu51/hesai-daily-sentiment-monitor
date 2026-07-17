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

本项统一使用 Google News RSS 搜索进行过去 24 小时初筛。RSS 地址格式为：

```text
https://news.google.com/rss/search?q=<URL 编码查询>&hl=en-US&gl=US&ceid=US:en
```

查询中加入 `when:1d`，按记者、媒体和别名分批检索；控制频率并避免高并发请求，以降低 `429`、`403`、空结果或验证码页面的概率。RSS 是候选发现来源，不是原始媒体全文；只可将 RSS 实际返回的标题、链接、来源和时间写入简报，不能把 RSS 无结果表述为已逐页核验后的绝对“无报道”。

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
Google News RSS 初筛未发现上述重点记者过去 24 小时内新发表、且与 Hesai 相关性较高的报道；未逐篇原始媒体页核验。
```

### 3. Hesai 关键词新闻 RSS 追踪

除记者名单外，必须单独使用 Google News RSS 搜索 `Hesai`、`HESAI`、`HSAI`、`禾赛科技`，并将检索结果纳入当日汇总。

每条高相关新闻必须包含：

- 标题
- RSS 显示的来源和发布时间
- RSS 条目链接
- 重点信息，控制在 2-4 条
- 可能对 Hesai 的影响，必须非常精简

只收录直接涉及 Hesai、其股票、产品、客户、监管或激光雷达产业链的结果；财经网站的自动估值页、重复转载、无作者的模板化股票内容应降级标注或不纳入执行摘要。若 RSS 无高可信结果，明确写：

```text
Google News RSS 初筛未发现过去 24 小时内直接涉及 Hesai 的高可信新闻。
```

### 4. X 博主 @aleabitoreddit 过去 24 小时言论

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

5. Hesai 关键词新闻追踪
   - RSS 新闻列表
   - 重点信息
   - 对 Hesai 的潜在影响

6. 重点媒体与记者报道追踪
   - 报道列表
   - 重点信息
   - 对 Hesai 的潜在影响

7. @aleabitoreddit 言论追踪
   - 帖子列表
   - 原文和中文直译
   - 对 Hesai 的潜在影响

8. 附录
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

社媒信息必须优先使用 `superpowers-social` MCP；记者报道和 Hesai 新闻必须使用 Google News RSS 搜索。

基本原则：

- X：使用 `twitter_search`、`twitter_read`、`twitter_thread`、`twitter_user_tweets` 获取正文、账号、发布时间、链接和互动数据。
- Reddit：使用 `reddit_search` 定位候选，使用 `reddit_get_post` 获取正文及必要评论；覆盖四个指定子版块。
- 不把 MCP 搜索摘要当作事实。对拟收录的重点帖子，必须调用对应详情工具取得正文；MCP 无法返回或字段矛盾时，标注“社媒接口未能可靠确认”，不编造内容。
- 记者与 Hesai 新闻：用 Google News RSS 低频、分批检索，记录实际命中的 RSS 条目。遇到 `429`、`403`、空结果或无法解析 XML 时，写明 RSS 访问 / 检索受限，不把它写成“未发现报道”。
- 最终简报在附录列明 `superpowers-social MCP` 和 Google News RSS，并说明社媒接口和 RSS 聚合结果各自的限制。

可使用的搜索查询示例：

```text
MCP：reddit_search(subreddit=stocks|investing|wallstreetbets|ChinaStocks, query=HESAI OR HSAI OR lidar OR "physical AI" OR "AI stocks", sort=new, time_filter=day)
MCP：twitter_search(query=(HESAI OR HSAI OR "physical AI" OR lidar OR "AI stocks") since:YYYY-MM-DD)
MCP：twitter_user_tweets(handle=aleabitoreddit)
RSS：Hesai OR HESAI OR HSAI OR 禾赛科技 when:1d
RSS："记者姓名" "媒体名称" when:1d
RSS："Josh Wasington" OR "Josh Washington" "Acumen Media" when:1d
RSS："Doug Boulduc" OR "Doug Bolduc" "Automotive News Europe" when:1d
RSS："Brena Noble" "The Detroit News" when:1d
RSS："Brian Foster" "The Glass Almanac" when:1d
```

如工具支持时间过滤，优先使用过去 24 小时过滤。

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

## GitHub Pages 部署规则

- 本项目固定部署到 GitHub repo：`sunwu51/hesai-daily-sentiment-monitor`。
- 不要按日期创建新的 GitHub repo，不要为每日简报重复新建站点。
- 页面部署平台固定为 GitHub Pages。
- GitHub Pages 站点地址固定为：

```text
https://sunwu51.github.io/hesai-daily-sentiment-monitor/
```

- 部署由 GitHub Actions 工作流 `.github/workflows/pages.yml` 负责触发和发布。
- 如无特殊说明，所有可发布内容都应通过提交到 `main` 分支并 push 到远端来触发部署。
- 如果本地 Git remote 丢失，应重新连接到既有仓库 `https://github.com/sunwu51/hesai-daily-sentiment-monitor.git`，而不是新建别的 repo。
- 交付给用户时，除本地文件路径外，还要附上最新可访问的 GitHub Pages 链接。

## Git 提交规则

- 当前目录是 Git 项目，每次修改完成后都需要提交改动。
- 完成内容修改后，执行 Git commit，并 push 到 `main` 分支触发 GitHub Pages 部署。
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
