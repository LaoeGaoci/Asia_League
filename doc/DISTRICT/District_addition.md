### 1.设置大人物点数

代码详情参考 `src/District.xml`

```xml
    <!-- 特色区域的大人物点数 -->
    <District_GreatPersonPoints>
        <Row DistrictType="DISTRICT_ASIAN_ACADEMIC_CENTER" GreatPersonClassType="GREAT_PERSON_CLASS_SCIENTIST" PointsPerTurn="2"/>
        <Row DistrictType="DISTRICT_ASIAN_CULTURAL_CENTER" GreatPersonClassType="GREAT_PERSON_CLASS_ARTIST" PointsPerTurn="2"/>
        <Row DistrictType="DISTRICT_ASIA_FINANCIAL_CENTER" GreatPersonClassType="GREAT_PERSON_CLASS_MERCHANT" PointsPerTurn="5"/>
    </District_GreatPersonPoints>
```

| DistrictType | GreatPersonClassType                              | PointsPerTurn |
| ------------ | ------------------------------------------------- | ------------- |
| 对应特色区域ID     | 选择对应的大人物<br/>如大科学家：`GREAT_PERSON_CLASS_SCIENTIST` | 提供的点数         |

### 2.设置区域相邻加成

```xml
    <!-- 特色区域的相邻加成 -->
    <District_Adjacencies>
        <Row DistrictType="DISTRICT_CAMPUS" YieldChangeId="ASIAN_ACADEMIC_CENTER_SCIENCE"/>
        <Row DistrictType="DISTRICT_THEATER" YieldChangeId="ASIAN_CULTURAL_CENTER_CULTURE"/>
        <Row DistrictType="DISTRICT_COMMERCIAL_HUB" YieldChangeId="ASIA_FINANCIAL_CENTER_GOLD"/>
    </District_Adjacencies>
```

| DistrictType | YieldChangeId |
| ------------ | ------------- |
| 对应特色区域ID     | 连接对应特性        |

```xml
    <Adjacency_YieldChanges>
        <Row ID="ASIAN_ACADEMIC_CENTER_SCIENCE" Description="LOC_DISTRICT_ASIAN_ACADEMIC_CENTER_SCIENCE" YieldType="YIELD_SCIENCE" YieldChange="2" TilesRequired="1" AdjacentDistrict="DISTRICT_ASIAN_ACADEMIC_CENTER"/>
        <Row ID="ASIAN_CULTURAL_CENTER_CULTURE" Description="LOC_DISTRICT_ASIAN_CULTURAL_CENTER_CULTURE" YieldType="YIELD_CULTURE" YieldChange="2" TilesRequired="1" AdjacentDistrict="DISTRICT_ASIAN_CULTURAL_CENTER"/>
        <Row ID="ASIA_FINANCIAL_CENTER_GOLD" Description="LOC_DISTRICT_ASIA_FINANCIAL_CENTER_GOLD" YieldType="YIELD_GOLD" YieldChange="10" TilesRequired="1" AdjacentDistrict="DISTRICT_ASIA_FINANCIAL_CENTER"/>
    </Adjacency_YieldChanges>
```

| ID   | Description | YieldType | YieldChange | TilesRequired | AdjacentDistrict |
| ---- | ----------- | --------- | ----------- | ------------- | ---------------- |
| 特性名称 | 对应本地化描述     | 加成类型      | 加成参数        | 为相邻x格提供加成     | 对应特色区域ID         |
