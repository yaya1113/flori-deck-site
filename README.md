# 花艺在线 · 在线花艺搭配平台

> 网页制作课程设计作品 —— 基于 HTML5 / CSS3 / 原生 JavaScript 的鲜花定制服务平台静态站点。

## 项目简介

面向线上鲜花定制场景设计的 5 页面响应式站点，覆盖花艺搭配推荐、花束展示、定制服务、品牌介绍与联系咨询五条主线。
站点以 Design Token 统一多页面视觉规范，通过 Flexbox 弹性布局与 Media Query 断点实现桌面端与移动端自适应。

## 功能模块

| 页面 | 文件 | 内容 |
| --- | --- | --- |
| 花艺搭配 | `index.html` | 六类花材寓意卡片 + 热门搭配推荐 |
| 花束展示 | `bouquet.html` | 爱情 / 生日 / 毕业 / 婚礼 / 节日 / 热销排行六大系列 |
| 定制服务 | `custom.html` | 四步定制流程 + 四项服务优势 |
| 关于我们 | `about.html` | 品牌故事、企业文化、发展历程、品牌数据、团队、理念 |
| 联系我们 | `contact.html` | 门店展示、联系方式、地图、服务承诺、在线留言表单 |

## 技术要点

- **HTML5 语义化结构**：使用 `header / nav / section / footer` 组织页面骨架。
- **CSS3 弹性布局**：`Flexbox` 完成卡片网格、流程步骤与联系卡片的自适应排列。
- **Media Query 响应式**：`768px` 断点下导航栏转为纵向排列，卡片网格转为单列。
- **Design Token**：以 CSS 自定义属性统一主色、阴影、圆角与内容宽度，保证跨页面视觉一致。
- **结构与样式分离**：公共样式抽离至 `css/style.css`，页面级样式内联于对应 `<style>` 块。
- **图片压缩**：57 张素材经尺寸约束与 JPEG 重编码，由 45MB 压缩至 4MB，显著降低首屏加载耗时。

## 在线访问

**https://yaya1113.github.io/flori-deck-site/**

## 目录结构

```
flori-deck-site/
├── index.html          # 花艺搭配（站点入口）
├── bouquet.html        # 花束展示
├── custom.html         # 定制服务
├── about.html          # 关于我们
├── contact.html        # 联系我们
├── css/
│   └── style.css       # 全局公共样式（Design Token / 布局 / 组件 / 响应式）
├── images/             # 57 张花材与图标素材
└── .nojekyll           # 关闭 Jekyll 处理，保证静态资源原样部署
```

## 版本管理

项目使用 Git 进行版本管理，按功能拆分提交：

```bash
git log --oneline
```

| 提交 | 内容 |
| --- | --- |
| `chore: 初始化站点结构与首页` | 建立仓库骨架与入口页 |
| `feat: 补全花束展示与定制服务页面` | 完成两大业务模块页面 |
| `feat: 完善关于我们与联系我们页面` | 补齐品牌与联系模块页面 |
| `style: 抽取公共样式表并统一 Design Token` | 抽离 `css/style.css`，统一视觉规范 |
| `fix: 修复导航链接与资源路径失效问题` | 修正带空格的 `href` 与 `../images/` 错误路径 |
| `perf: 压缩图片资源并配置 GitHub Pages 部署` | 45MB → 4MB，新增 `.nojekyll` |

## 部署

采用 GitHub Pages 静态托管：

1. 仓库根目录即站点根目录，无需构建步骤。
2. 仓库设置中开启 **Pages**，Source 选择 `main` 分支、根目录（`/ (root)`）。
3. `.nojekyll` 文件用于跳过 Jekyll 处理，避免下划线开头的目录被忽略。

## 作者

张盛丫 · 学号 20240301068 · 青岛城市学院 计算机科学与技术
