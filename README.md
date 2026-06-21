## ⚙️ Lovelace 仪表盘 YAML 更新日期 2026-06-11

#### 1️⃣ 切换仪表盘为yaml模式：修改主配置文件

编辑 `configuration.yaml` 文件，添加以下配置：

```yaml
# 启用 Lovelace YAML 模式
lovelace:
  mode: yaml
  # 引入资源配置文件
  resources: !include 资源配置.yaml
```

#### 2️⃣ 创建 资源配置.yaml 文件

```yaml
# Lovelace 自定义资源配置
mode: yaml
resources:
  - url: /hacsfiles/button-card/button-card.js
    type: module
  - url: /hacsfiles/kiosk-mode/kiosk-mode.js
    type: module

dashboards:
  xiaoshi-pad-ui:
    mode: yaml
    title: 平板
    icon: hass:tablet
    show_in_sidebar: true
    filename: 仪表盘-平板端/平板端主UI.yaml
  xiaoshi-phone-ui:
    mode: yaml
    title: 手机
    icon: hass:phone
    show_in_sidebar: true
    filename: 仪表盘-手机端/手机端主UI.yaml
```
#### 3️⃣ 按需求下载各个集成（数据类集成）

#### 4️⃣ 下载卡片汇总集成（所有的卡片都集中在这个集成内）

#### 5️⃣ 清楚浏览器缓存

#### 6️⃣ 仪表盘添加，搜索相应卡片即可（所有卡片均配置了可视化编辑器）

#### 7️⃣ 可参照本项目提供yaml文件修改也可以

---

# 🏠 Home Assistant 自定义集成汇总

> 📋  Home Assistant 自定义集成和仪表盘卡片项目

## 📦 集成（Integration）汇总

### 📅 卡片汇总集成 `v2026.6.4.06`

**🔗 项目地址：** https://github.com/xiaoshi930/xiaoshi

---

### 📅 本地万年历 `v4.4`

**🔗 项目地址：** https://github.com/xiaoshi930/lunar_calendar

---

### ⚡ 国网信息辅助 `v4.2`

**🔗 项目地址：** https://github.com/xiaoshi930/state_grid_info

---

### ⛽ 中国油价信息 `v3.5`
**🔗 项目地址：** https://github.com/xiaoshi930/petrochina

---

### 🎵 音乐播放器 `v2.7`

**🔗 项目地址：** https://github.com/xiaoshi930/music_player

---

### 🌤️ 和风天气 `v6.8`

**🔗 项目地址：** https://github.com/xiaoshi930/qweather

---

### 📜 本地古诗词 `v1.4`

**🔗 项目地址：** https://github.com/xiaoshi930/chinese_poetry

---

### 🖥️ PVE信息 `v1.2`

**🔗 项目地址：** https://github.com/xiaoshi930/proxmoxve

---

### 📅 课程表 `v1.2`

**🔗 项目地址：** https://github.com/xiaoshi930/classschedule

---

### 🗺️ 腾讯地图通勤 `v1.6`

**🔗 项目地址：** https://github.com/xiaoshi930/tencent_commute

---

### 💡 浴霸转空调`v1.4`

**🔗 项目地址：** https://github.com/xiaoshi930/bathroom_climate

---

### 💡 自动灯光（人在/人体）`v1.5`

**🔗 项目地址：** https://github.com/xiaoshi930/auto_light

---

## 赞助
<img width="300" height="409" alt="f63d14c2556924806d50f897590ad54" src="https://github.com/user-attachments/assets/06f862ba-299b-40df-a9a1-8fe14ec4df7e" />

