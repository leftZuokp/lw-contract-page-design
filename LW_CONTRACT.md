# LW_CONTRACT（劳务经营合同主表）

> 主键：**ID**　|　业务字段 66 个，公共字段 10 个（BaseDomain）

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
| 26 | **SETTLE_AMOUNT** | NUMBER(18, 2) | Y |  | 合同结算额 |
| 27 | **SETTLE_UNIT** | VARCHAR2(255) | Y |  | 结算单位 |
| 28 | **SETTLE_CYCLE** | VARCHAR2(20) | Y |  | 结算周期(MONTH-月结 QUARTER-季结 HALF_YEAR-半年结 YEAR-年结) |
| 29 | **CURRENCY_CODE** | VARCHAR2(20) | Y |  | 结算币种(字典 CURRENCY) |
| 30 | **SETTLE_TYPE** | VARCHAR2(20) | Y |  | 结算类型(FIXED_30-月固定天数(30) ACTUAL-月实际天数) |
| 31 | **PAYMENT_METHOD** | VARCHAR2(50) | Y |  | 付款方式(字典 LW_PAYMENT_METHOD) |
| 32 | **INVOICE_TYPE** | VARCHAR2(50) | Y |  | 发票类型(字典 LW_INVOICE_TYPE) |
| 33 | **STANDARD_NAME** | VARCHAR2(255) | Y |  | 标准名称 |
| 34 | **AGREEMENT_TYPE** | VARCHAR2(30) | Y |  | 协议方式(SINGLE_VESSEL-单船协议标准 SINGLE_POST-单岗协议标准) |
| 35 | **HK_PROJECT_CODES** | VARCHAR2(500) | Y |  | 香港公司项目(字典 LW_HK_PROJECT 编码，多个以英文逗号分隔) |
| 36 | **STANDARD_REMARK** | VARCHAR2(500) | Y |  | 标准备注 |
| 37 | **SIGNED_CREATE_BY** | VARCHAR2(64) | Y |  | 签署日期首次设置-创建人 |
| 38 | **SIGNED_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 签署日期首次设置-创建人名称 |
| 39 | **SIGNED_CREATE_TIME** | DATE | Y |  | 签署日期首次设置-创建时间 |
| 40 | **SIGNED_UPDATE_BY** | VARCHAR2(64) | Y |  | 签署日期变更-更新人 |
| 41 | **SIGNED_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 签署日期变更-更新人名称 |
| 42 | **SIGNED_UPDATE_TIME** | DATE | Y |  | 签署日期变更-更新时间 |
| 43 | **EFFICIENT_CREATE_BY** | VARCHAR2(64) | Y |  | 生效日期首次设置-创建人 |
| 44 | **EFFICIENT_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 生效日期首次设置-创建人名称 |
| 45 | **EFFICIENT_CREATE_TIME** | DATE | Y |  | 生效日期首次设置-创建时间 |
| 46 | **EFFICIENT_UPDATE_BY** | VARCHAR2(64) | Y |  | 生效日期变更-更新人 |
| 47 | **EFFICIENT_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 生效日期变更-更新人名称 |
| 48 | **EFFICIENT_UPDATE_TIME** | DATE | Y |  | 生效日期变更-更新时间 |
| 49 | **LIFTED_CREATE_BY** | VARCHAR2(64) | Y |  | 解除日期首次设置-创建人 |
| 50 | **LIFTED_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 解除日期首次设置-创建人名称 |
| 51 | **LIFTED_CREATE_TIME** | DATE | Y |  | 解除日期首次设置-创建时间 |
| 52 | **LIFTED_UPDATE_BY** | VARCHAR2(64) | Y |  | 解除日期变更-更新人 |
| 53 | **LIFTED_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 解除日期变更-更新人名称 |
| 54 | **LIFTED_UPDATE_TIME** | DATE | Y |  | 解除日期变更-更新时间 |
| 55 | **DISPUTE_CREATE_BY** | VARCHAR2(64) | Y |  | 争议日期首次设置-创建人 |
| 56 | **DISPUTE_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 争议日期首次设置-创建人名称 |
| 57 | **DISPUTE_CREATE_TIME** | DATE | Y |  | 争议日期首次设置-创建时间 |
| 58 | **DISPUTE_UPDATE_BY** | VARCHAR2(64) | Y |  | 争议日期变更-更新人 |
| 59 | **DISPUTE_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 争议日期变更-更新人名称 |
| 60 | **DISPUTE_UPDATE_TIME** | DATE | Y |  | 争议日期变更-更新时间 |
| 61 | **TERMINATION_CREATE_BY** | VARCHAR2(64) | Y |  | 终止日期首次设置-创建人 |
| 62 | **TERMINATION_CREATE_BY_NAME** | VARCHAR2(64) | Y |  | 终止日期首次设置-创建人名称 |
| 63 | **TERMINATION_CREATE_TIME** | DATE | Y |  | 终止日期首次设置-创建时间 |
| 64 | **TERMINATION_UPDATE_BY** | VARCHAR2(64) | Y |  | 终止日期变更-更新人 |
| 65 | **TERMINATION_UPDATE_BY_NAME** | VARCHAR2(64) | Y |  | 终止日期变更-更新人名称 |
| 66 | **TERMINATION_UPDATE_TIME** | DATE | Y |  | 终止日期变更-更新时间 |

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
