# Icon.xml 文件说明与教程

## 1. 简介

`Icon.xml` 文件用于定义亚洲文明及其领袖的图标资源，包括文明图标、领袖图标、领袖外交背景图以及特色建筑图标。该文件主要由 `IconTextureAtlases` 和 `IconDefinitions` 两个部分组成。

---

## 2. `IconTextureAtlases` 部分

该部分用于定义图标的纹理图集，包括不同尺寸的图标文件。每个 `Row` 定义一个特定的图标资源，并指定文件路径。

### 2.1 文明图标

```xml
<Row Name="ATLAS_CIVILIZATION_CIVILIZATION_ASIA" IconSize="256" IconsPerRow="1" IconsPerColumn="1" Filename="ICON_CIVILIZATION_ASIA_256.dds"/>
```

- `Name`：定义纹理图集的名称。
- `IconSize`：指定图标的尺寸，例如 256px。
- `IconsPerRow` / `IconsPerColumn`：定义图标在 DDS 纹理中的排列方式。
- `Filename`：DDS 纹理文件的名称。

### 2.2 领袖图标

```xml
<Row Name="ATLAS_LEADER_LEADER_ERQ" IconSize="256" IconsPerRow="1" IconsPerColumn="1" Filename="ICON_LEADER_ERQ_256.dds"/>
```

- 用于定义特定领袖的头像图标。
- 需要为不同大小提供对应的 DDS 资源。

### 2.3 领袖外交背景图

```xml
<Row Name="ATLAS_LEADER_BACKGROUND_LEADER_ERQ" IconSize="256" IconsPerRow="1" IconsPerColumn="1" Filename="ICON_BACKGROUND_LEADER_ERQ_256.dds"/>
```

- 定义领袖在外交界面中的背景图。

### 2.4 特色建筑图标

```xml
<Row Name="ICON_DISTRICT_ASIAN_ACADEMIC_CENTER" Atlas="ICON_ATLAS_BUILDINGS" Index="18"/>
```

- `Name`：自定义建筑的唯一名称。
- `Atlas`：该图标所属的纹理图集名称。
- `Index`：该图标在图集中对应的索引。

---

## 3. `IconDefinitions` 部分

该部分用于将 `IconTextureAtlases` 中定义的图集资源与实际游戏中使用的 `ICON_` 资源名称进行绑定。

```xml
<Row Name="ICON_CIVILIZATION_ASIA" Atlas="ATLAS_CIVILIZATION_CIVILIZATION_ASIA" index="0"/>
<Row Name="ICON_LEADER_ERQ" Atlas="ATLAS_LEADER_LEADER_ERQ" index="0"/>
<Row Name="ICON_BACKGROUND_LEADER_ERQ" Atlas="ATLAS_LEADER_BACKGROUND_LEADER_ERQ" index="0"/>
```

- `Name`：游戏内部使用的图标名称，必须与相关数据定义一致。
- `Atlas`：该图标在 `IconTextureAtlases` 部分对应的纹理集名称。
- `Index`：图标在图集中的位置。


