# LW_CONTRACT_SINGLE_VESSEL（劳务经营合同-单船协议标准子表）

> 主键：**ID**　|　业务字段 8 个，公共字段 10 个（BaseDomain）

## 索引

| 索引名 | 字段 |
|--------|------|
| IDX_LW_CSV_CONTRACT | `CONTRACT_ID, IS_VOID` |
| IDX_LW_CSV_INFO | `VESSEL_INFO_ID` |

## 业务字段

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **ID** 🔑PK | VARCHAR2(32) | N |  | 主键 |
| 2 | **CONTRACT_ID** ⬅外键 | VARCHAR2(32) | Y |  | 劳务经营合同ID(LW_CONTRACT.ID) |
| 3 | **VESSEL_INFO_ID** ⬅外键 | VARCHAR2(32) | Y |  | 船舶子表ID(LW_CONTRACT_VESSEL_INFO.ID) |
| 4 | **VESSEL_CODE** | VARCHAR2(20) | Y |  | 船舶代码 |
| 5 | **VESSEL_NAME** | VARCHAR2(50) | Y |  | 船舶名称 |
| 6 | **START_DATE** | DATE | Y |  | 生效日期 |
| 7 | **MONTHLY_AGREEMENT_FEE** | NUMBER(18, 2) | Y |  | 月度单船协议费用 |
| 8 | **REMARK** | VARCHAR2(500) | Y |  | 备注 |

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
