# Lovelace 仪表盘 YAML 配置指南

## 切换仪表盘

### 1. 修改主配置文件

编辑 `configuration.yaml` 文件，添加以下配置：

```yaml
# 启用 Lovelace YAML 模式
lovelace:
  mode: yaml
  # 引入资源配置文件
  resources: !include 资源配置.yaml
```
### 2. 创建 资源配置.yaml 文件，内容如下：
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

## 添加自定义集成  
hacs里添加自定义库

# 🏠 Home Assistant 自定义集成汇总

> 📋 这里汇总了所有 Home Assistant 自定义集成和仪表盘卡片项目

## 📦 集成（Integration）汇总

### 📅 本地万年历 `v2.0`

**🔗 项目地址：** https://github.com/xiaoshi930/lunar_calendar

**🎨 仪表盘卡片UI：**
- 手机端日期（自带弹出万年历）：`type: custom:xiaoshi-lunar-calendar-phone-date`
- 手机端万年历：`type: custom:xiaoshi-lunar-calendar-phone`
- 平板端日期（自带弹出万年历）：`type: custom:xiaoshi-lunar-calendar-pad-date`
- 平板端万年历：`type: custom:xiaoshi-lunar-calendar-pad`
- 日历：`type: custom:xiaoshi-lunar-calendar`
- 生日信息卡片：`type: custom:xiaoshi-birthday-card`

---

### ⚡ 国网信息辅助 `v2.1`

**🔗 项目地址：** https://github.com/xiaoshi930/state_grid_info

**🎨 仪表盘卡片UI：**
- 国网信息表格：`type: custom:xiaoshi-state-grid-table`
- 国网信息日历：`type: custom:xiaoshi-state-grid-calendar`
- 国网每日图表：`type: custom:xiaoshi-state-grid-chart-day`
- 国网每月图表：`type: custom:xiaoshi-state-grid-chart-month`
- 国网手机端UI：`type: custom:xiaoshi-state-grid-phone`
- 国网平板端UI：`type: custom:xiaoshi-state-grid-pad`

---

### ⛽ 中国油价信息 `v2.0`

**🔗 项目地址：** https://github.com/xiaoshi930/petrochina

**🎨 仪表盘卡片UI：**
- 油价信息卡片：`type: custom:xiaoshi-petrochina-card`

---

### 🎵 音乐播放器 `v2.0`

**🔗 项目地址：** https://github.com/xiaoshi930/music_player

**🎨 仪表盘卡片UI：**
- 音乐播放器：`type: custom:xiaoshi-music-player`

---

### 📜 本地古诗词 `v1.4`

**🔗 项目地址：** https://github.com/xiaoshi930/chinese_poetry

**🎨 仪表盘卡片UI：** 无

---

### 🌤️ 和风天气 `v1.8`

**🔗 项目地址：** https://github.com/xiaoshi930/qweather

**🎨 仪表盘卡片UI：** 无

---

### 🗺️ 腾讯地图通勤 `v1.4`

**🔗 项目地址：** https://github.com/xiaoshi930/tencent_commute

**🎨 仪表盘卡片UI：** 无

---

### 🖥️ PVE信息 `v1.1`

**🔗 项目地址：** https://github.com/xiaoshi930/proxmoxve

**🎨 仪表盘卡片UI：** 无

---

### 💡 自动灯光（人在/人体）`v1.5`

**🔗 项目地址：** https://github.com/xiaoshi930/auto_light

**🎨 仪表盘卡片UI：** 无

---

### 🎨 主题辅助器 `v1.5`

**🔗 项目地址：** https://github.com/xiaoshi930/xiaoshi_theme

**🎨 仪表盘卡片UI：** 无

---

## 📊 仪表盘（Dashboard）汇总

### 📱 消逝卡（平板端）`v0.0.7`

**🔗 项目地址：** https://github.com/xiaoshi930/xiaoshi-pad-card

**🎨 仪表盘卡片UI：**
- （平板端）温度湿度分布卡：`type: custom:xiaoshi-pad-grid-card`
- （通用端）HA更新信息卡：`type: custom:xiaoshi-update-card`
- （通用端）HA离线信息卡：`type: custom:xiaoshi-offline-card`
- （通用端）信息余额卡：`type: custom:xiaoshi-balance-card`

---

### 📱 消逝卡（手机端）`v0.0.6`

**🔗 项目地址：** https://github.com/xiaoshi930/xiaoshi-phone-card

**🎨 仪表盘卡片UI：**
- （手机端）空调/水暖毯/电暖器/热水器：`type: custom:xiaoshi-phone-climate-card`
- （手机端）加湿器：`type: custom:xiaoshi-phone-humidifier-card`
- （手机端）净化器：`type: custom:xiaoshi-phone-purifier-card`
- （手机端）电脑卡：`type: custom:xiaoshi-phone-computer-card`
- （手机端）灯光卡：`type: custom:xiaoshi-phone-light-card`
- （手机端）插座卡：`type: custom:xiaoshi-phone-switch-card`
- （手机端）输入卡：`type: custom:xiaoshi-phone-text-card`
- （手机端）视频卡：`type: custom:xiaoshi-phone-video-card`
- （手机端）图像卡：`type: custom:xiaoshi-phone-image-card`

---

## 准备UI  
1.平板端UI，修改【平板端主UI.yaml】和【button卡片模板\主界面弹出菜单】内容  
2.手机端UI，修改【手机端主UI.yaml】和【表体区域弹出卡片.yaml】和【动态区域弹出卡片.yaml】内容  
3.更换实体  
4.修改任何文件以后，在【平板端主UI.yaml】和【手机端主UI.yaml】这2个主文件空白地方随便加几个空格后，保存生效，刷新网页即可  
5.因为手机端屏蔽了一些无效点击反馈，但是同时也屏蔽了鼠标指针，所以手机端调试UI时，可以打开F12-切换仿真设备  

## 赞助
<img width="300" height="409" alt="f63d14c2556924806d50f897590ad54" src="https://github.com/user-attachments/assets/06f862ba-299b-40df-a9a1-8fe14ec4df7e" />

