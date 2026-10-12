# LW_CONTRACT（劳务经营合同主表）

> 主键：**ID**　|　业务字段 58 个，公共字段 10 个（BaseDomain）

## 索引

| 索引名 | 字段 |
|--------|------|
| IDX_LW_CONTRACT_NO | `CONTRACT_NO, IS_VOID` |
| IDX_LW_CONTRACT_EFF | `EFFECTIVE_DATE` |

## 业务字段

| # | 字段 | 类型 | 可空 | 默认 | 说明 |
|---|------|------|:--:|------|------|
| 1 | **ID** 🔑PK | VARCHAR2(32) | N |  | 主键 |
| 2 | **CONTRACT_NO** | VARCHAR2(100) | Y |  | 合同编号 |
| 3 | **CONTRACT_NAME** | VARCHAR2(500) | Y |  | 合同名称 |
| 4 | **SEAMAN_DB_BLOCK** | VARCHAR2(50) | Y |  | 板块(字典 CTS_SETTLEMENT_BLOCK) |
| 5 | **PARTY_A** | VARCHAR2(255) | Y |  | 合同甲方 |
| 6 | **PARTY_B** | VARCHAR2(255) | Y |  | 合同乙方 |
| 7 | **PARTY_C** | VARCHAR2(255) | Y |  | 合同丙方 |
| 8 | **PARTY_D** | VARCHAR2(255) | Y |  | 合同丁方 |
| 9 | **SIGNING_DATE** | DATE | Y |  | 签署日期 |
| 10 | **EFFECTIVE_DATE** | DATE | Y |  | 合同生效日期 |
| 11 | **EXPIRY_DATE** | DATE | Y |  | 合同终止日期(失效日期) |
| 12 | **EXPIRATION_DATE** | VARCHAR2(100) | Y |  | 合同有效期(描述) |
| 13 | **EXPIRATION_PERIOD_MONTH** | VARCHAR2(20) | Y |  | 有效期(月) |
| 14 | **EXTENSION_CLAUSE** | VARCHAR2(50) | Y |  | 延期条款(字典 EXTENSION_CLAUSE) |
| 15 | **VALUE_ADDED_TAX** | NUMBER(1) | Y |  | 是否含税(0-否 1-是) |
| 16 | **CONTRACT_CHARACTER** | VARCHAR2(50) | Y |  | 合同性质(字典 CONTRACT_CHARACTER) |
| 17 | **CONTRACT_TEXT_TYPE** | VARCHAR2(50) | Y |  | 合同文本类型(字典 CONTRACT_TEXT_TYPE) |
| 18 | **SIGNATORY** | VARCHAR2(100) | Y |  | 合同签署人 |
| 19 | **ORGANIZER** | VARCHAR2(64) | Y |  | 承办单位 |
| 20 | **DEPARTMENT** | VARCHAR2(100) | Y |  | 承办部门 |
| 21 | **UNDERTAKER** | VARCHAR2(64) | Y |  | 承办人 |
| 22 | **BUSINESS_KEY** | VARCHAR2(255) | Y |  | 附件 |
| 23 | **RELIEVE_DATE** | DATE | Y |  | 解除日期 |
| 24 | **DISPUTE_DATE** | DATE | Y |  | 争议日期 |
| 25 | **DISPUTE_CASE** | VARCHAR2(1000) | Y |  | 争议情况 |
| 26 | **SETTLE_AMOUNT** | NUMBER(18,2) | Y |  | 合同结算额 |
| 27 | **CURRENCY_CODE** | VARCHAR2(20) | Y |  | 结算币种(字典 CURRENCY) |
| 28 | **SETTLE_TYPE** | VARCHAR2(20) | Y |  | 结算类型(FIXED_30-月固定天数(30) ACTUAL-月实际天数) |
| 29 | **SIGNED_CREATE_BY** | VARCHAR2(64) | Y |  | 签署日期首次设置-创建人 |
| 30 | **SIGNED_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 签署日期首次设置-创建人名称 |
| 31 | **SIGNED_CREATE_TIME** | DATE | Y |  | 签署日期首次设置-创建时间 |
| 32 | **SIGNED_UPDATE_BY** | VARCHAR2(64) | Y |  | 签署日期变更-更新人 |
| 33 | **SIGNED_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 签署日期变更-更新人名称 |
| 34 | **SIGNED_UPDATE_TIME** | DATE | Y |  | 签署日期变更-更新时间 |
| 35 | **EFFICIENT_CREATE_BY** | VARCHAR2(64) | Y |  | 生效日期首次设置-创建人 |
| 36 | **EFFICIENT_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 生效日期首次设置-创建人名称 |
| 37 | **EFFICIENT_CREATE_TIME** | DATE | Y |  | 生效日期首次设置-创建时间 |
| 38 | **EFFICIENT_UPDATE_BY** | VARCHAR2(64) | Y |  | 生效日期变更-更新人 |
| 39 | **EFFICIENT_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 生效日期变更-更新人名称 |
| 40 | **EFFICIENT_UPDATE_TIME** | DATE | Y |  | 生效日期变更-更新时间 |
| 41 | **LIFTED_CREATE_BY** | VARCHAR2(64) | Y |  | 解除日期首次设置-创建人 |
| 42 | **LIFTED_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 解除日期首次设置-创建人名称 |
| 43 | **LIFTED_CREATE_TIME** | DATE | Y |  | 解除日期首次设置-创建时间 |
| 44 | **LIFTED_UPDATE_BY** | VARCHAR2(64) | Y |  | 解除日期变更-更新人 |
| 45 | **LIFTED_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 解除日期变更-更新人名称 |
| 46 | **LIFTED_UPDATE_TIME** | DATE | Y |  | 解除日期变更-更新时间 |
| 47 | **DISPUTE_CREATE_BY** | VARCHAR2(64) | Y |  | 争议日期首次设置-创建人 |
| 48 | **DISPUTE_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 争议日期首次设置-创建人名称 |
| 49 | **DISPUTE_CREATE_TIME** | DATE | Y |  | 争议日期首次设置-创建时间 |
| 50 | **DISPUTE_UPDATE_BY** | VARCHAR2(64) | Y |  | 争议日期变更-更新人 |
| 51 | **DISPUTE_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 争议日期变更-更新人名称 |
| 52 | **DISPUTE_UPDATE_TIME** | DATE | Y |  | 争议日期变更-更新时间 |
| 53 | **TERMINATION_CREATE_BY** | VARCHAR2(64) | Y |  | 终止日期首次设置-创建人 |
| 54 | **TERMINATION_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 终止日期首次设置-创建人名称 |
| 55 | **TERMINATION_CREATE_TIME** | DATE | Y |  | 终止日期首次设置-创建时间 |
| 56 | **TERMINATION_UPDATE_BY** | VARCHAR2(64) | Y |  | 终止日期变更-更新人 |
| 57 | **TERMINATION_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 终止日期变更-更新人名称 |
| 58 | **TERMINATION_UPDATE_TIME** | DATE | Y |  | 终止日期变更-更新时间 |

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
