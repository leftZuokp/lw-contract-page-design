# LW_CONTRACT_VESSEL_INFO（劳务经营合同-船舶子表）

> 主键：**ID**　|　业务字段 5 个，公共字段 10 个（BaseDomain）

## 索引

| 索引名 | 字段 |
|--------|------|
| IDX_LW_CVI_CONTRACT | `CONTRACT_ID, IS_VOID` |
| IDX_LW_CVI_VESSEL | `VESSEL_CODE` |

## 业务字段

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **ID** 🔑PK | VARCHAR2(32) | N |  | 主键 |
| 2 | **CONTRACT_ID** | VARCHAR2(32) | Y |  | 劳务经营合同ID(LW_CONTRACT.ID) |
| 3 | **VESSEL_CODE** | VARCHAR2(20) | Y |  | 船舶代码 |
| 4 | **VESSEL_NAME** | VARCHAR2(50) | Y |  | 船舶名称 |
| 5 | **PRINCIPAL_CODE** | VARCHAR2(20) | Y |  | 主结算单位 |

<details><summary>公共字段（BaseDomain，所有表一致）</summary>

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **OFFICE_CODE** | VARCHAR2(64) | Y |  | 机构编码 |
| 2 | **CREATE_BY** | VARCHAR2(64) | Y |  | 创建人ID |
| 3 | **CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 创建人姓名 |
| 4 | **CREATE_TIME** | DATE | Y |  | 创建时间 |
| 5 | **UPDATE_BY** | VARCHAR2(64) | Y |  | 更新人ID |
| 6 | **UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 更新人姓名 |
| 7 | **UPDATE_TIME** | DATE | Y |  | 更新时间 |
| 8 | **LOC_TIME_ZONE** | VARCHAR2(64) | Y |  | 时区 |
| 9 | **IS_VOID** | NUMBER(1) | Y | 0 | 是否作废(0-否 1-是) |
| 10 | **VERSION** | NUMBER(19) | Y | 0 | 版本号 |

</details>
