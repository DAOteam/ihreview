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

### 统一全站内页菜单并将 Workspace 改为黑色主按钮

- 优先级：`P1`
- 页面或界面：除首页 `https://imagehub.ai/` 和登录后的 Workspace 页面外，站点地图 `https://imagehub.ai/sitemap.xml` 中其余全部公开页面的共用页头；功能快捷按钮删除范围为全部 32 个独立功能落地页；Workspace 黑色样式同时覆盖首页、全部内页及登录后的 Workspace 页面；覆盖桌面端、移动端、登录状态和未登录状态
- 当前问题与线上证据：每个独立功能落地页的页头右侧仍显示一个指向本页主操作区域的功能按钮，并位于 `Workspace` 之前。例如 `https://imagehub.ai/free-ai-image-generator/` 显示 `Generate an image`，`https://imagehub.ai/ai-background-remover/` 显示 `Get Started`。页面正文已经提供完整的上传、生成或编辑入口，页头中的同类按钮重复占用导航空间。相同桌面视口下，`https://imagehub.ai/free-ai-image-enhancer/` 的 Workspace 已呈黑底白字，而 Image Generator 和 Background Remover 的 Workspace 仍呈白底黑字；部分页面的 Logo 显示、导航间距、按钮尺寸和右侧控件布局也会因页面级样式而不同。页头没有稳定使用同一套视觉与响应式规则。
- 修改要求：除首页和登录后的 Workspace 页面外，所有公开页面必须使用同一套共用页头结构、样式和响应式规则，不再保留任何页面级菜单变体或覆盖样式。相同视口和登录状态下，各页页头的外层高度与边界、Logo 尺寸与显隐断点、五个导航分类的字体、字号、字重、间距、下拉箭头、hover、focus-visible、展开状态及当前分类黑色胶囊样式必须一致；右侧控件的顺序、间距、垂直对齐和响应式折叠规则必须一致。唯一允许的页面差异是与当前功能对应的导航分类选中状态，以及由登录状态决定显示 `Sign in` 或头像与账户菜单。信息页面没有对应功能分类时，五个分类均保持未选中样式。从全部 32 个独立功能落地页的共用页头中彻底删除随当前功能变化的快捷按钮，包括但不限于 `Generate an image`、`Enhance Image Free`、`Get Started` 及其他指向本页 Hero、上传区、工作台或功能操作区的同类页头 CTA；任何视口或登录状态均不得渲染该按钮或遗留空占位。将全站所有页头中的 `Workspace` 统一为黑色主按钮：背景 `rgb(0, 0, 0)`、文字 `rgb(255, 255, 255)`、无边框、`40px` 高、`8px 16px` 内边距、`9999px` 圆角，并统一 hover、focus-visible 和 active 状态。未登录桌面端右侧只保留 `Workspace`、`Sign in`；登录桌面端只保留 `Workspace`、头像或账户菜单。移动端统一显示 Logo、`Sign in` 或账户入口及菜单按钮；展开菜单后将全宽黑色 `Workspace` 固定放在菜单顶部，其余五个导航分类按桌面端相同顺序显示。
- 验收标准：在 `1440px`、`1280px`、`1024px` 和 `390px` 视口逐一比较全部非首页、非 Workspace 的公开页面；相同视口和登录状态下，页头除当前分类选中状态外必须具有相同的 DOM 控件结构、外层高度、Logo 显示规则、导航顺序与间距、字体样式、颜色、边框、圆角、阴影、右侧控件布局和移动端菜单结构。不得再出现 Image Enhancer 与其他页面使用不同菜单样式的情况。全部 32 个功能页的页头均不再出现当前功能专属 CTA；相关文案只可保留在页面正文中。全站登录和未登录状态下的 Workspace 均为黑底白字、无边框、40px 高和胶囊圆角；移动端菜单内为相同配色的全宽按钮。页头没有空白占位、控件重叠、横向溢出或异常对齐；所有菜单、Workspace、`Sign in`、头像及账户控件均可用鼠标、触摸和键盘操作，具有正确的可访问名称、展开状态和清晰焦点。首页和登录后的 Workspace 页面除 Workspace 按钮统一为黑色外，其余页头结构与样式保持现状。
- 不要修改：不要用某个异常页面的页面级 CSS 覆盖其他页面；不要删除或改写页面正文中的生成、上传、编辑、下载、重新开始或滚动到 Hero 的按钮；除指定视觉样式外，不要修改 Workspace 的文案、位置、跳转和登录行为；不要修改 `Sign in`、头像、账户菜单、导航分类内容与顺序、登录规则、功能参数、工具行为、URL、Title、Meta Description、Canonical 或页面 H1；不要用图标按钮、浮动按钮或移动端菜单项重新创建已删除的功能快捷入口。

