# Hackntu_x_Cathay_2017

## dataset (for preview purpose)

### profile
| field            | type   | Description              |
|------------------|--------|--------------------------|
| customer_id      | String | 客戶 ID                  |
| birth_time       | Long   | 出生時間戳記              |
| gender           | String | 性別                     |
| contact_loc      | String | 居住地區                  |
| contact_code     | String | 居住地區郵遞區號代碼       |
| register_loc     | String | 戶籍地區                  |
| register_code    | String | 戶籍地區郵遞區號代碼     |
| start_time       | Long   | 起始往來時間戳記         |
| aum              | Double | 近三個月平均的總資產餘額 |
| net_profit       | Double | 近一年淨收益             |
| credit_card_flag | String | 是否有信用卡產品往來     |
| loan_flag        | String | 是否有貸款產品往來       |
| deposit_flag     | String | 是否有存款產品往來       |
| wealth_flag      | String | 是否有理財產品往來       |
| partition_time   | Long   | snapshot時間戳記     |

### event
#### themes
* cctxn
* atm
* cti
* mybank

| field          | type   | description                          |
|----------------|--------|--------------------------------------|
| actor_type     | String | 值皆是"customer_id"                  |
| actor_id       | String | 行為者ID                             |
| action_type    | String | 行為類型                             |
| action_time    | Long   | 行為發生時間戳記                     |
| object_type    | String | 影響物件類型                         |
| object_id      | String | 影響物件ID                           |
| channel_type   | String | 通路類型                             |
| channel_id     | String | 通路ID                               |
| attrs          | String | 補充資料 - JSON string               |
| theme          | String | 主題 - cc_txn, atm, cti, mybank      |
| partition_time | Long   | 最近上一區段時間戳記 (可串連profile) |

## example
* Wrangling data with Apache Spark

## other reference
* [Python+Spark 2.0+Hadoop 機器學習與大數據分析實戰](https://www.tenlong.com.tw/products/9789864341535)
* [Learning Spark](http://shop.oreilly.com/product/0636920028512.do)
