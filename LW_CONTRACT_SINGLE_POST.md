# LW_CONTRACT_SINGLE_POST（劳务经营合同-单岗协议标准子表）

> 主键：**ID**　|　业务字段 19 个，公共字段 10 个（BaseDomain）

## 索引

| 索引名 | 字段 |
|--------|------|
| IDX_LW_CSP_CONTRACT | `CONTRACT_ID, IS_VOID` |
| IDX_LW_CSP_STANDARD | `STANDARD_ID` |

## 业务字段

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **ID** 🔑PK | VARCHAR2(32) | N |  | 主键 |
| 2 | **CONTRACT_ID** | VARCHAR2(32) | Y |  | 劳务经营合同ID(LW_CONTRACT.ID) |
| 3 | **STANDARD_ID** | VARCHAR2(32) | Y |  | 标准子表ID(LW_CONTRACT_STANDARD.ID) |
| 4 | **START_DATE** | DATE | Y |  | 生效日期 |
| 5 | **POSITION_CODE** | VARCHAR2(20) | Y |  | 职务编码 |
| 6 | **POSITION_NAME** | VARCHAR2(50) | Y |  | 职务名称 |
| 7 | **IS_NEW_METHOD** | NUMBER(1) | Y |  | 新人新办法(0-否 1-是) |
| 8 | **IS_FOREIGN** | NUMBER(1) | Y |  | 是否外籍(0-否 1-是) |
| 9 | **BASE_SALARY** | NUMBER(18,2) | Y |  | 基薪(船员薪水) |
| 10 | **TRAVEL_SALARY** | NUMBER(18,2) | Y |  | 路途薪(出入境工资) |
| 11 | **LEAVE_ASSESS_BONUS** | NUMBER(18,2) | Y |  | 离船考核奖(完成合同奖) |
| 12 | **SUPPLIER_RETURN_BONUS** | NUMBER(18,2) | Y |  | 供方老手返船奖(船员回流奖) |
| 13 | **AGENCY_FEE** | NUMBER(18,2) | Y |  | 代理费 |
| 14 | **MANAGEMENT_FEE** | NUMBER(18,2) | Y |  | 管理费 |
| 15 | **ASSEMBLY_FEE** | NUMBER(18,2) | Y |  | 集结包干费 |
| 16 | **UNIFORM_FEE** | NUMBER(18,2) | Y |  | 制服费(劳保费) |
| 17 | **TRAINING_FEE** | NUMBER(18,2) | Y |  | 培训费 |
| 18 | **FOOD_FEE** | NUMBER(18,2) | Y |  | 伙食费 |
| 19 | **REMARK** | VARCHAR2(500) | Y |  | 备注 |

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
