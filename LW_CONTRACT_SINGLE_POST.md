# LW_CONTRACT_SINGLE_POST（劳务经营合同-单岗协议标准子表）

> 主键：**ID**　|　业务字段 22 个，公共字段 10 个（BaseDomain）

## 索引

| 索引名 | 字段 |
|--------|------|
| IDX_LW_CSP_CONTRACT | `CONTRACT_ID, IS_VOID` |
| IDX_LW_CSP_INFO | `VESSEL_INFO_ID` |

## 业务字段

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **ID** 🔑PK | VARCHAR2(32) | N |  | 主键 |
| 2 | **CONTRACT_ID** ⬅外键 | VARCHAR2(32) | Y |  | 劳务经营合同ID(LW_CONTRACT.ID) |
| 3 | **VESSEL_INFO_ID** ⬅外键 | VARCHAR2(32) | Y |  | 船舶子表ID(LW_CONTRACT_VESSEL_INFO.ID) |
| 4 | **VESSEL_CODE** | VARCHAR2(20) | Y |  | 船舶代码 |
| 5 | **VESSEL_NAME** | VARCHAR2(50) | Y |  | 船舶名称 |
| 6 | **START_DATE** | DATE | Y |  | 生效日期 |
| 7 | **POSITION_CODE** | VARCHAR2(20) | Y |  | 职务编码 |
| 8 | **POSITION_NAME** | VARCHAR2(50) | Y |  | 职务名称 |
| 9 | **IS_NEW_METHOD** | NUMBER(1) | Y |  | 新人新办法(0-否 1-是) |
| 10 | **IS_FOREIGN** | NUMBER(1) | Y |  | 是否外籍(0-否 1-是) |
| 11 | **BASE_SALARY** | NUMBER(18, 2) | Y |  | 基薪(船员薪水) |
| 12 | **TRAVEL_SALARY** | NUMBER(18, 2) | Y |  | 路途薪(出入境工资) |
| 13 | **LEAVE_ASSESS_BONUS** | NUMBER(18, 2) | Y |  | 离船考核奖(完成合同奖) |
| 14 | **OVERDUE_SUBSIDY** | NUMBER(18, 2) | Y |  | 超期补贴(船员超期奖) |
| 15 | **SUPPLIER_RETURN_BONUS** | NUMBER(18, 2) | Y |  | 供方老手返船奖(船员回流奖) |
| 16 | **AGENCY_FEE** | NUMBER(18, 2) | Y |  | 代理费 |
| 17 | **MANAGEMENT_FEE** | NUMBER(18, 2) | Y |  | 管理费 |
| 18 | **ASSEMBLY_FEE** | NUMBER(18, 2) | Y |  | 集结包干费 |
| 19 | **UNIFORM_FEE** | NUMBER(18, 2) | Y |  | 制服费(劳保费) |
| 20 | **TRAINING_FEE** | NUMBER(18, 2) | Y |  | 培训费 |
| 21 | **FOOD_FEE** | NUMBER(18, 2) | Y |  | 伙食费 |
| 22 | **REMARK** | VARCHAR2(500) | Y |  | 备注 |

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