### 在 Blur Background 首屏功能模块加入 Before/After 对比案例

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/ai-blur-background/` 的首屏 Hero 功能模块及其下方现有 Before/After 案例区；覆盖桌面端、平板端和移动端
- 当前问题与线上证据：当前首屏只显示标题、说明和图片上传操作区，没有任何处理前后效果示例。现有 `Woman crossing a city street` Before/After 滑动对比位于下一屏的 `background-blur-proof` 内容区，用户进入页面后无法在首屏同时确认输入方式和背景虚化效果。
- 修改要求：将页面现有 `Woman crossing a city street` Before/After 滑动对比案例复用到首屏功能模块，不要另外复制一套相同案例。桌面端和宽屏平板端将首屏功能区域改为双栏布局：左侧保留现有上传与操作区，右侧显示完整对比组件；窄屏平板端和移动端改为纵向排列，上传与操作区在前，对比组件紧随其后。迁移后删除下一屏中重复的同一组对比组件及其遗留空白，但保留该内容区其余不重复的标题、说明和案例。对比组件必须保留清晰可见的 `Before`、`After` 标识，支持鼠标拖动、触摸拖动和键盘调节，滑杆具有描述其用途的可访问名称。为两张案例图片提供与实际显示尺寸匹配的响应式资源、明确的宽高属性和稳定的宽高比；首屏可见且可能成为 LCP 的案例图片不得延迟加载。
- 验收标准：在 `1440px`、`1280px`、`1024px` 和 `390px` 视口首次打开页面且不进行任何交互时，首屏功能模块内均能同时看到上传入口和至少一部分足以辨认处理差异的 Before/After 对比案例；桌面端为左右双栏，移动端为上下排列，没有遮挡、裁切、异常空白或横向滚动。拖动滑杆时原图和背景虚化结果切换流畅，鼠标、触摸、Tab 与方向键均可操作，读屏可识别其名称和当前值。页面中不再重复展示同一组 `Woman crossing a city street` 对比素材；图片加载前后布局不跳动，首屏案例不因懒加载而出现明显延迟。
- 不要修改：不要改变图片上传、文件校验、任务提交、登录判断、处理参数、结果下载或错误提示逻辑；不要替换现有对比案例图片或虚构新的处理效果；不要修改页面 URL、Title、Meta Description、Canonical、H1、正文文案、导航、页脚或其他功能模块；不要为了容纳案例而缩小交互控件至难以点击，或隐藏现有上传说明和隐私提示。

### 将 AI Edit 首屏静态示例改为可拖动的 Before/After 组件

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/ai-edit/` 首屏编辑器右侧的 `Example` 卡片；覆盖桌面端、平板端和移动端
- 当前问题与线上证据：`Example` 卡片当前只渲染一张 `https://imagehub.ai/images/ai-photo-editor/hero-section.webp`，图片本身包含 `Before`、`After`、中间分隔线和手柄图形。页面中不存在 `input[type="range"]` 或 `role="slider"`，用户看到的分隔线无法拖动，也不能逐步查看编辑前后的完整画面。
- 修改要求：停止在该卡片中显示合成图片 `hero-section.webp`，改用制作该示例时对应的完整原图和完整编辑结果图作为两个独立图片层，二者必须具有相同像素尺寸、画面构图、主体位置和宽高比；不得把当前合成图左右裁切后冒充两张完整素材。底层显示完整 Before 图，上层显示完整 After 图，并根据滑杆百分比从左到右裁切上层；初始位置固定为 `50%`。组件内以独立 HTML 文本显示 `Before` 和 `After`，在分界线上显示可拖动手柄。滑杆使用原生 `input[type="range"]` 或完整等价的 `role="slider"` 语义，可访问名称固定为 `Compare before and after AI photo edit`，取值范围为 0–100，并持续暴露当前百分比。鼠标拖动、点击轨道、单指触摸拖动均必须实时更新画面；键盘左右方向键每次移动 1%，Home 移到 0%，End 移到 100%。拖动只改变对比位置，不触发图片拖拽、页面横向滚动、文字选择或页面导航。为两张图片声明正确宽高和稳定宽高比；作为首屏内容，两张图片均不得延迟加载。若项目中不存在制作 `hero-section.webp` 所用的两张独立完整素材，停止此任务并报告缺少原图和结果图，不得生成、补画、推测或使用无关图片替代。
- 验收标准：首次进入页面时，`Example` 卡片显示同一示例的完整 Before 和完整 After 画面，分界线位于 50%；移动滑杆至 0% 时完整显示 Before，移动至 100% 时完整显示 After，中间任意位置均保持两层像素级对齐，没有缩放差异、跳动、空白或接缝错位。鼠标、触摸、Tab、左右方向键、Home 和 End 操作均符合指定行为；读屏可识别名称、最小值、最大值和当前值。`1440px`、`1280px`、`1024px` 和 `390px` 视口下组件完整位于卡片内，不遮挡左侧上传与提示词区域，不产生横向滚动；移动端触摸拖动滑杆时页面仍可正常纵向滚动。页面源码不再把 `hero-section.webp` 作为该 Example 卡片的展示内容，也不存在把静态手柄图形覆盖在单张合成图上的伪交互实现。
- 不要修改：不要改变示例人物、相机、编辑效果或视觉风格，不要生成新的案例效果；不要修改左侧上传、提示词、示例提示按钮、Generate、任务提交、登录、结果或下载逻辑；不要改变 `Example` 文案、页面 URL、Title、Meta Description、Canonical、H1、正文、Gallery、导航或页脚；不要添加自动播放、循环动画、闪烁切换或必须登录后才能使用的对比功能。

### 消除全站 Before/After 滑动组件的拖拽卡顿

