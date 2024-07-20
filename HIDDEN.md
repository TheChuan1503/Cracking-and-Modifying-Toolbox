# 隐藏的功能
- `killaura/tp_enabled` 环绕杀戮(需开启杀戮)
- `switcher/enabled` 见下

**switcher/enabled**
```jsonc
{
  "type": "toggle",
  "path": "switcher/enabled",
  "label": "插槽切换器",
  "items": [
    {
      "type": "slider",
      "path": "switcher/slot_count",
      "label": "插槽位置",
      "values":[1,2,3,4,5,6,7,8,9]
    },
    {
      "type": "action",
      "path": "auther/thehuan",
      "label": "↑攻击实体后在范围内循环主手位置",
      "icon": "ic_feather_black_24dp"
    }
  ]
}
```