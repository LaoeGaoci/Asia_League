## 特色建筑定义参数解析与示例：

代码部分详情见src/District.xml

🏦亚洲金融中心：

```xml
<!-- 定义特色区域为区域 -->
<Types>
    <Row Type="DISTRICT_ASIA_FINANCIAL_CENTER" Kind="KIND_DISTRICT"/>
</Types>

<!-- 定义特色区域的详细参数设置 -->
<District>
<Row DistrictType="DISTRICT_ASIA_FINANCIAL_CENTER"
             Name="LOC_DISTRICT_ASIA_FINANCIAL_CENTER_NAME"
             Description="LOC_DISTRICT_ASIA_FINANCIAL_CENTER_DESCRIPTION"
             PrereqTech="TECH_BANKING"
             PlunderType="PLUNDER_GOLD"
             PlunderAmount="50"
             AdvisorType="ADVISOR_GENERIC"
             Cost="30"
             CostProgressionModel="COST_PROGRESSION_NUM_UNDER_AVG_PLUS_TECH"
             CostProgressionParam1="40"
             Maintenance="1"
             RequiresPlacement="true"
             RequiresPopulation="true"
             Aqueduct="false"
             NoAdjacentCity="false"
             InternalOnly="false"
             ZOC="false"
             CaptureRemovesBuildings="false"
             CaptureRemovesCityDefenses="false"
             MilitaryDomain="NO_DOMAIN"
             CityStrengthModifier="2"/>
</District>
```

📌 主要参数解析

| **字段**          | **含义**                      | **示例值**                                            |
| --------------- | --------------------------- | -------------------------------------------------- |
| `DistrictType`  | 区域的唯一 ID，在 MOD 代码中用于引用      | `"DISTRICT_ASIA_FINANCIAL_CENTER"`                 |
| `Name`          | 该区域在游戏 UI 中显示的名称（本地化标签）     | `"LOC_DISTRICT_ASIA_FINANCIAL_CENTER_NAME"`        |
| `Description`   | 该区域的详细描述（本地化标签）             | `"LOC_DISTRICT_ASIA_FINANCIAL_CENTER_DESCRIPTION"` |
| `PrereqTech`    | **解锁该区域需要的科技**              | `"TECH_BANKING"`                                   |
| `PlunderType`   | 当该区域被劫掠（Plunder）时，提供的资源类型   | `"PLUNDER_GOLD"`                                   |
| `PlunderAmount` | 该区域被掠夺时，产生的资源数量             | `50`                                               |
| `AdvisorType`   | 游戏内 **顾问（Advisor）** 提供的建议类别 | `"ADVISOR_GENERIC"`                                |

---

## **💰 生产成本相关**

| **字段**                  | **含义**                    | **示例值**                                      |
| ----------------------- | ------------------------- | -------------------------------------------- |
| `Cost`                  | **建造该区域所需的基础生产力**         | `120`                                        |
| `CostProgressioncostl`  | **成本增长模式**，决定随着游戏进程如何调整成本 | `"COST_PROGRESSION_NUM_UNDER_AVG_PLUS_TECH"` |
| `CostProgressionParam1` | **成本增长参数**，影响增长速度         | `40`                                         |
| `Maintenance`           | **每回合维护成本（金币）**           | `1`                                          |

---

## **🏛 建造与放置规则**

| **字段**               | **含义**                          | **示例值**   |
| -------------------- | ------------------------------- | --------- |
| `RequiresPlacement`  | 该区域 **是否需要占据地图上的一个格子**          | `"true"`  |
| `RequiresPopulation` | 该区域 **是否需要满足人口需求**（随城市人口增长解锁）   | `"true"`  |
| `NoAdjacentCity`     | 该区域 **是否禁止建造在邻近城市中心**           | `"false"` |
| `InternalOnly`       | 该区域 **是否只能在国内使用（无法被外交或战斗机制影响）** | `"false"` |

---

## **⚔️ 军事与掠夺**

| **字段**                       | **含义**                                        | **示例值**       |
| ---------------------------- | --------------------------------------------- | ------------- |
| `ZOC`                        | 该区域 **是否有区域控制力（Zone of Control, ZOC）**        | `"false"`     |
| `CaptureRemovesBuildings`    | **当该城市被占领时，该区域的建筑是否被移除**                      | `"false"`     |
| `CaptureRemovesCityDefenses` | **当该城市被占领时，该区域是否会导致城市失去防御能力**                 | `"false"`     |
| `MilitaryDomain`             | **该区域是否影响军事单位**（如 **空军基地** 使用 `"DOMAIN_AIR"`） | `"NO_DOMAIN"` |

---

## **🏙 影响城市属性**

| **字段**                 | **含义**                           | **示例值**      |
| ---------------------- | -------------------------------- | ------------ |
| `Appeal`               | **该区域对城市宜居度（Appeal）的影响**（值越高越宜居） | `金融中心不提供宜居度` |
| `CityStrengthModifier` | **该区域对城市防御强度的加成**（值越高防御越强）       | `2`          |

🏯亚洲国立文化中心

与金融中心学术中心不同的地方在于，该区域由市政`CIVIC_DRAMA_POETRY`解锁，所以需要将原本的`PrereqTech`改为`PrereqCivic`

| `PrereqCivic` | **解锁该区域需要的市政** | `CIVIC_DRAMA_POETRY` |
| ------------- | -------------- | -------------------- |
