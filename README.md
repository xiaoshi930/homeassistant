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

## 导入NR流  
NR基本都替换掉了，还剩一点点，按需导入  

## 准备UI  
1.平板端UI，修改【平板端主UI.yaml】和【button卡片模板\主界面弹出菜单】内容  
2.手机端UI，修改【手机端主UI.yaml】和【表体区域弹出卡片.yaml】和【动态区域弹出卡片.yaml】内容  
3.更换实体  
4.修改任何文件以后，在【平板端主UI.yaml】和【手机端主UI.yaml】这2个主文件空白地方随便加几个空格后，保存生效，刷新网页即可  
5.因为手机端屏蔽了一些无效点击反馈，但是同时也屏蔽了鼠标指针，所以手机端调试UI时，可以打开F12-切换仿真设备  

## 赞助
<img width="300" height="409" alt="f63d14c2556924806d50f897590ad54" src="https://github.com/user-attachments/assets/06f862ba-299b-40df-a9a1-8fe14ec4df7e" />