- 优先级：`P1`
- 页面或界面：当前使用共享 Before/After 组件的 15 个公开页面：`https://imagehub.ai/`、`https://imagehub.ai/ai-background-changer/`、`https://imagehub.ai/ai-remove/`、`https://imagehub.ai/ai-unblur-images/`、`https://imagehub.ai/ai-image-upscaler/`、`https://imagehub.ai/ai-object-remover/`、`https://imagehub.ai/ai-open-eyes/`、`https://imagehub.ai/ai-photo-restoration/`、`https://imagehub.ai/ai-backgrounds-generate/`、`https://imagehub.ai/ai-beauty/`、`https://imagehub.ai/ai-blur-background/`、`https://imagehub.ai/ai-body-editor/`、`https://imagehub.ai/ai-denoise/`、`https://imagehub.ai/ai-shadow-generator/` 和 `https://imagehub.ai/free-ai-image-enhancer/`；同时覆盖本文件要求在 `https://imagehub.ai/ai-edit/` 新增的组件及以后复用该共享组件的页面
- 当前问题与线上证据：共享组件在正常 `prefers-reduced-motion: no-preference` 环境下，对裁切层 `clip-path`、分隔线 `left` 及相关状态持续应用 `120ms ease-out` 过渡，拖动过程中每次新位置都会重新开始动画，导致画面和手柄追赶指针。组件同时注册 `pointerdown`/`pointermove` 和 `mousedown`/`mousemove` 两套鼠标路径，一次桌面拖动会产生重复处理；每个组件还各自向 `window` 注册 `mousemove` 和 `mouseup`。首页有 10 个组件、Photo Restoration 有 9 个组件，即使只拖动一个滑杆，也会执行所有实例的全局监听回调。每次移动还会调用 `getBoundingClientRect()`，随后立即写入 CSS 自定义属性、`aria-valuenow` 和数据属性，没有通过 `requestAnimationFrame` 合并同一帧内的事件。大尺寸图片上的连续 `clip-path` 重绘进一步放大卡顿。
- 修改要求：所有上述页面必须改用同一套修复后的共享组件行为，不得保留页面级旧实现。只使用 Pointer Events 处理鼠标、触摸和触控笔：在 `pointerdown` 时记录当前组件边界、设置拖动状态并调用 `setPointerCapture(pointerId)`；在组件捕获的 `pointermove`、`pointerup`、`pointercancel` 和 `lostpointercapture` 中完成拖动，不再额外注册 `mousedown`、`mousemove`、`mouseup` 或每个实例独立的 `window` 移动监听器。`pointermove` 只保存最新指针横坐标；当本帧尚无待执行任务时安排一次 `requestAnimationFrame`，在该帧中根据缓存边界计算百分比并一次性更新组件。不得在每次 `pointermove` 中调用 `getBoundingClientRect()`；组件边界只在拖动开始时读取，并在 `ResizeObserver` 或窗口尺寸变化后失效重算。拖动和键盘直接操作期间，裁切层、分隔线与手柄的位置变化必须使用 `transition: none`，不得继续对 `clip-path`、`left`、`transform` 或其他位置属性应用 120ms 追随动画；颜色、阴影等非位置反馈可以保留不超过 120ms 的过渡。分隔线不得在拖动时通过 `left` 触发布局，改为基于缓存像素位置的 `translate3d`；裁切层继续使用同一个百分比状态更新 `clip-path`。只在实际拖动的当前组件上临时启用 `will-change: clip-path, transform`，结束拖动后立即移除，其他未操作组件不得长期创建合成层。每个渲染帧最多写入一次裁切位置、一次分隔线变换和一次 `aria-valuenow`；百分比没有变化时不得重复写入。键盘继续支持左右方向键、Home 和 End，并与指针路径调用同一个帧更新函数。页面切换、局部导航或组件卸载时清理 `ResizeObserver`、未执行的动画帧和全部监听器。
- 验收标准：在 Chrome DevTools Performance 中分别对首页、Photo Restoration、Blur Background、Image Enhancer、Open Eyes 和新增 AI Edit 组件进行至少 5 秒连续左右拖动；指针移动期间裁切边界和手柄在下一动画帧内到达最新位置，松手后不存在持续约 120ms 的追赶、回弹或残余移动。一次物理鼠标移动只进入一条 Pointer Events 更新路径；同一组件每个动画帧最多执行一次位置更新，`pointermove` 调用栈中不出现 `getBoundingClientRect()`，也不存在每个组件独立的 `window mousemove`/`mouseup` 监听器。性能记录中不得出现由滑杆处理函数造成的超过 50ms Long Task；快速往返拖动不丢失 Pointer Capture，不越过 0–100 范围，不出现图片空白、裁切裂缝、分隔线与裁切边界错位或页面横向滚动。使用鼠标、触摸、触控笔、Tab、左右方向键、Home 和 End 均可连续操作；`aria-valuenow` 与可见位置一致。逐一抽查列出的 15 个现有页面及 AI Edit 新组件，交互手感和行为一致；`prefers-reduced-motion: reduce` 下不新增任何位置动画。
- 不要修改：不要降低图片分辨率、替换 Before/After 素材、删除对比组件、减少页面案例数量或用自动播放掩盖拖拽延迟；不要牺牲键盘、触摸、触控笔或读屏支持；不要修改对比组件以外的页面布局、文案、功能流程、URL、Title、Meta Description、Canonical 或 H1；不要永久对页面全部图片或全部滑杆启用 `will-change`，不要通过降低事件采样到明显跳跃的固定间隔来伪装流畅。

### 修复 AI Edit 页面错误的 Privacy 和 Terms 链接

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/ai-edit/` 的上传与数据处理说明区域
- 当前问题与线上证据：页面中的 `Privacy Policy` 当前指向 `/privacy-policy/`，该地址返回 301 并跳转到首页；`Terms of Use` 当前指向 `/terms-of-use/`，该地址返回 404。用户和搜索引擎均无法通过这两个上下文链接进入实际法律页面。
- 修改要求：将 `Privacy Policy` 的链接目标精确改为 `/privacy/`，将 `Terms of Use` 的链接目标精确改为 `/terms/`。保留当前可见链接文案、所在句子、打开方式和视觉样式。使用站内根相对路径，不新增中间跳转。
- 验收标准：在 `https://imagehub.ai/ai-edit/` 点击 `Privacy Policy` 后直接打开 `https://imagehub.ai/privacy/`，点击 `Terms of Use` 后直接打开 `https://imagehub.ai/terms/`；两个目标 URL 均返回 200，页面源码中不再包含 `/privacy-policy/` 或 `/terms-of-use/`；重新抓取站点地图中的全部页面，不存在指向这两个旧地址的内部链接。
- 不要修改：不要改写 Privacy、Terms 或 AI Edit 的正文，不要把链接改为首页、锚点或外部地址；不要修改法律页面 URL、Title、Meta Description、Canonical、H1、页脚链接或站点地图。

