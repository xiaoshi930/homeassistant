## ⚙️ Lovelace 仪表盘 YAML 更新日期 2026-06-11

### yaml参考文件获取地址：https://github.com/xiaoshi930/homeassistant

### 1️⃣ 切换仪表盘为yaml模式：修改主配置文件

编辑 `configuration.yaml` 文件，添加以下配置：

```yaml
# 启用 Lovelace YAML 模式
lovelace:
  mode: yaml
  # 引入资源配置文件
  resources: !include 资源配置.yaml
```

### 2️⃣ 创建 资源配置.yaml 文件

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
### 3️⃣ 按需求下载各个集成（数据类集成）

### 4️⃣ 下载卡片汇总集成（所有的卡片都集中在这个集成内）

### 5️⃣ 清楚浏览器缓存

### 6️⃣ 仪表盘添加，搜索相应卡片即可（所有卡片均配置了可视化编辑器）

### 7️⃣ 可参照本项目提供yaml文件修改也可以

---

# 🏠 Home Assistant 自定义集成汇总

> 📋  Home Assistant 自定义集成和仪表盘卡片项目

## 📦 集成（Integration）汇总

### 📅 卡片汇总集成 `v2026.6.4.06`

**🔗 项目地址：** https://github.com/xiaoshi930/xiaoshi

> 汇总卡版本：2026.6.4.06 | 共 **53** 个卡片类型 |

---- 本项目目前不依赖任何第3方的东西（数据获取除外，目前不依赖NR、辅助实体、其他第三方卡片、button_card等）
- 原生弹窗（不依赖browser_mod，移值https://bbs.hassbian.com/thread-32007-1-1.html）
- 原生全屏（不依赖kiosk-mode）
- 原生定时器（不依赖辅助实体timer,不依赖设备本身是否有定时功能，覆盖卡片：空调、加湿器、净化器等设备卡片）

#### 一、手机端主UI框架卡片

| type | 卡片名称 | 功能介绍 |
|------|----------|----------|
| `custom:xiaoshi-phone-card` | 消逝手机端主UI卡片 | 主UI框架，每个子模块套用下方3项内容 |
| `custom:xiaoshi-avatar-card` | 消逝手机端头像卡片 | 支持添加多个成员，显示每个成员的在家情况，距离，电量等，多用户下支持滑动切换，右上角显示在家总人数|
| `custom:xiaoshi-dynamic-card` | 消逝手机端动态区域卡片 | 支持根据设备开启情况动态加载图标，图标弹窗根据设备开启情况动态加载卡片 |
| `custom:xiaoshi-room-card` | 消逝房间卡片 | 支持各种设备按钮，温湿度显示，人在显示情况，弹窗内容设置 |

#### 二、手机端设备卡片（全功能形，主要使用场景手机端，平板端也可使用）

| type | 卡片名称 | 功能介绍 |
|------|----------|----------|
| `custom:xiaoshi-phone-climate-card` | 消逝卡(B移动端)-空调/水暖毯/热水器卡 | 适合手机端的空调/水暖毯/热水器等，可做到全功能覆盖，支持全局定时器 |
| `custom:xiaoshi-phone-humidifier-card` | 消逝卡(B移动端)-加湿器/除湿机卡 | 适合手机端的加湿器/除湿机等，可做到全功能覆盖，支持全局定时器 |
| `custom:xiaoshi-phone-purifier-card` | 消逝卡(B移动端)-净化器卡 | 适合手机端的净化器等，可做到全功能覆盖，支持全局定时器 |
| `custom:xiaoshi-phone-computer-card` | 消逝卡(B移动端)-电脑卡 | 旧电脑卡，（注：信息卡类里有新电脑卡）|
| `custom:xiaoshi-phone-light-card` | 消逝卡(B移动端)-灯光卡  | 旧灯光卡，（注：信息卡类里有新电脑卡）|
| `custom:xiaoshi-phone-switch-card` | 消逝卡(B移动端)-插座卡 | 关联插座需要先解锁 |
| `custom:xiaoshi-music-player` | 消逝卡(B移动端)-音乐播放器 | 带歌词的音乐播放器 |
| `custom:xiaoshi-tv-player` | 消逝卡(B移动端)-电视播放器 | 电视播放器，支持小米集成、adb方式、标准红外、esp红外、涂鸦红外 |
| `custom:xiaoshi-phone-fan-card` | 消逝卡(B移动端)-循环扇/风扇卡 | 适合手机端的循环扇/风扇等，可做到全功能覆盖，支持全局定时器 |
| `custom:xiaoshi-cover-card` | 消逝(B移动端)-窗帘/卷帘卡片 | 窗帘卡片 |
| `custom:xiaoshi-phone-other-card` | 消逝卡(B移动端)-其他设备卡 | 可自行拼装不通用类设备卡片，如扫地机器人、洗碗机、洗衣机、冰箱、鱼缸等，支持数值显示、滑动条显示|
| `custom:xiaoshi-lunar-calendar-phone` | 消逝万年历日历 - 手机端信息聚合 | 万年历信息，包括：阳历、阴历、节气、节日、生日、纪念日等信息，时间随意调整查看 |
| `custom:xiaoshi-lunar-calendar-phone-date` | 消逝万年历 - 手机日期 | 手机端专用展示日期，弹出万年历信息 |

