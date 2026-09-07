---
site_id: "imagehub"
name: "ImageHub"
production_url: "https://imagehub.ai/"
changelog_url: "not_established"
delivery_method: "not_established"
target_repository: "not_established"
default_branch: "not_established"
updated_at: "2026-09-07"
---

# ImageHub 当前待办事项

## 待决事项

### 建立真实可访问的 Privacy、Terms 与 About 页面

- 优先级：`P0`
- 页面或界面：全站页脚，以及待建立的 Privacy、Terms 与 About 页面
- 当前问题：截至 2026-09-07，首页和已抽查的工具页页脚都显示 `Privacy`、`Terms`、`About`，但三个链接实际均指向当前页面的 `#`，不会打开任何说明页面；公开站点地图列出的 33 个 URL 也不包含隐私政策、服务条款或 About 页面。与此同时，首页声称结果可商用，Watermark Remover 声称不存储上传图片或生成结果，登录弹窗又称登录可保护用户工作区，访客无法核对数据处理、内容权利、账户规则或运营主体。
- 需要决定：由业务负责人和合格法律顾问确认运营主体、适用法律、用户上传与生成内容的权利、允许和禁止的用途、投诉或下架流程、账户条款、实际处理方、传输与存储位置、保留和删除规则、Cookie/本地存储规则及联系渠道，然后批准对应公开页面。
- 选项与取舍：推荐分别建立长期可访问的 `/privacy/`、`/terms/`、`/about/`，让页脚链接直达并纳入站点地图；Privacy 只写真实的数据流程，Terms 明确内容许可、商用范围、责任限制和滥用规则，About 提供可核验的产品与运营主体信息。若完整法律文本尚未审定，应先停止未加限定的商用、无存储等绝对承诺，而不是继续保留无效链接。

### 统一免费、登录、次数、输出与商用承诺

- 优先级：`P0`
- 页面或界面：`https://imagehub.ai/`、全部 32 个工具页、登录弹窗及未来的 Terms 页面
- 当前问题：首页 FAQ 写 `every tool here is free to use`、`Nothing is locked behind an account`、`There's no daily cap and no per-image credits`，并承诺结果无水印且可商用；Image Generator 也重复 `Free`、`No login`、`Unlimited runs`、`HD output`。但网站同时提供登录和保存工作区入口，部分公开工具页的登录弹窗显示 `Accounts are not available right now. Everything else on the site still works.`。当前没有公开条款、套餐边界或服务限制说明，访客无法判断这些绝对承诺是否适用于每个工具、匿名和登录状态、所有输出尺寸及长期产品规则。
- 需要决定：确认每个工具在匿名与登录状态下的真实价格、次数或速率限制、排队和失败规则、输出尺寸与格式、水印规则、账户功能、商用许可及未来变更方式，并指定全站唯一事实来源。
- 选项与取舍：推荐先建立一张内部可验证的能力与限制表，再把首页、工具页、登录弹窗和 Terms 统一到同一套英文文案；只有经过生产验证且可长期兑现的项目才保留 `free`、`no login`、`unlimited`、`HD`、`commercial use` 等绝对词。若存在公平使用、速率、文件、地区、模型或账户限制，应在首次使用前就用简洁限定语说明；若账户暂不可用，应隐藏或明确禁用入口并说明不影响哪些匿名功能。

### 核实或删除无法公开验证的增长与效果数据

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/` 的 Traction 区块，以及含结果、精度、合规或转化承诺的工具页
- 当前问题：首页公开展示 `130+ countries`、`98.9% AI task success rate`、`86% of creators come back for more`，但没有数据口径、样本、时间范围或来源。Background Remover 还使用 `sub-pixel accurate`、`strictly compliant` with Amazon, eBay and Shopify requirements、`Increase your store's click-through rates` 等结果性表述；这些效果和平台合规性无法仅从公开页面核验，也不能由本次审计推定为真实。
- 需要决定：确认每项数据或效果声明是否有可复现的计算方法、当前样本、时间范围、适用范围和公开依据，并确定谁负责持续更新；没有充分依据的声明是否立即删除或改成可验证的产品描述。
- 选项与取舍：推荐删除没有可公开支撑的百分比、回访率、国家数、精度、平台严格合规和点击率提升承诺；若确有可靠数据，则保留数值并就近标注口径、时间范围与可访问来源。可改用不承诺结果的事实性文案，例如描述支持的格式、实际输出类型和可观察的工作流程。

