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

> 汇总卡版本：2026.6.4.06 | 共 **53** 个卡片类型 |

---

#### 一、手机端主UI框架卡片

| type | 卡片名称 |
|------|----------|
| `custom:xiaoshi-phone-card` | 消逝手机端主UI卡片 |
| `custom:xiaoshi-avatar-card` | 消逝手机端头像卡片 |
| `custom:xiaoshi-dynamic-card` | 消逝手机端动态区域卡片 |
| `custom:xiaoshi-room-card` | 消逝房间卡片 |

#### 二、手机端设备卡片（全功能形，主要使用场景手机端，平板端也可使用）

| type | 卡片名称 |
|------|----------|
| `custom:xiaoshi-phone-climate-card` | 消逝卡(B移动端)-空调/水暖毯/热水器卡 |
| `custom:xiaoshi-phone-humidifier-card` | 消逝卡(B移动端)-加湿器/除湿机卡 |
| `custom:xiaoshi-phone-purifier-card` | 消逝卡(B移动端)-净化器卡 |
| `custom:xiaoshi-phone-computer-card` | 消逝卡(B移动端)-电脑卡（注：信息卡类里有新电脑卡） |
| `custom:xiaoshi-phone-light-card` | 消逝卡(B移动端)-灯光卡（注：信息卡类里有新电脑卡）  |
| `custom:xiaoshi-phone-switch-card` | 消逝卡(B移动端)-插座卡 |
| `custom:xiaoshi-music-player` | 消逝卡(B移动端)-音乐播放器 |
| `custom:xiaoshi-tv-player` | 消逝卡(B移动端)-电视播放器 |
| `custom:xiaoshi-phone-fan-card` | 消逝卡(B移动端)-循环扇/风扇卡 |
| `custom:xiaoshi-cover-card` | 消逝(B移动端)-窗帘/卷帘卡片 |
| `custom:xiaoshi-phone-other-card` | 消逝卡(B移动端)-其他设备卡（注：可自行拼装不通用类设备卡片，如扫地机器人、洗碗机、洗衣机、冰箱、鱼缸等）  |
| `custom:xiaoshi-lunar-calendar-phone` | 消逝万年历日历 - 手机端信息聚合 |
| `custom:xiaoshi-lunar-calendar-phone-date` | 消逝万年历 - 手机日期 |

#### 三、手机端设备小型卡片（只有简单开关功能，后续会继续补充）

| type | 卡片名称 |
|------|----------|
| `custom:xiaoshi-small-climate-card` | 消逝卡(C微型卡)-空调/水暖毯/热水器卡 |
| `custom:xiaoshi-small-humidifier-card` | 消逝卡(C微型卡)-加湿器卡 |
| `custom:xiaoshi-small-purifier-card` | 消逝卡(C微型卡)-净化器卡 |

#### 四、平板端卡片（全功能形，主要使用平板端）

| type | 卡片名称 |
|------|----------|
| `custom:xiaoshi-pad-card` | 消逝卡(A平板端)-背景卡（主UI框架卡） |
| `custom:xiaoshi-avatar-pad-card` | 消逝(A平板端)-头像卡片 |
| `custom:xiaoshi-dynamic-pad-card` | 消逝(A平板端)-右侧状态条 |
| `custom:xiaoshi-top-bar-card` | 消逝卡(A平板端)-顶部状态条 |
| `custom:xiaoshi-chinese-poetry-card` | 消逝(A平板端)-古诗词卡片 |
| `custom:xiaoshi-pad-climate-card` | 消逝卡(A平板端)-空调/水暖毯/热水器/加湿器/除湿机卡 |
| `custom:xiaoshi-pad-fan-card` | 消逝卡(A平板端)-循环扇/风扇/净化器卡 |
| `custom:xiaoshi-pad-grid-card` | 消逝卡(A平板端)-温湿度分布卡 |
| `custom:xiaoshi-weather-pad-card` | 消逝(A平板端)-天气卡片 |
| `custom:xiaoshi-sun-moon-card` | 消逝(A平板端)-日出日落月升月落卡片 |
| `custom:xiaoshi-lunar-calendar-pad` | 消逝万年历日历 - 平板端信息 |
| `custom:xiaoshi-lunar-calendar-pad-date` | 消逝万年历 - 平板日期 |
| `custom:xiaoshi-birthday-card` | 消逝万年历 - 生日信息卡片 |
| `custom:xiaoshi-lunar-calendar` | 消逝万年历日历 - 日历信息UI |

#### 五、信息类卡片（button类的自带弹出card卡片、手机端/平板端都可使用）

| type | 卡片名称 |
|------|----------|
| `custom:xiaoshi-ha-info-card` | 消逝HA信息卡片 |
| `custom:xiaoshi-ha-info-button` | 消逝HA信息卡片按钮 |
| `custom:xiaoshi-todo-card` | 消逝待办信息卡片 |
| `custom:xiaoshi-todo-button` | 消逝待办信息片按钮 |
| `custom:xiaoshi-chart-card` | 消逝温湿度曲线卡 |
| `custom:xiaoshi-chart-button` | 消逝温湿度曲线片按钮 |
| `custom:xiaoshi-balance-card` | 消逝余额信息卡片 |
| `custom:xiaoshi-balance-button` | 消逝余额信息片按钮 |
| `custom:xiaoshi-consumables-card` | 消逝耗材信息卡片 |
| `custom:xiaoshi-consumables-button` | 消逝耗材信息片按钮 |
| `custom:xiaoshi-petrochina-card` | 中国油价信息卡片 |
| `custom:xiaoshi-petrochina-button` | 中国油价信息片按钮 |
| `custom:xiaoshi-state-grid-info` | 消逝公用事业卡片（水、电、气） |
| `custom:xiaoshi-state-grid-button` | 消逝公用事业片卡片按钮（水、电、气） |
| `custom:xiaoshi-weather-phone-card` | 消逝天气卡片 |
| `custom:xiaoshi-weather-phone-button` | 消逝天气按钮卡片 |
| `custom:xiaoshi-button` | 消逝空白按钮 |
| `custom:xiaoshi-device-button` | 消逝灯光按钮/设备按钮 |
| `custom:xiaoshi-light-card` | 消逝卡(移动端)-房间灯光卡 |
| `custom:xiaoshi-iot-computer-card` | 消逝卡(B移动端)-电脑卡(IOTLink) |
| `custom:xiaoshi-pve-card` | 消逝卡-PVE卡片 |
| `custom:xiaoshi-class-card` | 消逝卡-课程表卡片 |

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

