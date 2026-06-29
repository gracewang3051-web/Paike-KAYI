# 郭锴熠 暑假课表 · 静态部署版

永久公网 URL：**[paike-app.onrender.com](https://paike-app.onrender.com)**

## 部署架构
- **平台**：Render Static Site（免费 plan）
- **数据**：`schedule.json`（与 `~/Desktop/排课/schedule.json` 同步）
- **编辑**：保留 `~/Desktop/排课/editor.html` + `server.py` 在本机（localhost:18790）
- **更新流程**：Mac 上改完 → push schedule.json → Render 自动 rebuild（1-2 分钟）

## 本地预览
```bash
cd ~/Desktop/paike-app
python3 -m http.server 8080
# 访问 http://localhost:8080
```

## 文件
- `index.html` — 整页（fetch schedule.json + 渲染）
- `schedule.json` — 课程数据
- `render.yaml` — Render 部署配置

## 视图
- **PC**：网格视图（5 时段 × 7 天）+ 列表视图切换
- **手机**（< 700px）：自动只显示列表视图
- 莫兰迪配色（数学雾蓝 / 物理鼠尾草 / 化学烟粉 / 事件沙橘）

## 数据格式
参见 `schedule.json`：
- `classes[]` — 课程
- `events[]` — 事件（飞跃理想项目）
- `gaps[]` — 待确认项
- `period` — 起止日期 + 标签

## 部署历史
- 2026-06-29 v1：紫紫部署首版

<!-- auto-deploy test 20:27:14 -->

<!-- auto-deploy verify 20:32:00 -->
