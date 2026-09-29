# 三板斧 · 埋点事件字典

- PostHog EU · project = `sanbanfu` · uid key = `sanbanfu-uid`
- 匿名随机 8 位 uid（localStorage），零 PII；localhost 自动跳过；sendBeacon 发送。

| 事件 | 触发 | 属性 |
|------|------|------|
| `page_view` | 页面加载 | `page=index`，`ref`（来路域名，直达记 `direct`） |
| `tab_switch` | 切换 tab | `to` ∈ {pp, bd, pb, tn, how, map} |
| `png_download` | 下载长图（底部按钮或悬浮按钮） | `file` ∈ {pingpong, badminton, pickleball, tennis} |
| `share_copy` | 复制图分享文案 | `tab` ∈ {pp, bd, pb, tn} |
| `tech_detail` | 点击技术展开要领/易错 | `sport`，`name` |
| `map_sport` | 自测切换运动 | `to` ∈ {pp, bd, pb, tn} |
| `map_toggle` | 自测勾选/取消技术 | `sport`，`name`，`on` (bool) |
| `map_share` | 复制版图战绩 | `sport`，`pct` |

查询一律带 `properties.project = 'sanbanfu'` 过滤。
