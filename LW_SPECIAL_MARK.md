# LW_SPECIAL_MARK（船员特殊标记（特殊维护页面））

> 主键：**ID**　|　业务字段 10 个，公共字段 10 个（BaseDomain）

## 索引

| 索引名 | 字段 |
|--------|------|
| IDX_LSM_EMP | `EMP_NO, START_DATE` |
| IDX_LSM_VESSEL | `VESSEL_CODE, IS_VOID` |
| IDX_LSM_MARK | `IS_VOID, SPECIAL_MARK` |
| IDX_LSM_BATCH | `IMPORT_BATCH_NO, IS_VOID` |

## 业务字段

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **ID** 🔑PK | VARCHAR2(32 CHAR) | N |  | 主键ID |
| 2 | **VESSEL_CODE** | VARCHAR2(20 CHAR) | Y |  | 船舶代码 |
| 3 | **EMP_NO** | VARCHAR2(20 CHAR) | Y |  | 工号 |
| 4 | **EMP_NAME** | VARCHAR2(100 CHAR) | Y |  | 姓名 |
| 5 | **POSITION_CODE** | VARCHAR2(20 CHAR) | Y |  | 现任职务 |
| 6 | **START_DATE** | TIMESTAMP(6) | Y |  | 开始日期 |
| 7 | **END_DATE** | TIMESTAMP(6) | Y |  | 结束日期，为空表示长期有效 |
| 8 | **SPECIAL_MARK** | VARCHAR2(20 CHAR) | Y |  | 特殊标记（字典CATEGORY=BUSINESS_CONTRACT_MARK的CODE） |
| 9 | **IMPORT_BATCH_NO** | VARCHAR2(32 CHAR) | Y |  | 导入批次号，导入时自动生成，用于批量删除 |
| 10 | **REMARK** | VARCHAR2(2000 CHAR) | Y |  | 备注 |

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
