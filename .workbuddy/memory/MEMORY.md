# 项目长期笔记

## 项目页组织规范（用户指定）
- 项目页放 `src/pages/pr/<编码>/`，编码 = `p + 立项日期 YYYYMMDD`（如 `p20260908` = 兰森食堂）；资源（原始内容 html、页面 css、参考原稿 reference/）放 `src/projects/<编码>/`。
- 布局用 `src/layouts/ProjectLayout.astro`（props: title/description/crumb/foot + slot:actions）；页面样式由各页面自行 import，不进布局。
- 配色/字体统一用 global.css `@theme` token（--color-amber 等深色主题）。

## 已有项目
- `pr/p20260908` — 兰森食堂（私域白领外卖平台）：plan = PRD 梳理稿（口令 20260908，sha256 前端校验）；pricing = 合作方案报价（M1 一口价 + 月费档位联动，CONFIG 在 pricing.astro）。

## 环境注意
- `astro build` 在 WorkBuddy 沙箱会在 ssrMoveAssets 报错（环境限制）；验证用 dev server（用户常开在 4321）。
- 批量替换用 `perl -pi -e`（sed -i 不可用）；BSD grep 交替用 `-E`。