### 统一上传图片的隐私与存储说明

- 优先级：`P0`
- 页面或界面：所有需要上传图片的工具页，重点包括 `https://imagehub.ai/ai-watermark-remover/`、`https://imagehub.ai/ai-background-remover/`、登录工作区及待建立的 Privacy 页面
- 当前问题：Watermark Remover 多处绝对声称 `ImageHub does not store uploads or results`，Background Remover 只说明文件会为移除背景请求而处理，首页和页脚又使用 `Runs in your browser`。这些文案没有说明处理是否完全在本机浏览器完成，还是会上传到服务器或模型提供商，也没有说明日志、缓存、备份、失败请求、登录工作区收藏和删除机制；不同页面的详细程度不一致。
- 需要决定：确认每个工具的真实数据流、第三方处理方、传输加密、临时或持久存储、日志和备份、保留期限、训练用途、人工访问、账户与匿名差异、删除方式，以及 `Runs in your browser` 和 `does not store` 可以准确表达的边界。
- 选项与取舍：若处理完全在本地，明确写 `Processed locally in your browser; the image is not uploaded` 并以技术验证支撑；若图片会发送到服务端或第三方，改为准确说明处理目的、接收方、保留期限和删除方式。只有在上传内容、结果、缓存、日志和备份均不被持久保存时才保留绝对的 `does not store`，并让所有上传入口与 Privacy 使用同一套事实。

### 清理站点地图页面的 SEO 长度与隐藏标题结构

- 优先级：`P2`
- 页面或界面：站点地图 `https://imagehub.ai/sitemap.xml` 当前列出的全部 33 个公开页面
- 当前问题：33 个页面均返回 200，均有唯一 Title、唯一 Meta Description 和自引用 Canonical；当前基础抓取没有发现批量缺失或重复。仍有少量可清理项：`/ai-body-editor/` 的 Title 为 61 个字符；`/ai-background-remover/`、`/ai-image-extender/`、`/free-ai-image-generator/`、`/ai-beauty/`、`/ai-body-editor/` 的 Meta Description 分别为 164、167、162、175、174 个字符。每页静态 HTML 还因隐藏的登录弹窗包含第二个 H1，虽然未打开弹窗时辅助功能树只呈现页面主 H1，仍会让文档标题结构不必要地重复。
- 需要决定：是否批准本批次缩短上述 1 个 Title 与 5 个 Meta，并把登录弹窗标题调整为不与页面主标题竞争的语义层级；当前没有 Search Console 查询数据或经验证的搜索量，因此不应借此批量重写其余页面关键词。
- 选项与取舍：推荐只做最小技术清理：保留现有 URL、页面主题、唯一 Canonical 和当前英文语言，把 Title 控制在 60 个字符以内、Meta 控制在 160 个字符以内，并让每个关闭状态页面只有一个主 H1；若保留当前较长 Meta，搜索结果可能自行截断，但不会因此宣称存在排名损失。

### 确定网站修改的交付方式并建立公开更新日志

- 优先级：`P1`
- 页面或界面：推荐任务仓库 `https://github.com/DAOteam/ihreview`、ImageHub 网站代码交付流程及待建立的公开更新日志
- 当前问题：`DAOteam/ihreview` 是本次审计文档仓库，当前未提供 ImageHub 网站代码仓库、默认分支或受控生产工作区，也没有已建立的公开 changelog URL。缺少这些信息时，执行代理无法安全确定应该直接发布还是提交 Pull Request；按当前规则，在公开更新日志建立前，本次审计发现也不能进入 `已批准任务`。
- 需要决定：选择 `direct_publish` 或 `pull_request`；若选择 Pull Request，提供真实的网站代码仓库和默认分支；同时确定一个长期公开、可核验并保留历史记录的 changelog URL，以及本次发现中获准实施的范围。
- 选项与取舍：已有授权且连接生产的受控工作区时选择 `direct_publish`；需要代码审查时选择 `pull_request` 并提供真实仓库与默认分支。更新日志推荐建立独立公开页面并加入页脚，只记录实际发布且用户可见的变化；确认后再更新本文件 frontmatter，并把获批且实现条件完整的工作移入 `已批准任务`，同时增加恰好一项本批次 changelog 任务。
