
# Basic information of a company or an entity should include following information

 * 公司或组织全称 
 * 加密币名称
 * 加密币名称缩写  
 * 公司或者组织的法定代表人 
 * 公司或者组织的办公地址 
 * 公司或者组织的联系方式
 if you use invoke function getDocument(), it should return bytes that contain a json object 
 ```javascript
 {
	"EntityName":"RegTech",
	"TokenName":"Ethereum",
	"TokenShortName":"ETH",
	"LegalRepresentative":"The name of legal representative",
	"Address":"The registered address of the entity"
	"Contact":"the email or phone of entity "
 }
 ```
 -------------
 JSON schema defined as following 
 ```javascript
{
  "$schema": "http://weiresearch.com/draft-021/schema#",
  "type": "object",
  "properties": {
    "EntityName": {
      "type": "string"
    },
    "TokenName": {
      "type": "string"
    },
    "TokenShortName": {
      "type": "string"
    },
    "LegalRepresentative": {
      "type": "string"
    },
    "Address": {
      "type": "string"
    },
    "Contact": {
      "type": "string"
    }
  },
  "required": [
    "EntityName",
    "TokenName",
    "TokenShortName",
    "LegalRepresentative",
    "Address",
    "Contact"
  ]
}
  ```
 * 加密币公开转让场所：
 * 成立时间 
 * 加密币公开转让时间 
 * 主要产品与服务项目 
 * 普通股总Token数 
 * 控股股东 
 * 实际控制人 
 * 统一社会信用代码 
 * 注册资本 
 ```javascript
{
	"CryptocurrencyExchange": ["OKEX", "HUObi", "CoinBase"],
	"Established": "2018-01-01",
	"CrowdfundTime": "2019-01-01",
	"MainProductsServices": "long text field ",
	"TotalNumber": 1000000,
	"ControllingShareholder": ["Lee", "Tom", "Ryan"],
	"TheActualController": ["Lee", "Tom", "Ryan"],
	"UnifiedSocialCreditCode": "BIX3789570",
	"RegisteredCapital": {
		"Number": 100000000,
		"Currency": "CNY"
	}
}
 ```
 JSON schema defined as following
 ```javascript
{
  "$schema": "http://weiresearch.com/draft-021/schema#",
  "type": "object",
  "properties": {
    "CryptocurrencyExchange": {
      "type": "array",
      "items": [
        {
          "type": "string"
        },
        {
          "type": "string"
        },
        {
          "type": "string"
        }
      ]
    },
    "Established": {
      "type": "string"
    },
    "CrowdfundTime": {
      "type": "string"
    },
    "MainProductsServices": {
      "type": "string"
    },
    "TotalNumber": {
      "type": "integer"
    },
    "ControllingShareholder": {
      "type": "array",
      "items": [
        {
          "type": "string"
        },
        {
          "type": "string"
        },
        {
          "type": "string"
        }
      ]
    },
    "TheActualController": {
      "type": "array",
      "items": [
        {
          "type": "string"
        },
        {
          "type": "string"
        },
        {
          "type": "string"
        }
      ]
    },
    "UnifiedSocialCreditCode": {
      "type": "string"
    },
    "RegisteredCapital": {
      "type": "object",
      "properties": {
        "Number": {
          "type": "integer"
        },
        "Currency": {
          "type": "string"
        }
      },
      "required": [
        "Number",
        "Currency"
      ]
    }
  },
  "required": [
    "CryptocurrencyExchange",
    "Established",
    "CrowdfundTime",
    "MainProductsServices",
    "TotalNumber",
    "ControllingShareholder",
    "TheActualController",
    "UnifiedSocialCreditCode",
    "RegisteredCapital"
  ]
}
 ```