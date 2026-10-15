# 项目主页模板（Jekyll）

这是为你「塑料模具工厂 · 产能负荷预测与经济分析系统」生成的**项目介绍页**，基于 Jekyll，可一键部署到 GitHub Pages。

## 目录结构

```
project_website/
├── _config.yml              # Jekyll 配置
├── index.md                 # 页面内容（改这里！）
├── _layouts/
│   └── project_page.html    # 页面布局模板
└── static/
    └── image/
        ├── dashboard.svg    # 看板占位图（替换成真实截图）
        └── pipeline.svg     # 架构图
```

## 使用步骤

### 1. 改内容
打开 `index.md`，把开头的占位信息改掉：

| 占位 | 改成 |
|------|------|
| `你的名字` | 你的姓名 |
| `你的单位 / 团队` | 你的单位或团队名 |
| `https://github.com/你的用户名/moju` | 你的 GitHub 仓库地址 |
| `https://你的应用.onrender.com` | 系统在线地址（部署后可填） |

### 2. 替换图片
把你系统的实际运行截图保存为 PNG，放到 `static/image/` 里，然后在 `index.md` 中把对应的图片引用改掉，例如：

```markdown
![系统看板](static/image/dashboard.png)
```

### 3. 本地预览（可选）
安装 Jekyll 后运行：

```bash
cd project_website
bundle install
bundle exec jekyll serve
```

浏览器打开 http://localhost:4000 查看效果。

### 4. 部署到 GitHub Pages
1. 在 GitHub 新建一个仓库，比如叫 `project_website`；
2. 把本文件夹上传 / push 到该仓库；
3. 仓库 → `Settings` → `Pages` → `Build and deployment` 选 `Deploy from a branch` → 分支选 `main`、目录选 `/(root)` → Save；
4. 约 1 分钟后访问：`https://你的用户名.github.io/project_website/`。

> 注意：如果部署后图片不显示，打开 `_config.yml`，把 `baseurl: ""` 改成 `baseurl: "/project_website"`（`/仓库名`）即可。

## 提示
- 这个页面是**静态介绍页**，用来展示项目是什么、有什么功能、截图和链接；
- 你那个 Flask 系统本身需要 Python 运行环境，请另外部署到 Render / Railway 等平台（见项目根目录说明）。
