# 修改/增强功能
#### 功能文件所在目录结构
```
Toolbox.apk/
│
└── res/
    └── raw/
        ├── ui_categories.json
        ├── ui_xxx.json
        └── ui_toolbar_xxx.json
```
#### 文件描述
其中
* `ui_categories.json` 里面声明了所有的ui文件(**同时需要在`resources.arsc`中声明**)
* `ui_xxx.json` 为普通功能文件
* `ui_toolbar_xxx.json` 为工具栏功能文件
#### 各文件结构
**ui_xxx.json**
```jsonc
{
  "name": "分类名",
  "help_id": "分类id",
  "android_icon": "图标",
  "shortcut_color": "快捷方式颜色",

  "items": [
    {
      "type": "功能类型",
      "path": "功能id",
      "label": "功能名",
      "icon": "图标",
      "value": 值,
      "values": 可取值数组,
      "range_value": 取值范围
    } // 功能对象
  ] // 功能列表
}
```
**ui_toolbar_xxx.json**
```jsonc
{
  "show_if": {
    "and": [
      "rapid_build/enabled",
      "rapid_build/command_mode"
    ] // 功能同时开启(toggle)
  }, // 显示条件

  "items": [
    {
      "type": "toggle", // 不能为slider
      "path": "rapid_build/selection_mode",
      "value": 1,
      "icon": "ic_area1_black_24dp"
    }, // 功能对象
  ] // 功能列表
}
```
#### 功能类型
- `toggle` 开关
- `action` 按钮(箭头)
- `slider` 滑块

~~今天的文档就写到这里吧，未完待续~~