### 建立完整且统一的 ImageHub 品牌实体

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/`、`https://imagehub.ai/about/`，以及站点地图中所有输出 `Organization`、`WebSite`、`WebPage`、`WebApplication` 或其他 JSON-LD 的公开页面
- 当前问题与线上证据：首页的 `Organization` 目前只有 `name: ImageHub` 和 `url`；About 页面虽然公开显示运营主体 `QUEST LABS LIMITED`、业务地址和联系邮箱，但没有 `AboutPage` 或组织实体结构化数据。部分功能页把组织和网站 URL 写为 `https://imagehub.ai`，首页则使用 `https://imagehub.ai/`。生成式搜索无法从机器可读数据中稳定确认 ImageHub 品牌、`imagehub.ai` 域名和 QUEST LABS LIMITED 运营主体属于同一实体。
- 修改要求：全站只使用一个组织实体标识 `https://imagehub.ai/#organization` 和一个网站实体标识 `https://imagehub.ai/#website`。所有 JSON-LD 中的组织实体必须使用相同字段：`@type` 为 `Organization`，`@id` 为 `https://imagehub.ai/#organization`，`name` 为 `ImageHub`，`legalName` 为 `QUEST LABS LIMITED`，`url` 为 `https://imagehub.ai/`，`email` 为 `support@imagehub.ai`；`logo` 使用 `ImageObject`，`@id` 为 `https://imagehub.ai/#logo`，`url` 与 `contentUrl` 均为 `https://imagehub.ai/images/imagehub-logo.png`，`width` 和 `height` 均为 `512`；`address` 使用 `PostalAddress`，`streetAddress` 为 `RM 1605 HO KING COMM CTR, 2-16 FA YUEN ST`，`addressLocality` 为 `MONG KOK`，`addressRegion` 为 `HONG KONG`，`addressCountry` 为 `HK`；`contactPoint` 使用 `ContactPoint`，`contactType` 为 `customer support`，`email` 为 `support@imagehub.ai`。网站实体必须使用 `https://imagehub.ai/#website`，其 `publisher` 引用该组织 `@id`。About 页面增加 `AboutPage`，`@id` 为 `https://imagehub.ai/about/#webpage`，`url` 为 `https://imagehub.ai/about/`，`name` 为 `About ImageHub`，`isPartOf` 引用网站实体，`about` 和 `mainEntity` 均引用组织实体。全部功能页的 `WebPage` 和 `WebApplication` 通过 `publisher`、`provider` 或现有对应关系引用同一个组织实体；本文件另行要求为 AI Background Generator 和 AI Open Eyes 新增的 JSON-LD 也必须使用这套实体。
- 验收标准：首页、About 和全部含 JSON-LD 的功能页均只引用上述两个稳定站点级 `@id`；不存在第二个 ImageHub `Organization`、不同组织 URL、无尾斜杠站点 URL或互相冲突的 Logo、邮箱和地址。About 页面可被识别为 `AboutPage`，且组织实体中的运营主体、地址、邮箱和页面可见内容逐字一致。所有 JSON-LD 均可解析，Schema.org Validator 不报告语法错误或无效类型；查看任一功能页的实体图时，`WebApplication`、`WebPage`、`WebSite`、`Organization` 和 About 页面能够通过 `@id` 连成同一实体关系。
- 不要修改：不要新增 `sameAs`、成立年份、创始人、员工、总部、奖项、认证、评分、客户数量或未公开的公司资料；不要创建或链接任何未经用户确认的社交账号、公司资料页或第三方目录；不要改写 About、Privacy、Terms 的可见正文、运营主体、地址或邮箱，不要更换现有 Logo 文件。

### 删除 Background Remover 无依据的三秒处理承诺

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/ai-background-remover/` 的步骤区、目录、结构化数据及任何复用该标题的位置
- 当前问题与线上证据：页面步骤标题当前为 `How to Extract Subjects in 3 Seconds.`，但页面没有公开测试方法、样本、文件条件、网络环境或处理时间数据，无法支持固定三秒完成的结果承诺。
- 修改要求：将 `How to Extract Subjects in 3 Seconds.` 精确替换为 `How to Remove an Image Background in Three Steps.`，并同步更新目录、锚点可访问名称、`HowTo` JSON-LD 的 `name` 及同页任何逐字复用该标题的位置。保留当前三个步骤及其顺序，不新增任何秒数、平均速度、最快速度或即时完成承诺。
- 验收标准：页面可见步骤标题和 `HowTo` 结构化数据名称均逐字为 `How to Remove an Image Background in Three Steps.`；页面源码、Meta、Open Graph、Twitter 和 JSON-LD 中不再出现 `3 Seconds`、`three seconds` 或语义等价的固定处理时间承诺；三个现有步骤、上传入口和下载流程保持完整。
- 不要修改：不要改变实际处理性能、队列、模型、上传限制、输出格式、步骤数量或功能流程；不要替换为 `instant`、`immediate`、`real-time` 或其他无法公开验证的速度承诺；不要改写页面其他已经限定适用范围的功能说明。

### 移除关闭状态账户弹窗对页面语义结构的污染

- 优先级：`P2`
- 页面或界面：站点地图 `https://imagehub.ai/sitemap.xml` 中全部公开页面的未登录初始 HTML、登录弹窗、邮箱验证码步骤、内容安全确认弹窗和账户 Profile 弹窗
- 当前问题与线上证据：未打开任何账户界面时，每个公开页面的 DOM 和标题结构仍包含 `Profile`、`Welcome to ImageHub`、`Check email for the code`、`Quick check before we start` 等弹窗 H2 及完整弹窗内容。虽然部分祖先节点通过 CSS 不显示，这些与当前页面主题无关的重复文本仍进入初始文档和通用内容提取结果，稀释功能页的标题与答案结构。
- 修改要求：公开页面首次返回和完成 hydration 后，在用户尚未触发对应界面时，不得创建 Profile、登录、验证码或内容安全确认弹窗的完整 DOM、标题和正文。用户点击现有触发控件后再挂载对应弹窗；弹窗打开时保留当前可见文案和 H2 标题，通过 `dialog` 或等价对话框语义、`aria-modal="true"` 与 `aria-labelledby` 建立正确可访问名称，将焦点移入弹窗并限制在弹窗内。切换到验证码或内容安全确认步骤时，只挂载当前步骤，不得同时保留其他隐藏步骤的 H2。关闭后卸载弹窗内容并将焦点返回原触发控件。已登录用户的 Profile 内容同样只在打开账户入口后挂载。
- 验收标准：未登录直接请求并渲染站点地图中的任一公开页面，未操作时的 HTML 和 DOM 标题列表中均不存在 `Profile`、`Welcome to ImageHub`、`Check email for the code`、`Quick check before we start` 或其他关闭弹窗标题；页面 H2 只描述当前页面正文。打开登录、验证码、安全确认和 Profile 后，对应 H2 仅出现一次，读屏能够朗读弹窗名称，Tab 不会离开弹窗；关闭后相关标题从 DOM 移除且焦点返回触发位置。登录、验证码、安全确认和账户操作结果与修改前一致，无闪烁、布局跳动或首次点击失效。
- 不要修改：不要删除弹窗可见标题、说明、输入项、安全确认、错误提示或关闭按钮；不要将打开状态弹窗标题降级为无语义文本，不要破坏认证、验证码、账户资料、退出登录、内容政策检查或焦点管理；不要为了隐藏内容而只使用负坐标、透明度或视觉裁切继续把完整弹窗留在初始语义树中。

