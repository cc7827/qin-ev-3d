# 比亚迪 秦 EV · 整车控制单元安装位置 3D 标注

面向新能源汽车维修教学的交互式 3D 示意图：白车身 + 10 个关键控制单元/总成的安装位置标注，
点击任意部件（或左侧列表项）即在旁边弹出**实拍解析图**，用于把「3D 位置」和「实车照片」对上。

> 制作：枣庄职业学院 · 陈澄　　车型参照：秦 EV（4765×1837×1515 mm，轴距 2718 mm）

## 网站内容

| 文件 | 说明 |
|---|---|
| `index.html` | 整个应用（Three.js 从 CDN 加载，无需构建工具） |
| `unit-key.jpg` | 智能钥匙模块（PEPS）实拍 —— 后备箱内、主驾驶一侧车身 |
| `unit-bcm.jpg` | BCM 车身控制器实拍 —— 仪表台下方、驾驶员左腿前方 |
| `unit-vcu.jpg` | VCU 整车控制器实拍 —— 中央扶手箱内 |
| `engine-bay.jpg` | 前机舱总布置实拍（点机舱内任意部件弹出） |
| `battery-pack.jpg` | 动力电池包实拍（点地板下电池包光点弹出） |
| `ac-port.png` / `dc-port.jpg` | 交流慢充口 7 芯 / 直流快充口 9 芯参考图 |
| `.nojekyll` | 让 GitHub Pages 跳过 Jekyll 处理，加快部署 |

## 发布到 GitHub Pages（网页操作，不需要装 git）

1. 登录 GitHub，右上角 **+ → New repository**
   - Repository name 填 `qin-ev-3d`（可自定，只能英文/数字/连字符）
   - 选 **Public**（免费账号的 Pages 只对公开仓库开放）
   - 点 **Create repository**
2. 在新仓库页面点 **Add file → Upload files**
3. 把本文件夹里**全部 9 个文件**（`index.html`、6 张图、`.nojekyll`）一起拖进去，点 **Commit changes**
   > 注意：是把文件拖进去，不要让它们落在子文件夹里 —— `index.html` 必须在仓库根目录。
   > `.nojekyll` 是隐藏文件，Windows 资源管理器看不到的话，可以先在「查看」里勾选「隐藏的项目」。
4. 仓库顶部 **Settings → 左侧 Pages**
   - Source 选 **Deploy from a branch**
   - Branch 选 **main**，目录选 **/ (root)**，点 **Save**
5. 等 1～2 分钟刷新该页面，顶部会出现
   `Your site is live at https://<你的用户名>.github.io/qin-ev-3d/`
   —— 这就是发给学习者的永久链接。

### 以后要改内容

重新上传同名文件即可（Add file → Upload files → 覆盖），Pages 会在 1 分钟内自动更新；
也可以直接在网页上点 `index.html` → 铅笔图标 → 编辑 → Commit。

## 关于图片显示

- 所有图片都用**相对路径**引用（`unit-key.jpg` 等），只要图片和 `index.html` 在同一个仓库目录下，
  部署后点部件就能正常显示，不依赖任何外链图床。
- 图片已压缩到适合手机加载：整站约 **0.9 MB**（原图 5.5 MB）。
- 若某张图缺失，卡片会显示「图片未找到」，不会白屏崩溃。

## 兼容性

- 电脑：Chrome / Edge 最新版，三栏布局
- 手机：竖屏自动切换为「顶部条 + 抽屉 + 底部面板」，支持单指旋转、双指缩放
- 需要联网：Three.js 从 jsDelivr 加载（失败时自动回退 unpkg）

## 版权

© 枣庄职业学院 陈澄 制作 · 请勿搬运。页面内含两处水印（右下角署名 + 画面中央极淡斜排水印）。
用于教学演示时请保留署名；如需用于教材出版或商业用途，请联系作者。