#### 三、手机端设备小型卡片（只有简单开关功能，后续会继续补充）

| type | 卡片名称 | 功能介绍 |
|------|----------|----------|
| `custom:xiaoshi-small-climate-card` | 消逝卡(C微型卡)-空调/水暖毯/热水器卡 | 适合手机端的空调/水暖毯/热水器等，简单开关功能 |
| `custom:xiaoshi-small-humidifier-card` | 消逝卡(C微型卡)-加湿器卡 | 适合手机端的加湿器等，简单开关功能 |
| `custom:xiaoshi-small-purifier-card` | 消逝卡(C微型卡)-净化器卡 | 适合手机端的净化器等，简单开关功能 |

#### 四、平板端卡片（全功能形，主要使用平板端）

| type | 卡片名称 | 功能介绍 |
|------|----------|----------|
| `custom:xiaoshi-pad-card` | 消逝卡(A平板端)-背景卡（主UI框架卡） |主UI框架，包含：主题、动态背景颜色、天气变化效果、灯光设置（内含十余种灯光样式）、灯光长按调光、设备光效、设备按钮、及相应的弹出卡片设置 |
| `custom:xiaoshi-avatar-pad-card` | 消逝(A平板端)-头像卡片 | 显示每个成员的在家情况，距离，电量，话费信息等 |
| `custom:xiaoshi-dynamic-pad-card` | 消逝(A平板端)-右侧状态条 | 自定义竖向动作条，自动加载开启设备的数量、颜色、动画等，及弹出卡片设置 |
| `custom:xiaoshi-top-bar-card` | 消逝卡(A平板端)-顶部状态条 | 自定义横向动作条，自动加载按钮类信息卡片及弹出卡片设置，也可以加button_card显示（每个人的信息流不同，无法全部覆盖，可用button_card设置） |
| `custom:xiaoshi-chinese-poetry-card` | 消逝(A平板端)-古诗词卡片 | 对接古诗词集成，本地execl古诗词文件，集成目录内，可自行修改添加古诗词，界面显示，可刷新，可调用音箱执行命令实体播放 |
| `custom:xiaoshi-pad-climate-card` | 消逝卡(A平板端)-空调/水暖毯/热水器/加湿器/除湿机卡 | 适合平板端的空调/水暖毯/热水器/加湿器/除湿机等，可做到全功能覆盖，支持全局定时器 |
| `custom:xiaoshi-pad-fan-card` | 消逝卡(A平板端)-循环扇/风扇/净化器卡 |  适合平板端的循环扇/风扇/净化器等，可做到全功能覆盖，支持全局定时器 |
| `custom:xiaoshi-pad-grid-card` | 消逝卡(A平板端)-温湿度分布卡 | 按房间图设置温度、湿度分布图、及对应弹出卡片 |
| `custom:xiaoshi-weather-pad-card` | 消逝(A平板端)-天气卡片 | 对接天气集成，支持按ha地点、手机实体设置天气gps数据源，支持只在前端打开时刷新数据（节约api数量），全量天气数据，包括：天气状况、最低最高温度、降雨量、风速、风向等|
| `custom:xiaoshi-sun-moon-card` | 消逝(A平板端)-日出日落月升月落卡片 | 简单展示日升日落，月升月落的卡片 | 
| `custom:xiaoshi-lunar-calendar-pad` | 消逝万年历日历 - 平板端信息 | 万年历信息，包括：阳历、阴历、节气、节日、生日、纪念日等信息，时间随意调整查看 |
| `custom:xiaoshi-lunar-calendar-pad-date` | 消逝万年历 - 平板日期 | 平板端专用展示日期、最近的节日、最近的生日，弹出万年历信息 |
| `custom:xiaoshi-birthday-card` | 消逝万年历 - 生日信息卡片 | 结合万年历，显示生日信息卡片 |
| `custom:xiaoshi-lunar-calendar` | 消逝万年历日历 - 日历信息UI | 日历部分卡片 |

