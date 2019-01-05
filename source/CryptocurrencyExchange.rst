
Cryptocurrency Exchange
***********************

# Cryptocurrency exchange information show the inital plan of distribution for the security token
 If you use invoke function getDocument(), it should return bytes that contain a json object 
 
 * 加密币公开转让场所：
 * 成立时间 
 * 加密币公开转让时间 
 * 主要产品与服务项目 
 * 普通股总Token数 
 * 控股股东 
 * 实际控制人 
 * 统一社会信用代码 
 * 注册资本 
 
 .. code:: json
	
	{
		"CryptocurrencyExchange": ["OKEX", "Huobi", "CoinBase"],
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
	
 ..
 
 JSON schema
 
 .. code:: json
	 
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
 
 ..