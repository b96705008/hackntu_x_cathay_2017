# Hackntu_x_Cathay_2017
* Thanks for everyone's attending!

## introduction(pdf)
* 資料介紹 
* 方向建議與實作
* 商業分析 

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

#### sample
```
1,1871111837,F,D,181903,F,373933,3320438400,1217.1769900503969,528.7309192220683,Y,Y,N,N,3696969600
```

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
| partition_time | Long   | 最近上一區段時間戳記 (可串連profile) |
| theme          | String | 主題 - cc_txn, atm, cti, mybank      |

#### sample
```
customer_id,17,inquire,3696970704,saving_acct,MJQXLDJMQQOYAPFBBPBS,ATM,NCZHYDSTABCUAXLYJLQZ,"{\"action\": {\"txn_amt\": 0.0, \"txn_fee_amt\": 0.0, \"trans_type\": \"trans_out\"}, \"object\": {\"target_bank_code\": \"B_bank\", \"target_acct_nbr\": \"UMOTEPKACILAPBIKOYHZ\"}, \"channel\": {\"address_zipcode\": 601401, \"machine_bank_code\": \"C_bank\"}}",3696969600,atm
```

## example
* Easy Profiling
* Wrangling data with Apache Spark

## Already installed libraries in VM
### Python 2.7
#### sklearn, numpy, pandas, jupyter, networkx, keras, tensorflow, flask, django, xgboost
### R 3.3.3
#### xgboost
### Java 1.7
### Spark 2.1
### node.js
### IDE
#### sublime, pycharm, Rstudio

## other reference
### Credit Card 
* [MCC codes](https://github.com/b96705008/mcc-codes)

### Spark 
* [Python+Spark 2.0+Hadoop 機器學習與大數據分析實戰](https://www.tenlong.com.tw/products/9789864341535)

* [Learning Spark](http://shop.oreilly.com/product/0636920028512.do)
* [Spark RDD minibatch for Deep learning](https://github.com/b96705008/pyspark-dl-utils/blob/master/example/Minibatch.ipynb) - Welcome for refining
* [R on Spark](http://spark.apache.org/docs/latest/sparkr.html)

### Python 
* [Hands-On Machine Learning with Scikit-Learn and TensorFlow](http://shop.oreilly.com/product/0636920052289.do)