#### 五、信息类卡片（button类的自带弹出card卡片、手机端/平板端都可使用）

| type | 卡片名称 | 功能介绍 |
|------|----------|----------|
| `custom:xiaoshi-ha-info-card` | 消逝HA信息卡片 | 展示ha的版本信息、资源占用量、加载项占用量、备份信息、离线设备统计、离线实体统计、更新、重启、备份等功能 |
| `custom:xiaoshi-ha-info-button` | 消逝HA信息卡片按钮 | 上面卡片的按钮，显示需要关注的总条数 |
| `custom:xiaoshi-todo-card` | 消逝待办信息卡片 | 结合ha自带的待办事项，展示待办信息，新增、修改、删除待办信息 |
| `custom:xiaoshi-todo-button` | 消逝待办信息片按钮 | 上面卡片的按钮，显示需要待办数，过期显示红色 |
| `custom:xiaoshi-chart-card` | 消逝温湿度曲线卡 | 简单的温湿度曲线卡片 |
| `custom:xiaoshi-chart-button` | 消逝温湿度曲线片按钮 | 上面卡片的按钮，显示温湿度 |
| `custom:xiaoshi-balance-card` | 消逝余额信息卡片 | 统计各项余额信息（如电话费等），自定义预警条件 |
| `custom:xiaoshi-balance-button` | 消逝余额信息片按钮 | 上面卡片的按钮，显示总余额、平均余额、最低余额 |
| `custom:xiaoshi-consumables-card` | 消逝耗材信息卡片 | 统计各项耗材信息（如电量等），自定义预警条件 |
| `custom:xiaoshi-consumables-button` | 消逝耗材信息片按钮 | 上面卡片的按钮，显示符合条件的低耗材数量 |
| `custom:xiaoshi-petrochina-card` | 中国油价信息卡片 | 结合油价集成，展示最新油价、油价省份排行、油价调价历史等 |
| `custom:xiaoshi-petrochina-button` | 中国油价信息片按钮 | 上面卡片的按钮，显示对应油号的单价 |
| `custom:xiaoshi-state-grid-info` | 消逝公用事业卡片（水、电、气） | 水电气卡片、日历数据、月图表、日图表等 |
| `custom:xiaoshi-state-grid-button` | 消逝公用事业片卡片按钮（水、电、气） | 上面卡片的按钮，显示对应的余额 |
| `custom:xiaoshi-weather-phone-card` | 消逝天气卡片 | 对接天气集成，支持按ha地点、手机实体设置天气gps数据源，支持只在前端打开时刷新数据（节约api数量），全量天气数据，包括：天气状况、最低最高温度、降雨量、风速、风向等|
| `custom:xiaoshi-weather-phone-button` | 消逝天气按钮卡片 | 上面卡片的按钮，显示当前天气状况+预警条数 |
| `custom:xiaoshi-button` | 消逝空白按钮 | 单独做了一个符合统一风格的空白按钮，可自行设置显示内容和弹出卡片内容 |
| `custom:xiaoshi-device-button` | 消逝灯光按钮/设备按钮 | 单独做了一个符合统一风格的灯光或设备的按钮，可自行设置显示内容和弹出卡片内容 |
| `custom:xiaoshi-light-card` | 消逝卡(移动端)-房间灯光卡 | 新灯卡，可按照房间设置灯光，支持全关、全开、调光、调色、情景模式等 |
| `custom:xiaoshi-iot-computer-card` | 消逝卡(B移动端)-电脑卡(IOTLink) | 结合windows的IOTLink的软件，自动生成卡片 |
| `custom:xiaoshi-pve-card` | 消逝卡-PVE卡片 | 结合pve集成，自动获取pve相关的卡片，子设备关机、重启等 |
| `custom:xiaoshi-class-card` | 消逝卡-课程表卡片 | 结合课程表集成，展示课程表 |

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