### 为 Sitemap 和页面实体增加真实的新鲜度信号

- 优先级：`P2`
- 页面或界面：`https://imagehub.ai/sitemap.xml` 中全部 37 个公开 URL、这些页面的页面级 JSON-LD，以及 `https://imagehub.ai/changelog/`
- 当前问题与线上证据：Sitemap 的全部 URL 当前只有 `<loc>`，没有 `<lastmod>`；抽查的 `CollectionPage`、`WebPage`、`WebApplication` 和其他页面级 JSON-LD 也没有 `dateModified`。Changelog 已使用带有效 `datetime` 的 `<time>`，但 Sitemap 和实体图没有提供与内容更新一致的新鲜度信息。
- 修改要求：为 Sitemap 中每个 URL输出 ISO 8601 `YYYY-MM-DD` 格式的 `<lastmod>`，日期必须来自该页面正文、元数据、功能说明、结构化数据或用户可见界面最后一次实际发生内容变化的日期；仅发布、重建、缓存刷新、依赖升级或部署而页面内容未变化时，不得更新该日期。为每个现有或本批次新增的页面级 `WebPage`、`CollectionPage`、`AboutPage`、`FAQPage` 和 `HowTo` 实体加入与对应页面 `<lastmod>` 一致的 `dateModified`。为 Privacy 和 Terms 使用其可见 `Effective date` 作为首次发布日期，并在正文实际更新时同步修改可见日期、Sitemap 和结构化数据。为 Changelog 增加 `CollectionPage` 页面实体，`@id` 为 `https://imagehub.ai/changelog/#webpage`，`url` 为 `https://imagehub.ai/changelog/`，`name` 为 `Changelog`，`isPartOf` 引用网站实体，`dateModified` 等于最新一条真实更新记录的日期；保留每条记录现有 `<time datetime="YYYY-MM-DD">`。
- 验收标准：Sitemap 中 37 个 `<url>` 均且仅有一个有效 `<lastmod>`；日期不晚于当前日期，不早于页面首次上线日期，同一页面的 Sitemap `lastmod` 与页面级 JSON-LD `dateModified` 一致。只修改一个页面并重新构建时，仅该页面及因新增记录而实际变化的 Changelog、首页或目录页更新日期，其他未变页面日期保持不变。Privacy、Terms 和 Changelog 的可见日期、`datetime`、Sitemap 和 JSON-LD 相互一致；所有日期均可从实际内容变更记录复现，不使用服务器文件时间或统一部署时间批量覆盖。
- 不要修改：不要在每次构建或部署时把全部页面日期更新为当天，不要填写未来日期、虚构发布日期或使用图片、脚本、样式和依赖文件的修改时间代替页面内容时间；不要删除 Changelog 历史记录或改变其时间顺序。

### 统一全站工具事实摘要和免费使用规则

