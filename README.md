# web-playground

个人娱乐时写的小网站合集：纯静态 HTML，零依赖、零构建，双击就能玩。

## 站点

| 名称 | 一句话玩法 | 打开方式 |
| --- | --- | --- |
| [年会抽奖](./annual-lottery/) | 贴一份名单、配几个奖项，点按钮滚动抽人，中奖记录自动存本地 | `annual-lottery/index.html` |
| [沙丁鱼群 2D](./sardine-boids/) | 一屏 boids 沙丁鱼群游来游去，合群、避让、绕开捕食者 | `sardine-boids/index.html` |
| [沙丁鱼群 3D](./sardine-boids-3d/) | 3D 版鱼群，带虎鲸捕食者，能围观谁被吃掉 | `sardine-boids-3d/index.html` |

> 旧版年会抽奖（v1，上传 txt 名单的简版）留在 [archive/annual-lottery-v1.html](./archive/annual-lottery-v1.html)，仅作存档，不再维护。

## 本地打开

两种方式，选一个就行：

1. **直接双击**仓库根目录的 `index.html`，从落地页点进各个站点。
2. **起个本地服务**（想在手机上看、或浏览器对 `file://` 有意见时）：

   ```bash
   python -m http.server 8000
   # 然后打开 http://localhost:8000
   ```

所有页面都是单文件 HTML，CSS / JS 全部内联，不联网也能跑（沙丁鱼 3D 用的是浏览器原生 WebGL/Canvas，没有引入任何外部 CDN 或字体）。

## 新增站点的约定

- 每个站点一个目录，目录名用 ASCII 短横线小写，例如 `tiny-shooter/`。
- 目录里放一个 `index.html`，样式和脚本尽量内联，保持"单文件可跑"。
- 在根 `index.html` 的卡片区加一张卡片，指向新站点的目录。
- 在上面的站点表格里补一行。
- 过时或重写的旧版丢进 `archive/`，文件名带上版本号。

## 关于代码质量

这些都是玩票作品：想到哪写到哪，命名和结构不一定讲究，也懒得做构建和测试。看着能跑、玩着开心就够了。
