---
site_id: "imagehub"
name: "ImageHub"
production_url: "https://imagehub.ai/"
changelog_url: "https://imagehub.ai/changelog/"
delivery_method: "not_established"
target_repository: "not_established"
default_branch: "not_established"
updated_at: "2026-09-07"
---

# ImageHub 当前待办事项

## 已批准任务

### 建立 Privacy、Terms 与 About 页面

- 优先级：`P0`
- 页面或界面：全站页脚、`https://imagehub.ai/privacy/`、`https://imagehub.ai/terms/`、`https://imagehub.ai/about/` 和站点地图
- 当前问题与线上证据：全站页脚已有 `Privacy`、`Terms`、`About`，但三个链接均指向当前页面的 `#`；站点地图也没有对应页面。网站缺少公开的隐私政策、使用条款和运营主体介绍。
- 修改要求：创建三个可公开访问的英文页面，并把全站页脚链接分别连接到 `/privacy/`、`/terms/`、`/about/`。三页都显示运营主体 `QUEST LABS LIMITED`、地址 `RM 1605 HO KING COMM CTR, 2-16 FA YUEN ST, MONG KOK, HONG KONG` 和邮箱 `support@imagehub.ai`，使用实际首次发布日期作为 `Effective date`，不使用占位符。Privacy 必须说明：图片和提示词会发送到 ImageHub 服务端及完成任务所必需的 AI 服务商；内容仅用于提供所请求的服务，不用于训练模型；免费任务的上传内容和生成结果在任务完成后 24 小时内从活动系统删除；技术日志不保存图片内容；只有用户主动保存到 Workspace 的内容才持续保留，用户可以自行删除；同时如实说明账户信息、技术信息、Cookie 或本地存储、服务商处理、跨境处理、安全措施、用户请求方式和政策变更。Terms 必须说明：独立功能落地页无需账户，首页 all-in-one Workspace 发起任务必须登录；用户保留上传内容的权利，并仅授予提供服务所必需的处理许可；输出可用于个人及商业用途，但不保证独占性、版权成立或不侵犯第三方权利；侵权或下架请求发送至 `support@imagehub.ai`；禁止违法、侵权、欺诈、冒充、骚扰、绕过安全措施和任何 NSFW 内容。`Prohibited use` 必须原样包含：`No NSFW content. You must not use ImageHub to upload, submit, prompt for, generate, edit, transform, or share any content that is not safe for work (“NSFW”). This prohibition includes pornography, full or partial nudity, sexually explicit or sexually suggestive material, fetish content, sexual exploitation, sexual violence, graphic gore, and any sexualized content involving minors. NSFW content is prohibited without exception.` `Accounts` 必须原样包含：`Accounts and workspace access. You can use ImageHub tools directly from their individual tool pages without creating an account or signing in. You must sign in to start a task from the all-in-one workspace on the ImageHub homepage. An account is required only for tasks started from the homepage workspace.` About 使用以下正文：`ImageHub brings AI image generation, editing, enhancement, and transformation tools together in one browser-based workspace. People can use ImageHub to create new visuals, remove or replace backgrounds, improve image quality, restore photos, explore styles, and complete other everyday image tasks. Our goal is to make useful image workflows easier to access without requiring complex desktop software. Each ImageHub tool is designed around a focused task, with clear inputs and downloadable results. ImageHub is operated by QUEST LABS LIMITED.` 随后显示上述业务地址和联系邮箱。为三页分别设置唯一 Title、Meta Description、自引用 Canonical 和一个可见 H1，并把三页加入站点地图。
- 验收标准：三个 URL 均返回 200，页脚在首页及全部共用页脚页面都能直接打开对应 URL；页面中没有占位符、空链接或虚构的成立年份、团队规模、客户数量、总部、认证及安全承诺；Privacy 完整呈现已经确认的数据规则；Terms 完整呈现账户边界、内容权利、商业使用限制、投诉渠道及禁止用途，并完整包含两段指定英文规则；三页均只有一个 H1，Title、Meta Description、Canonical 唯一且正确，站点地图包含三个 URL。
- 不要修改：不要改变现有登录方式、Workspace 数据保存逻辑、免费任务的处理流程或删除机制；不要加入“完全在浏览器本地处理”“从不上传”“无限免费”“保证版权”“保证不侵权”等未经批准的承诺；不要弱化 NSFW 禁令或增加任何例外。

### 统一页头 Workspace 入口和登录说明