- 优先级：`P1`
- 页面或界面：全部 32 个独立功能落地页、首页 `https://imagehub.ai/` 的工具集合与 Workspace 说明、登录弹窗、内容安全确认界面、FAQ、CTA 辅助文案、功能徽章、页脚、Meta Description、Open Graph、Twitter 和对应结构化数据
- 当前问题与线上证据：不同页面分别使用 `Unlimited runs`、`Unlimited creativity`、`No daily cap`、`No quota wall`、`there is no limit on tries`、`as many tries as it takes`、`Create without limits` 等表述，与用户确认的全站共享免费额度不一致。各功能页对输入、输出、登录、水印、免费额度和并发任务的事实呈现也不统一，生成式搜索可能从不同页面提取出互相冲突的产品规则。
- 修改要求：全站使用同一产品规则：全部功能共享每个用户每日 3 次免费任务额度；所有 ImageHub 工具的成功输出均不添加 ImageHub 水印；每个用户同一时间只能处理 1 个任务。删除或改写所有暗示无限次数、没有每日限制、没有额度限制或可同时处理多个任务的可见文案、隐藏弹窗文案、Meta、社交摘要、FAQ 和 JSON-LD。每个独立功能落地页在首个操作区附近增加或统一一个可见标题为 `Tool facts` 的事实摘要，固定包含以下字段和精确英文规则：`Free usage` — `3 free tasks per user per day, shared across all ImageHub tools.`；`Watermark` — `No ImageHub watermark.`；`Concurrent tasks` — `One task can be processed at a time.`；`Account` — `No account is required on this individual tool page.`。同时加入 `Input` 和 `Output`：`Input` 必须逐字列出该页面实际文件选择器、前端校验和服务端校验共同接受的文件格式及所需图片数量；纯文本生成工具写 `Text prompt`；需要图片和提示词的工具同时写明两者；需要多张图片的工具写明实际数量和各图片用途。`Output` 必须写实际可下载文件类型；仅在输出格式固定且已经由下载结果验证时写具体扩展名，否则统一写 `Downloadable image`。首页 Workspace 的对应说明使用：`3 free tasks per user per day, shared across all ImageHub tools. Sign in to start tasks from the homepage workspace. One task can be processed at a time. Results have no ImageHub watermark.` 登录弹窗中原 `Create without limits` 改为 `Create with ImageHub`。已有额度计数、每日重置、用户识别、并发控制和水印逻辑作为事实来源；本任务不得另行定义识别方式、重置时区或规避规则。
- 验收标准：重新抓取站点地图全部页面并检查登录相关界面，不再出现 `unlimited`、`no limits`、`no daily cap`、`no quota wall`、`there is no limit`、`as many tries as it takes` 或语义等价的无限使用承诺。32 个独立功能页均有一个 `Tool facts` 摘要，四项固定规则逐字一致，`Input` 与实际上传控件及校验一致，`Output` 与实际下载结果一致。首页 Workspace 逐字显示指定说明，登录弹窗标题逐字为 `Create with ImageHub`。同一用户在任意工具组合中成功开始的前三个免费任务共同消耗当日 3 次额度，第四个任务按现有额度规则被阻止；已有未完成任务时不能同时开始第二个任务；成功输出不包含 ImageHub 水印。页面可见摘要、FAQ、Meta、Open Graph、Twitter 和 JSON-LD 不存在互相冲突的额度、水印、并发或登录说明。
- 不要修改：不要把额度改成每个工具各 3 次，不要把失败、取消、政策拦截或重复请求是否计入额度另作推断；不要改变现有用户识别方式、每日重置时区、额度扣减时点、错误文案、排队机制、登录要求或免费任务的保存与删除规则；不要承诺永久免费、无限使用、固定处理速度、固定输出尺寸或所有工具都输出同一格式；不要为输出添加水印，不要要求用户登录后才能使用独立功能落地页。

### 在 Workspace 免费额度用完时显示明确提示弹窗

- 优先级：`P1`
- 页面或界面：首页登录后的集合 Workspace 和登录后的完整 Workspace；覆盖桌面端与移动端的所有任务提交入口
- 当前问题与线上证据：用户确认全部 ImageHub 功能共享每个用户每日 3 次免费任务额度，但 Workspace 在额度用完后缺少明确弹窗，用户无法立即理解任务不能继续提交的原因以及何时可以再次免费使用。
- 修改要求：同一用户当天已经消耗完共享的 3 次免费任务额度后，在 Workspace 再次点击任一任务提交按钮时阻止提交并即时挂载模态弹窗。弹窗标题固定为 `Daily free limit reached`，正文固定为 `You’ve used your 3 free tasks for today. Please come back tomorrow.`，主按钮固定为 `Got it`，同时提供可访问名称为 `Close` 的关闭按钮。弹窗只能在用户尝试发起超出额度的任务时出现；第三个符合现有额度扣减规则的任务必须正常提交并完整显示结果，不得在结果上自动覆盖弹窗。提交前读取的剩余额度为 0 时直接显示弹窗；如果本地状态尚未更新但服务端返回当日免费额度已用完，也必须显示同一弹窗。超额尝试不得创建任务、上传新的任务数据、调用生成或编辑服务、加入队列、重复扣减额度或清空用户已经填写的提示词、选择的工具、模型、参数和已添加的参考图片。关闭弹窗后保留当前 Workspace 输入状态；用户当天再次尝试提交时重新显示同一提示，现有每日重置生效后下一次任务恢复正常提交。
- 验收标准：使用当天剩余 1 次免费额度的测试用户提交任务时，第三个免费任务正常创建、处理并显示结果；随后在首页集合 Workspace 和完整 Workspace 分别尝试第四个任务，均不创建任务并显示指定弹窗，标题、正文和 `Got it` 文案逐字一致。直接以剩余 0 次状态进入 Workspace 时不自动打断浏览，只有点击提交后才显示；模拟提交前额度状态过期并由服务端返回限额时也显示同一弹窗。超额尝试前后，提示词、工具、模型、参数和参考图片保持不变，额度计数不再增加。弹窗在 `1440px`、`1280px`、`1024px` 和 `390px` 视口完整可见，没有溢出；打开后焦点进入弹窗并停留其中，读屏识别为模态对话框并朗读标题与正文，`Got it`、`Close` 和 Escape 均可关闭，关闭后焦点返回原提交按钮。按现有每日重置规则进入下一日后，首次任务不再出现限额弹窗并可正常提交。
- 不要修改：不要改变每日 3 次额度、跨工具共享方式、用户识别、额度扣减条件、每日重置时区、并发任务限制、登录要求、免费任务保存与删除规则或无水印规则；不要在第三个任务完成时自动弹窗，不要跳转到定价、支付、登录或外部页面，不要新增购买、升级、倒计时、具体重置时刻或营销文案；不要用浏览器提示框替代站内模态弹窗，不要让限额弹窗覆盖其他非额度错误或改变已有错误处理优先级。

