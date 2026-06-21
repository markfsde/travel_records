# ORBIT · Travel Log 🛰️

科技现代风的 3D 旅行地球。深空黑背景 + 青色辉光，地球是发光网格 + 大陆点阵的赛博质感，去过的地方真正"亮起来"——发光核心、脉动光晕、射向太空的光柱。各大洲标有英文缩写（NA / SA / EU / AF / AS / OC）。纯前端单文件，直接传 GitHub Pages。

## 功能
- 发光网格地球，大陆用青色点阵呈现，标注洲名缩写
- 去过的地方亮起发光节点 + 光柱 + 脉动光晕，悬停显示地名
- 点击节点弹出 HUD 卡片：经纬度、日期、照片、笔记，可"Fly here"飞到该点
- 顶部 HUD 统计去过的地点数 / 国家数
- Log a place 表单：输地名一键定位（内置常见城市离线表 + OpenStreetMap 联网兜底），上传本地照片自动压缩
- 数据存浏览器本地，支持 Export / Import JSON 备份

## 操作
- 拖拽 / 触控板滑动：旋转地球（横向滑动转经度，纵向滑动转纬度）
- 滚轮 / 双指捏合：缩放
- 点击发光节点：打开记录

## 部署 GitHub Pages
1. 把 `index.html` 传到仓库
2. Settings → Pages → Deploy from a branch → main / root
3. 访问 `https://用户名.github.io/仓库名/`

零构建，上传即用。照片存浏览器本地，换设备记得 Export 备份。

## 技术栈
Three.js (r128) + 原生 JS/CSS。地球点阵用射线法判断经纬度是否落在大陆多边形内生成；光点/光柱用 AdditiveBlending 做辉光；触控板手势通过 wheel 事件的 deltaX/deltaY 与 ctrlKey 区分旋转和缩放。字体 Space Grotesk + JetBrains Mono。