- 优先级：`P0`
- 页面或界面：全站桌面端和移动端页头、`https://imagehub.ai/` 首屏集合功能模块、FAQ、页脚及全部独立功能落地页
- 当前问题与线上证据：未登录页头当前显示 `Sign in` 和 `Try ImageHub free`，没有 `Workspace` 入口；登录后头像左侧也没有 `Workspace`。首页 FAQ 仍笼统声称所有功能都无需登录，与“独立功能落地页无需登录、首页集合功能模块必须登录 Workspace”的实际产品规则冲突。
- 修改要求：登录状态下，在头像左侧增加可见文案固定为 `Workspace` 的按钮，点击后直接打开现有 Workspace。未登录状态下，完全删除 `Try ImageHub free`，在 `Sign in` 左侧增加 `Workspace`；点击后打开现有登录弹窗，登录成功后自动进入 Workspace。`Sign in` 继续执行现有普通登录行为。桌面端和移动端都必须保留清晰可发现的 Workspace 入口。首页集合功能模块在输入或提交区域显示 `Sign in to use the workspace. No account is required on individual tool pages.` 首页 FAQ 标题改为 `How ImageHub tools and workspace access work.`；问题 `Do I need an account or to log in?` 的答案改为 `You do not need an account when you use a tool from its individual tool page. Tasks started from the all-in-one workspace on the ImageHub homepage require you to sign in.`；全站共用的 `Free · no sign-up` 改为 `No sign-up on individual tool pages`。独立功能落地页继续允许用户无需登录直接提交任务。
- 验收标准：未登录页头右侧顺序为 `Workspace`、`Sign in`，页面中不再出现 `Try ImageHub free`；未登录点击 Workspace 会打开登录弹窗，成功登录后自动进入 Workspace。登录后页头右侧顺序为 `Workspace`、头像或账户菜单，点击 Workspace 直接进入 Workspace。移动端入口不与 Logo、导航或账户控件重叠。按钮支持键盘焦点及 Enter/Space 激活，具有明确的可访问名称。首页集合功能提交会要求登录，所有独立功能落地页仍可在未登录状态完成任务。FAQ、页脚和提示文案与这套规则完全一致。
- 不要修改：不要改变现有认证方式、Workspace 路由、头像、`Free` 套餐标记、账户菜单、导航分类或独立工具的任务流程；不要要求用户登录后才能使用独立功能落地页；不要把 Workspace 按钮改成其他泛化 CTA。

### 让 Tools 按钮显示当前选中的功能

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/` 首屏集合功能模块的 Tools 下拉框、已选功能状态及桌面端和移动端布局
- 当前问题与线上证据：选择功能后，左侧下拉按钮仍显示 `Tools`，右侧另行出现深色功能标签和清除按钮。同一状态由两个分离控件重复表达，占用输入区空间。
- 修改要求：没有选择功能时，下拉按钮显示现有图标、`Tools` 和展开箭头。选择功能后，同一个按钮立即显示完整的已选功能名称并关闭菜单，不再创建右侧功能标签或独立清除按钮。再次点击该按钮时展开同一功能列表，自动把当前选中项滚动到可见区域，使用现有选中样式及可访问状态清晰标记，并让键盘焦点落在当前项。用户选择其他功能后，更新按钮文案和对应功能状态，关闭菜单并把焦点返回触发按钮。保留正确的 `aria-expanded`；窄屏可在视觉上省略过长名称，但辅助技术必须获得完整功能名。
- 验收标准：初始状态只显示 `Tools`；选择 `Generate Background` 后按钮显示 `Generate Background`，右侧不存在 `Generate Background ×` 或任何替代标签和清除控件；选择其他功能时按钮立即显示新名称。再次展开菜单时当前项可见、被标记为选中且获得键盘焦点。鼠标、触摸和键盘均可切换功能，关闭菜单后焦点位置正确。桌面端和移动端均不发生控件重叠或输入区溢出。
- 不要修改：不要改变功能列表、分类、功能参数、图片数量要求、模型选择器、上传与提示词行为、首页 Workspace 登录规则或独立功能落地页；不要新增任何替代的已选功能标签或独立清除控件。

### 为 Traction 数据增加固定统计口径

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/` 的 Traction 区块
- 当前问题与线上证据：首页展示 `130+ countries`、`98.9% AI task success rate`、`86% of creators come back for more`，但没有数据口径、时间范围或更新时间，用户无法理解三个数字的计算方式。
- 修改要求：保留三个现有数字和标题，在同一区块就近增加 `How these figures are calculated` 展开入口。首次发布时，展开内容固定为：`Figures are based on aggregated ImageHub product activity for the 12 months ending August 2026 and are updated monthly. Country coverage counts countries and regions with at least one successful task, based on anonymized IP geolocation. Task success rate is the share of accepted tasks that produced a downloadable result, excluding user-cancelled tasks, policy-blocked requests, and duplicate requests. Creator return rate is the share of anonymized users who completed a first successful task and completed another successful task within 30 days.` 在入口附近显示 `Last updated: August 2026`。此后每月使用同一口径同步更新三个数字、12 个月统计截止月份和 `Last updated` 月份。
- 验收标准：三个数字保持显示；用户无需离开首页即可查看完整统计口径；首次发布内容逐字匹配指定英文文案，不存在占位符；统计周期明确为截至 August 2026 的过去 12 个月；国家覆盖、任务成功率和回访率的分子、分母或判断条件与指定文案一致；展开控件支持键盘操作并正确暴露展开状态。
- 不要修改：不要删除或重新计算现有三个数字，不要改变统计定义，不要公开个人信息、客户数据、内部日志、机密指标或安全敏感实现，不要使用只有 `internal data` 而没有口径的模糊说明。