### 统一公开页面的尾斜杠 URL 并实施 301 跳转

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/sitemap.xml` 中除首页外的全部 36 个公开页面，以及这些页面对应的不带尾斜杠 URL
- 当前问题与线上证据：36 个公开内页中只有 16 个不带尾斜杠的版本会 301 到带尾斜杠地址，其余 20 个不带尾斜杠地址仍返回 200，包括 `/ai-change-haircut`、`/ai-multiple-face-swap`、`/ai-remove`、`/ai-unblur-images`、`/free-ai-art-generator-from-image`、`/ai-open-eyes`、`/ai-edit`、`/ai-backgrounds-generate`、`/ai-beauty`、`/ai-blur-background`、`/ai-body-editor`、`/ai-denoise`、`/ai-headshot-generator`、`/ai-product-photography`、`/ai-shadow-generator`、`/free-ai-image-enhancer`、`/about`、`/privacy`、`/terms` 和 `/changelog`。同一内容因此可通过两种路径直接返回 200，增加重复抓取和规范化信号分散风险。
- 修改要求：以站点地图和现有 Canonical 使用的带尾斜杠 URL 为唯一规范地址。为全部 36 个公开内页统一配置服务端永久重定向：请求不带尾斜杠的页面路径时，只执行一次 301 并跳转到同路径的带尾斜杠地址；已有查询参数必须原样保留。带尾斜杠的规范页面继续直接返回 200。规则只作用于公开 HTML 页面，不得给静态资源、API、认证回调或带文件扩展名的请求追加斜杠。
- 验收标准：逐一请求站点地图中除首页外的 36 个 URL 的无尾斜杠版本，全部返回 301，`Location` 精确指向同源、同路径、带尾斜杠的 Canonical URL；跟随跳转后只经过一次重定向并返回 200。带尾斜杠页面直接返回 200，不形成循环或多跳。带查询参数抽查时参数完整保留；图片、脚本、样式、字体、API 和登录流程均不受影响。站点地图、Canonical、Open Graph URL、内部导航和面包屑继续只输出带尾斜杠地址。
- 不要修改：不要把规范地址改成无尾斜杠版本，不要使用 302、Meta Refresh 或客户端 JavaScript 跳转；不要重命名页面、改变页面内容、修改路由层级或给文件和 API 路径强制追加斜杠。

### 为 AI Background Generator 和 AI Open Eyes 补齐结构化数据

- 优先级：`P2`
- 页面或界面：`https://imagehub.ai/ai-backgrounds-generate/` 和 `https://imagehub.ai/ai-open-eyes/`
- 当前问题与线上证据：这两个功能页当前没有任何 `application/ld+json` 结构化数据，而其他同类功能页已经提供 `Organization`、`WebSite`、`WebPage`、`WebApplication`、`HowTo`、`FAQPage` 和 `BreadcrumbList`。搜索引擎无法从这两个页面获得与站内同类页面一致的机器可读实体和页面结构信息。
- 修改要求：在两个页面分别输出一个合法的 JSON-LD 图，并沿用其他功能页已经使用的站点级 `Organization` 和 `WebSite` 实体及其稳定 `@id`。每页加入与该页 URL、Title、Meta Description 和可见 H1 一致的 `WebPage`，加入表示该浏览器工具的 `WebApplication`，并加入从首页到当前页面的 `BreadcrumbList`。两个页面均已公开显示步骤与 FAQ，因此同时加入 `HowTo` 和 `FAQPage`；`HowTo` 的步骤名称、顺序和说明必须逐字对应页面可见步骤，`FAQPage` 的每个问题和答案必须逐字对应页面可见 FAQ。所有页面级实体使用该页带尾斜杠 Canonical 组成稳定且唯一的 `@id`，实体之间通过 `@id` 引用连接，不复制或创建第二套冲突的站点实体。
- 验收标准：两个页面各自存在且只存在一套合并后的 JSON-LD 图；JSON 可解析，没有重复键、空字段、占位符或无效 URL。Schema.org Validator 不报告语法错误；Google Rich Results Test 能识别页面实际支持的类型且不报告阻断性错误。`WebPage`、`WebApplication`、`BreadcrumbList`、`HowTo` 和 `FAQPage` 中的名称、URL、步骤及问答均与当前可见页面一致；修改页面可见步骤或 FAQ 后，对应 JSON-LD 必须同步更新。
- 不要修改：不要新增评分、评价、价格、库存、客户数量、成功率、认证或其他页面没有公开显示的数据；不要为了匹配结构化数据而改写页面正文；不要在 Privacy、Terms、About、Changelog 或其他页面批量复制功能页 Schema；不要创建与现有 `Organization` 或 `WebSite` 冲突的新实体。

### 为全站内容图片补齐尺寸并规范加载优先级

