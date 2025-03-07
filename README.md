﻿# 亚洲文明

文明VI亚洲文明模组，包含一个领袖(ERQ)，三个特色区域（亚洲文化中心、亚洲国立学术中心和亚洲金融中心）。
[配套教程](https://github.com/LaoeGaoci/CivVI_Mentor)

![文明图标](./Image/ITRODUCTION.png)

![外交界面](./Image/DIPLOMACY.png)

## 项目结构

### ArtDefs

包含mod中特色区域建筑的建筑模型。(District.artdef存在问题，游戏中无法显示区域的Landmarks)

### Icons

包含mod中使用的图标(文明LOGO，领袖头像，背景图)。

### Text

包含本地化文本文件，为mod提供游戏内的文本描述、名称和其他字符串数据。

### Textures

包含mod所需的图片资源文件

### XLps

包含XML文件，加入了mod中使用的图标（文明LOGO，领袖头像，背景图）。

### 代码文件

- **Asia.xml**: 包含亚洲文明的主要定义，特色能力。
- **Color.xml**: 包含颜色设置。
- **District.xml**: 定义了与本mod相关的区域设置
- **Leader.xml**: 包含亚洲文明领袖的定义，包括能力、特性和其他特征（包含加载界面和外交界面的设置）。
- **config.xml**: mod的配置文件（与领袖选择界面相关）。
- **moment.xml**: 有关历史年表的设定(存在问题，文字与图片加载失败)
