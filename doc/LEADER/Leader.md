## 1. 领袖基本定义：

```xml
<GameData>
    <Types>
        <Row Type="LEADER_ERQ" Kind="KIND_LEADER"/>
        <Row Type="TRAIT_LEADER_ERQ_WORLD_HARMONY" Kind="KIND_TRAIT"/>
    </Types>
</GameData>
```

- `Types` 部分定义了新的游戏元素。
- `LEADER_ERQ`：新领袖的唯一标识符。
- `TRAIT_LEADER_ERQ_WORLD_HARMONY`：该领袖的专属特性。

## 2. 设定领袖的基本信息：

```xml
<Leaders>
    <Row LeaderType="LEADER_ERQ"
         Name="LOC_LEADER_ERQ_NAME"
         InheritFrom="LEADER_DEFAULT"
         Sex="Male"/>
</Leaders>
```

- `LeaderType`：唯一的领袖标识符（必须与 `Types` 对应）。
- `Name`：领袖名称（此处使用的是本地化字符串 `LOC_LEADER_ERQ_NAME`）。
- `InheritFrom`：继承自默认领袖 `LEADER_DEFAULT`。
- `Sex`：性别（`Male` 表示男性，`Female` 表示女性）。


