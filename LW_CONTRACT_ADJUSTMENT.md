# LW_CONTRACT_ADJUSTMENT（调补维护（无固定核算标准的费用手工录入））

> 主键：**ID**　|　业务字段 13 个，公共字段 10 个（BaseDomain）

## 业务字段

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **ID** 🔑PK | VARCHAR2(32 CHAR) | N |  | 主键ID |
| 2 | **ADJUST_YEAR** | VARCHAR2(4 CHAR) | Y |  | 年（yyyy，如 2026） |
| 3 | **ADJUST_MONTH** | VARCHAR2(2 CHAR) | Y |  | 月（MM，补零两位，如 06） |
| 4 | **EMP_NO** | VARCHAR2(20 CHAR) | Y |  | 工号 |
| 5 | **EMP_NAME** | VARCHAR2(100 CHAR) | Y |  | 姓名 |
| 6 | **POSITION_CODE** | VARCHAR2(20 CHAR) | Y |  | 职务代码（CDM_POSITION.POSITION_CODE） |
| 7 | **VESSEL_CODE** | VARCHAR2(20 CHAR) | Y |  | 船舶代码（SMM_VESSEL.VESSEL_CODE） |
| 8 | **FEE_TYPE** | VARCHAR2(30 CHAR) | Y |  | 协议费用项目（字典CATEGORY=LW_ADJUST_FEE_TYPE：1=调补项目/2=其他项目） |
| 9 | **PROJECT_CODE** | VARCHAR2(50 CHAR) | Y |  | 项目（调补项目取字典LW_APPOINT_TO，其他项目取字典LW_OTHER，按FEE_TYPE联动） |
| 10 | **CURRENCY_CODE** | VARCHAR2(20 CHAR) | Y |  | 币种（字典CATEGORY=CURRENCY） |
| 11 | **AMOUNT** | NUMBER(18,2) | Y |  | 金额 |
| 12 | **IMPORT_BATCH** | VARCHAR2(32 CHAR) | Y |  | 导入批次号（yyyyMMddHHmmss），导入时自动生成，用于按批次批量删除 |
| 13 | **REMARK** | VARCHAR2(2000 CHAR) | Y |  | 备注 |

<details><summary>公共字段（BaseDomain，所有表一致）</summary>

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **VERSION** | NUMBER(19) | Y |  | 版本号 |
| 2 | **OFFICE_CODE** | VARCHAR2(20 CHAR) | Y |  | 机构编码 |
| 3 | **CREATE_BY** | VARCHAR2(64 CHAR) | Y |  | 创建人ID |
| 4 | **CREATE_TIME** | TIMESTAMP(6) | Y |  | 创建时间 |
| 5 | **UPDATE_BY** | VARCHAR2(64 CHAR) | Y |  | 更新人ID |
| 6 | **UPDATE_TIME** | TIMESTAMP(6) | Y |  | 更新时间 |
| 7 | **IS_VOID** | NUMBER(10) | Y |  | 是否作废(0-否 1-是) |
| 8 | **LOC_TIME_ZONE** | VARCHAR2(36 CHAR) | Y |  | 时区 |
| 9 | **CREATE_BY_NAME** | VARCHAR2(40 CHAR) | Y |  | 创建人姓名 |
| 10 | **UPDATE_BY_NAME** | VARCHAR2(40 CHAR) | Y |  | 更新人姓名 |

</details>