- 优先级：`P2`
- 页面或界面：`https://imagehub.ai/sitemap.xml` 中全部公开页面的正文图片、Hero 图片、Before/After 对比图、案例图和步骤图；不包含仅由 CSS 绘制的装饰图形、SVG 图标或账户头像
- 当前问题与线上证据：公开页面中大量 `<img>` 没有同时声明 `width` 和 `height`。抽查中，Blur Background 20 张图片有 16 张缺少尺寸，AI Background Generator 23 张有 21 张，Image Generator 18 张有 14 张，Image Enhancer 20 张有 18 张。浏览器在图片加载前无法稳定预留空间，增加累计布局偏移风险；部分首屏外图片也没有使用延迟加载。
- 修改要求：逐页检查站点地图中的全部公开页面，为每个正文 `<img>` 同时提供数值型 `width` 和 `height`，其比例必须与实际源图一致；CSS 保持响应式显示，使用 `max-width: 100%` 和自动高度或现有等价规则，不得拉伸图片。使用 `<picture>` 或 `srcset` 的图片仍必须在最终 `<img>` 上声明宽高。每页首屏可见且实际承担主要视觉内容的图片使用 `loading="eager"`；每页只有主要 LCP 候选图可以增加 `fetchpriority="high"`，其余图片不得使用高优先级。首屏以下的正文、案例和步骤图片统一使用 `loading="lazy"` 与 `decoding="async"`。Before/After 组件的两层图片共享完全相同的显示宽高和宽高比，加载前即预留完整组件空间。
- 验收标准：重新抓取站点地图全部页面，范围内每个 `<img>` 都同时具有有效的正整数 `width` 和 `height`，且与实际资源宽高比一致；没有因错误尺寸产生压缩、拉伸、裁切变化或组件错位。滚动前不请求首屏以下的懒加载图片；首屏主要图片不会因为错误懒加载而延迟出现；每页最多一个 `fetchpriority="high"`。在 `1440px`、`1280px`、`1024px` 和 `390px` 视口刷新并滚动页面，图片加载前后正文、按钮、对比滑杆和页脚不发生可见跳动，页面没有横向溢出。
- 不要修改：不要更换图片内容、重新生成处理效果、删除必要图片、降低可见清晰度或改变现有裁切构图；不要给所有图片统一设置相同宽高，不要给所有图片使用 eager 或高优先级加载；不要修改上传预览、用户生成结果、头像、图标或运行时任务图片的业务逻辑。

### 压缩过长的 Title 和 Meta Description

- 优先级：`P3`
- 页面或界面：`https://imagehub.ai/ai-background-remover/`、`https://imagehub.ai/ai-beauty/`、`https://imagehub.ai/ai-body-editor/`、`https://imagehub.ai/ai-image-extender/`、`https://imagehub.ai/free-ai-image-generator/` 和 `https://imagehub.ai/terms/`
- 当前问题与线上证据：上述页面的 Meta Description 当前为 162–175 个字符，容易在常见搜索结果宽度中被截断；AI Body Editor 的 Title 为 61 个字符，也超过站内多数功能页的标题长度。页面关键词和搜索意图已经明确，不需要用重复修饰词占用摘要空间。
- 修改要求：只替换以下指定字段，文案必须逐字一致。`/ai-background-remover/` 的 Meta Description 改为 `Remove image backgrounds online for free. Upload JPG, PNG, or WebP and download a transparent PNG with no signup, watermark, or manual masking.`；`/ai-beauty/` 的 Meta Description 改为 `Describe a beauty look, upload one photo, and download an HD result. Create natural or polished edits online for free, with no login or watermark.`；`/ai-body-editor/` 的 Title 改为 `Free AI Body Editor – Reshape Photos Online | ImageHub`，Meta Description 改为 `Upload a photo, describe the change, and download an HD result. Adjust proportions, waistlines, legs, or definition online with no login or watermark.`；`/ai-image-extender/` 的 Meta Description 改为 `Expand images online with AI. Choose an original or custom ratio, position the photo on the canvas, and download an HD result with no login or watermark.`；`/free-ai-image-generator/` 的 Meta Description 改为 `Turn a text prompt into an HD image in your browser. Generate images online for free with no login or watermark, then download the finished result.`；`/terms/` 的 Meta Description 改为 `Read ImageHub’s rules for accounts, uploads, generated content, prohibited uses, intellectual property, infringement reports, and service availability.` 同步更新各页对应的 Open Graph 和 Twitter 标题或摘要，使其与新的 Title 和 Meta Description 完全一致。
- 验收标准：六个页面源码中的 Title、Meta Description、`og:title`、`og:description`、`twitter:title` 和 `twitter:description` 与本任务指定文案对应一致；每页只有一个有效 Title 和一个 Meta Description，字符正确解码，不出现 HTML 实体、重复品牌名、截断字符或首尾空格。Canonical、H1 和正文保持原值；全站重新抓取后不存在重复 Title 或重复 Meta Description。
- 不要修改：不要改写页面 H1、正文、FAQ、功能承诺、登录说明、URL、Canonical、Schema 内容结构或其他页面元数据；不要加入 `best`、保证结果、虚构数据、平台认证、排名或竞争对比；不要把独立功能页正确的 `no login` 说明扩展到首页 Workspace。

### 发布本批次公开更新日志

- 优先级：`P1`
- 页面或界面：`https://imagehub.ai/changelog/`
- 当前问题与线上证据：当前 Changelog 已包含上一批次记录，但尚未记录本批次对用户影响较大的导航与 Workspace 入口、交互式效果对比、每日免费额度及额度用完提示。
- 修改要求：只记录本批次中重要且用户能够明显感知的变化。在相关重要任务实际发布后，向现有 Changelog 顶部新增一条使用真实发布日期的英文记录：`Updated navigation and Workspace access across ImageHub, added smoother interactive before-and-after previews to Blur Background and AI Photo Editor, and clarified the shared allowance of three free tasks per user each day with a clear notice when the daily limit is reached.` 保留全部既有记录及其日期，并让最新记录排在最前。法律链接、尾斜杠重定向、Schema、Sitemap、图片尺寸与加载属性、Title、Meta Description、隐藏 DOM 清理及其他 SEO 或内部技术调整不得写入本批次公开记录。
- 验收标准：`https://imagehub.ai/changelog/` 返回 200；最新记录日期与实际上线日期一致，正文逐字匹配指定英文文案；既有历史记录、Title、Meta Description、Canonical、H1、页脚链接和站点地图均保持正常。
- 不要修改：不要记录普通文案调整、轻微视觉样式、SEO 元数据、结构化数据、Sitemap、重定向、性能实现、代码文件、组件、架构、仓库、分支、提交、基础设施、服务商配置、成本、密钥、安全敏感实现、客户数据、内部指标、AI 提示词或内部工作流；不要为了凑齐发布记录而罗列小修复。如果本任务列出的重要变化没有实际上线，不要提前发布该记录；如果只有被排除的次要调整上线，不要新增 Changelog 记录。