### 改写 Background Remover 的结果性承诺

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/ai-background-remover/`
- 当前问题与线上证据：页面使用 `sub-pixel accurate`、`strictly compliant` with Amazon, eBay and Shopify requirements、`Increase your store's click-through rates` 等无法由公开页面证明的精度、平台合规和转化结果承诺。
- 修改要求：保留页面现有功能结构，将 `sub-pixel accurate` 改为 `Designed to preserve fine edges such as hair and product details.`；将 Amazon、eBay 和 Shopify 的严格合规表述改为 `Create clean product backgrounds for marketplace-ready listings. Always review each marketplace’s current image requirements before publishing.`；将点击率提升承诺改为 `Create cleaner, more consistent product images for your storefront.` 同步替换同页中语义相同的标题、正文、卡片和 FAQ 文案，确保页面不再暗示保证精度、自动满足第三方平台规则或必然提升点击率。
- 验收标准：页面中不再出现 `sub-pixel accurate`、`strictly compliant`、`Increase your store's click-through rates` 或语义等价的保证性文案；三个指定替换文案均显示在原声明对应的位置；页面仍清楚表达细节边缘处理、商品图片背景和店铺视觉一致性的用途；桌面端和移动端排版没有溢出。
- 不要修改：不要改变 Background Remover 的处理能力、上传流程、输出格式、页面布局、导航、定价或其他工具页面；不要新增精度百分比、平台认证、客户结果、点击率或销售提升数据。

### 修复登录弹窗造成的重复 H1

- 优先级：`P2`
- 页面或界面：站点地图 `https://imagehub.ai/sitemap.xml` 列出的全部公开页面及登录弹窗
- 当前问题与线上证据：当前 33 个公开页面的静态 HTML 都因登录弹窗标题 `Welcome to ImageHub` 使用 H1 而包含第二个 H1，造成页面主标题层级重复。
- 修改要求：保留每个页面当前可见的主 H1 文案和层级，把登录弹窗标题 `Welcome to ImageHub` 从 H1 改为 H2。保留弹窗通过 `aria-labelledby` 获得可访问名称的关系。弹窗关闭时不得暴露给辅助功能树；打开后把焦点移入弹窗并正确朗读 H2 标题；关闭后把焦点返回触发登录弹窗的控件。
- 验收标准：重新抓取站点地图中的全部公开页面，每页静态 HTML 必须且只能包含一个 H1，且该 H1 是页面当前可见的主标题；登录弹窗中不存在 H1，打开后存在可见的 `Welcome to ImageHub` H2，并具有正确的可访问名称和焦点行为。
- 不要修改：不要修改页面主 H1 文案、登录弹窗文案、认证流程、弹窗视觉样式、页面 Title 或 Meta Description；不要通过视觉隐藏第二个 H1、删除弹窗标题或移除可访问名称来规避问题。

### 发布本批次公开更新日志

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/changelog/`、全站页脚和站点地图
- 当前问题与线上证据：网站当前没有公开更新日志页面，用户无法查看本批次已上线的产品改进。
- 修改要求：创建公开可访问的 `/changelog/` 页面，在本批次其他任务实际发布后新增一条使用实际发布日期的英文更新记录。记录内容仅概括实际上线的用户可见变化：新增 Privacy、Terms、About 页面，统一 Workspace 入口与登录说明，优化首页 Tools 选择器，补充 Traction 统计口径，改写 Background Remover 结果性承诺，以及修复登录弹窗的重复 H1。若其中某项没有实际上线，不得写入该项。将 Changelog 加入全站页脚和站点地图；保留以后新增历史记录的时间顺序结构。
- 验收标准：`/changelog/` 返回 200，具有唯一 Title、Meta Description、自引用 Canonical 和一个可见 H1；页脚可直接打开该页面；站点地图包含该 URL；本批次记录日期真实、内容与实际上线范围一致，不包含未发布项目。
- 不要修改：不要记录代码文件、组件、架构、仓库、分支、提交、基础设施、服务商配置、成本、密钥、安全敏感实现、客户数据、内部指标、AI 提示词或内部工作流；不要删除或改写未来已有的历史记录。
