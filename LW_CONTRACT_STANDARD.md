# LW_CONTRACT_STANDARD（劳务经营合同-标准子表）

> 主键：**ID**　|　业务字段 8 个，公共字段 10 个（BaseDomain）

## 索引

| 索引名 | 字段 |
|--------|------|
| IDX_LW_CS_CONTRACT | `CONTRACT_ID, IS_VOID` |

## 业务字段

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **ID** 🔑PK | VARCHAR2(32) | N |  | 主键 |
| 2 | **CONTRACT_ID** | VARCHAR2(32) | Y |  | 劳务经营合同ID(LW_CONTRACT.ID) |
| 3 | **STANDARD_NAME** | VARCHAR2(255) | Y |  | 标准名称 |
| 4 | **AGREEMENT_TYPE** | VARCHAR2(30) | Y |  | 协议方式(SINGLE_VESSEL-单船协议标准 SINGLE_POST-单岗协议标准) |
| 5 | **HK_PROJECT_CODES** | VARCHAR2(500) | Y |  | 香港公司项目(字典 LW_HK_PROJECT 编码，多个以英文逗号分隔) |
| 6 | **UNIFORM_ISSUE_MODE** | VARCHAR2(20) | Y |  | 制服费发放方式(ONBOARD-上船发放 OFFBOARD-下船发放) |
| 7 | **CURRENCY_CODE** | VARCHAR2(20) | Y |  | 标准币种(字典 CURRENCY) |
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
