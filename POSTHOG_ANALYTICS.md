# 三板斧 · 埋点事件字典

- PostHog EU · project = `sanbanfu` · uid key = `sanbanfu-uid`
- 匿名随机 8 位 uid（localStorage），零 PII；localhost 自动跳过；sendBeacon 发送。

| 事件 | 触发 | 属性 |
|------|------|------|
| `page_view` | 页面加载 | `page=index` |
| `tab_switch` | 切换运动 tab | `to` ∈ {pp, bd, pb, tn} |
| `png_download` | 下载长图 | `file` ∈ {pingpong, badminton, pickleball, tennis} |
| `share_copy` | 复制分享文案 | `tab` ∈ {pp, bd, pb} |

查询一律带 `properties.project = 'sanbanfu'` 过滤。
