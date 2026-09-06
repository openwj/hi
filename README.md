# 我的码 · 共建仓库

独立全栈开发者的合作主页：找一起做产品的创业伙伴。你管业务，我管产品，从 MVP 一路做到有人付费。

由 `demo.html` 按当前 Astro 架构 1:1 还原：Astro 组件 + Tailwind（预检）+ Vue 集成，交互部分保留原生 JS 以保证行为一致。

## 项目结构

```text
/
├── demo.html              # 原始单文件版本（参考基准）
├── fufei.html             # 付费方案手册原始单文件 demo（参考基准）
├── public/
│   └── favicon.*
└── src
    ├── components/        # 按区块拆分的页面组件
    │   ├── Hero.astro     # 首屏 + 终端
    │   ├── Ticker.astro   # commit 跑马灯
    │   ├── Diff.astro     # 01 合作方式
    │   ├── Who.astro      # 02 找谁
    │   ├── Work.astro     # 03 作品仓库
    │   ├── Modes.astro    # 04 投入方式（含执行手册入口）
    │   ├── How.astro      # 05 流程
    │   ├── Path.astro     # 06 轨迹 + 数据带
    │   ├── Voices.astro   # 07 伙伴的话
    │   ├── About.astro    # 08 关于
    │   ├── Faq.astro      # 09 FAQ
    │   └── Pr.astro       # 10 发 PR
    ├── layouts
    │   ├── Layout.astro   # 主站 head / 顶栏 / 页脚 / 弹窗 / 主脚本
    │   └── PricingLayout.astro  # 手册页头尾布局（/pricing）
    ├── pages
    │   ├── index.astro    # 主站首页
    │   └── pricing.astro  # 合作执行手册（首页“投入方式”区块可跳入）
    └── styles
        ├── global.css     # Tailwind 预检 + 主站全套样式
        └── pricing.css    # 手册页独立样式
```

## 命令

| 命令           | 作用                               |
| :------------- | :--------------------------------- |
| `pnpm dev`     | 启动开发服务器 `localhost:4321`    |
| `pnpm build`   | 构建生产版本到 `./dist/`           |
| `pnpm preview` | 本地预览构建产物                   |

> 主站页面数据（项目、评价、FAQ、提交记录、邮箱）都在 `src/layouts/Layout.astro` 的脚本数据区；手册页数据与脚本在 `src/pages/pricing.astro`。替换成真实内容即可。