## ES mappings最佳实践

基于ES 7.x版本：
```
PUT http://10.10.6.85:9200/dev_product_info
{
    "settings":{
        "number_of_shards":3,
        "number_of_replicas":1,
        "refresh_interval":"10s"
    },
    "mappings":{
        "dynamic":false,
        "properties":{
            "id":{
                "type":"long"
            },
            "supplierSn":{
                "type":"keyword"
            },
            "productName":{
                "type":"text",
                "analyzer":"ik_max_word",
                "search_analyzer":"ik_smart"
            },
            "brandName":{
                "type":"text",
                "analyzer":"ik_max_word",
                "search_analyzer":"ik_smart"
            },
            "productCode":{
                "type":"text"
            },
            "firstCategoryId":{
                "type":"integer"
            },
            "firstCategoryName":{
                "type":"text",
                "index" : false
            },
            "secondaryCategoryId":{
                "type":"integer"
            },
            "secondaryCategoryName":{
                "type":"text",
                "index" : false 
            },
            "thirdCategoryId":{
                "type":"integer"
            },
            "thirdCategoryName":{
                "type":"text",
                "index" : false 
            },
            "supplierSpuCode":{
                "type":"keyword"
            },
            "supplierSkuCode":{
                "type":"keyword"
            },
            "spuCode":{
                "type":"keyword"
            },
            "skuCode":{
                "type":"keyword"
            },
            "productSpec":{
                "type":"text",
                "index" : false
            },
            "sellingPrice":{
                "type":"double"
            },
            "taxCostPrice":{
                "type":"double"
            },
            "costPrice":{
                "type":"double"
            },
            "taxRate":{
                "type":"double"
            },
            "salesDesc":{
                "type":"text",
                "index" : false
            },
            "supplierInvoiceType":{
                "type":"integer"
            },
            "notDeliveryRange":{
                "type":"text",
                "index" : false
            },
            "supplierSettlementPrice":{
                "type":"double"
            },
            "referCostPriceBase":{
                "type":"double"
            },
            "shopCostPriceBase":{
                "type":"double"
            },
            "submitTime":{
                "type":"date",
                "format":"yyyy-MM-dd HH:mm:ss"
            },
            "isUniformPrice":{
                "type":"integer"
            },
            "isPutawayInfoComplete":{
                "type":"integer"
            },
            "putawayEnable":{
                "type":"integer"
            },
            "refundAddress":{
                "type":"text",
                "index" : false
            },
            "deliveryCycle":{
                "type":"text",
                "index" : false
            },
            "version":{
                "type":"integer"
            },
            "createTime":{
                "type":"date",
                "format":"yyyy-MM-dd HH:mm:ss||epoch_millis"
            },
            "updateTime":{
                "type":"date",
                "format":"yyyy-MM-dd HH:mm:ss||epoch_millis"
            }
        }
    }
}
```
