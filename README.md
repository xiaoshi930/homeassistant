### 鉴于部分同学的NR不稳定、NR学习成本较高，现逐步淘汰配套NR，使用集成替代
### 暂时没有替代完成的：天气相关NR（操作UI部分的，数据获取已转到集成）、待办相关NR
### 所有集成移步到项目主页查看：https://github.com/xiaoshi930?tab=repositories
###  
  
  
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
# 在此处添加您的自定义资源
# - url: /hacsfiles/your-plugin/your-card.js
#   type: module

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
注意自定义库的类型，js为仪表盘、其余都是集成  


