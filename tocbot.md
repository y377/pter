| option  | value  | description  |
| :------------ | :------------ | :------------ |
| tocSelector  | `.js-toc`  | toc选择器,在哪里呈现目录  |
|tocElement   | element  | toc元素,或者，您可以改为传入 DOM 节点 |
| contentSelector  | `.js-toc-content`  | 内容选择器,在哪里抓取标题来构建目录  |
| contentElement  | element  | 内容元素,或者，您可以改为传入 DOM 节点  |
| headingSelector  | 'h1, h2, h3'  | 在 contentSelector 元素中抓取哪些标题  |
|ignoreSelector   | `'.js-toc-ignore'`  | 匹配 ignoreSelector 的标题将被跳过  |
| hasInnerContainers  |false   | 对于内容中相对或绝对定位容器内的标题  |
| linkClass  | `'toc-link'`  |  添加到链接的主类 |
| extraLinkClasses  | `''`  | 添加到链接的额外类  |
| activeLinkClass  | `'is-active-link'`  | 要添加到活动链接的类，该链接对应于页面上最顶部的标题 |
| listClass  | `'toc-list'`  | 要添加到列表中的主类  |
|extraListClasses   | `"`  | 要添加到列表中的额外类  |
| isCollapsedClass  | `'is-collapsed'`  | 当列表应该折叠时添加的类 |
| collapsibleClass  | `'is-collapsible'`  | 当列表应该能够折叠但不一定折叠时添加的类 |
| listItemClass  | `'toc-list-item'`  | 要添加到列表项的类 |
| activeListItemClass  | `'is-active-li'`  | 要添加到活动列表项的类 |
| collapseDepth  | 0  |  有多少标题级别不应折叠。例如，数字 6 将显示所有内容，因为只有 6 个标题级别，数字 0 将全部折叠。当您滚动到其中的标题时，隐藏的部分将打开和关闭。 |
| scrollSmooth  | true  | 启用平滑滚动 |
| scrollSmoothDuration  | 420  | 平滑滚动持续时间  |
|scrollSmoothOffset  | 0  | 平滑滚动偏移  |
|scrollEndCallback   | `function (e) {}`  | 滚动结束回调  |
| headingsOffset  | 1  | 标题与文档顶部之间的标题偏移量(这意味着较小的调整) |
| throttleTimeout  | 50  | 事件触发之间的超时，以确保它不会太快(出于性能原因)  |
| positionFixedSelector  | null  | 元素中添加positionFixedClass  |
| positionFixedClass  | `'is-position-fixed'`  | 添加固定位置类，使侧边栏在向下滚动超过 fixedSidebarOffset 后固定 |
| fixedSidebarOffset  | `'auto'`  | fixedSidebarOffset 可以是任何数字，但默认情况下设置为 auto，它将 fixedSidebarOffset 设置为边栏元素的 offsetTop 从文档顶部开始  |
| includeHtml  | false  | includeHtml 可以设置为 true 以包含来自标题节点的 HTML 标记，而不是仅包含 textContent  |
| includeTitleTags  | false  | includeTitleTags 自动设置链接的 html 标题标签以匹配标题。这对于 SEO 目的或截断标题时很有用 |
| onClick  | `function (e) {}`  | onclick 函数应用于目录中的所有链接。将以事件作为第一个参数调用，这可用于停止、传播、防止默认或执行操作 |
| orderedList  | true  | orderedList 可以设置为 false 以生成无序列表 (ul) 而不是有序列表 (ol) |
| scrollContainer  | null  | 如果有固定的文章滚动容器，设置计算标题的偏移量  |
| skipRendering  | false  | 如果ToC DOM已经被外部系统渲染，则阻止它的渲染 |
| headingLabelCallback  | false  | 更改标题标签的可选回调。<br> 例如，它可以用于减少并在您认为太长的多行标题上放置省略号。<br> 每次解析标题时调用。 需要一个字符串并返回修改后的标签以显示。<br> 此外，可以在标题上使用属性 `data-heading-label` 来指定<br>在 TOC 中使用的较短的字符串。<br>`function (string) => string` |
| ignoreHiddenElements  | false  | 忽略隐藏在 DOM 中的标题 |
| headingObjectCallback  | null  | 可选的回调来修改已解析标题的属性。<br>在节点参数中传递标题元素，在obj参数中提供默认解析器解析的信息。<br>函数必须返回相同或修改过的obj。<br>如果没有返回，则标题将从TOC中排除。<br>`function (object, HTMLElement) => object \| void` |
| basePath  | `''`  | 设置基本路径，如果你在' head '中使用' base '标签，这很有用 |
| disableTocScrollSync  | false  | 只在`tocSelector`滚动时生效，保持toc滚动位置与内容同步。  |
| tocScrollOffset  | 0  | 当滚动页面时，toc滚动（顶部）位置的偏移。只有在`disableTocScrollSync`为false时才有效。 |

---------------
