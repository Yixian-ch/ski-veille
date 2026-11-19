# ski-veille

法国和安道尔一周全包滑雪套餐（住宿、全食宿、雪票、雪具）的每日价格调查网站。

- `index.html`：静态网站，无需构建，直接部署仓库根目录即可（Vercel 的 Framework Preset 选 "Other"）。
- `reports/AAAA-MM-JJ.md`：每天一份调查报告。
- `reports/index.json`：报告日期列表，例如 `["2026-11-20", "2026-11-21"]`。网站据此显示日期选择。
- `vendor/`：随站点一起发布的 Markdown 渲染库（marked、DOMPurify）。

## 每日更新

每天的定时任务完成调查后：

1. 把报告写入 `reports/AAAA-MM-JJ.md`；
2. 把当天日期加入 `reports/index.json`（不重复）；
3. 提交并推送到 `main`，托管平台随即自动重新发布。
