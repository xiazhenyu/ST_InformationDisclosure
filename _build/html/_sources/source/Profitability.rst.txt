
Profitability
***********************
 # 盈利能力
  * 营业收入 Operating income is similar to a company's earnings before interest and taxes (EBIT) and is also referred to as the operating profit or recurring profit. The one big difference between operating income and EBIT is that EBIT includes any non-operating income the company generates 
  * 毛利率 Gross profit is the profit a company makes after deducting the costs associated with making and selling its products, or the costs associated with providing its services. Gross profit will appear on a company's income statement, and can be calculated with this formula: Gross profit = Revenue  
  * 归属于投资者的净利润 NetProfit
  
 .. code:: json
 
	Profitability
	{
		"StartDate": "2018-01-01",
		"EndDate": "2019-01-01",
		"Currency": "USD",
		"OperatingIncome": 100000.0000,
		"GrossProfit": 100000.0000,
		"NetProfit": 100000.0000
	}
 
 ..
 
  
 # 偿债能力
 ## 资产总计
  * Cash and cash equivalents
  * 应收账款 Accounts receivable 
    refers to the outstanding invoices a company has or the money clients owe the company. The phrase refers to accounts a business has a right to receive because it has delivered a product or service
  
  * 存货 Inventory
  * 长期股权投资
  * 固定资产
  * 可供出售金融资产
  
 ## 负债总计
  * 在建工程 
   Construction Work-in-Progress is a long-term asset account in which the costs of constructing long-term assets are recorded. The account Construction Work-in-Progress will have a debit balance and will be reported on the balance sheet as part of a company's Property, Plant and Equipment.
  * 短期借款
  * 长期借款
  
 ## 归属于投资者的净资产 
  Shareholders' equity is the net amount of a company's total assets and total liabilities, which are listed on a company's balance sheet. In part, shareholders' equity shows how much of a company's operations is financed by equity. Shareholders' equity is the net amount of a company's total assets and total liabilities, which are listed on a company's balance sheet. In part, shareholders' equity shows how much of a company's operations is financed by equity.   
 
 .. code:: json  
	
	Solvency
	{
		"Currency": "USD",
		"StartDate": "2018-01-01",
		"EndDate": "2019-01-01",
		"Assets": {
			"TotalAssets": 100000.0000,
			"CashAndCashEquivalents": 100000.0000,
			"AccountsReceivable": 100000.0000,
			"Inventory": 100000.0000,
			"Long-termEquityInvestment": 100000.0000,
			"FixedAssets": 100000.0000,
			"AvailableForSaleFinancialAssets": 100000.0000
		},
		"Liabilities": {
			"TotalLiabilities": 100000.0000,
			"ConstructionInProgress": 100000.0000,
			"ShortTermLoan": 100000.0000,
			"LongTermLoan": 100000.0000
		},
		"ShareholdersEquity": 100000.0000
	}
	
 ..	
 
 Schema
 
 .. code:: json

	{
	  "$schema": "http://weiresearch.com/draft-021/schema#",
	  "type": "object",
	  "properties": {
		"Currency": {
		  "type": "string"
		},
		"StartDate": {
		  "type": "string"
		},
		"EndDate": {
		  "type": "string"
		},
		"Assets": {
		  "type": "object",
		  "properties": {
			"TotalAssets": {
			  "type": "number"
			},
			"CashAndCashEquivalents": {
			  "type": "number"
			},
			"AccountsReceivable": {
			  "type": "number"
			},
			"Inventory": {
			  "type": "number"
			},
			"Long-termEquityInvestment": {
			  "type": "number"
			},
			"FixedAssets": {
			  "type": "number"
			},
			"AvailableForSaleFinancialAssets": {
			  "type": "number"
			}
		  },
		  "required": [
			"TotalAssets",
			"CashAndCashEquivalents",
			"AccountsReceivable",
			"Inventory",
			"Long-termEquityInvestment",
			"FixedAssets",
			"AvailableForSaleFinancialAssets"
		  ]
		},
		"Liabilities": {
		  "type": "object",
		  "properties": {
			"TotalLiabilities": {
			  "type": "number"
			},
			"ConstructionInProgress": {
			  "type": "number"
			},
			"ShortTermLoan": {
			  "type": "number"
			},
			"LongTermLoan": {
			  "type": "number"
			}
		  },
		  "required": [
			"TotalLiabilities",
			"ConstructionInProgress",
			"ShortTermLoan",
			"LongTermLoan"
		  ]
		},
		"ShareholdersEquity": {
		  "type": "number"
		}
	  },
	  "required": [
		"Currency",
		"StartDate",
		"EndDate",
		"Assets",
		"Liabilities",
		"ShareholdersEquity"
	  ]
	}
 .. 

 # 营运情况
 ## 利润构成
    * 营业收入
    * 营业成本
    * 毛利率
    * 管理费用
    * 销售费用
    * 财务费用
    * 营业利润
    * 营业外收入
    * 营业外支出
    * 净利润
  
 ## 收入构成
  * 主营业务收入
  * 其他业务收入
  
 ## 现金流量状况
  * 经营活动产生的现金流量净额
  * 投资活动产生的现金流量净额
  * 筹资活动产生的现金流量净额

  .. code:: json
	 
	Operational situation
	 {
		"Currency": "USD",
		"StartDate": "2018-01-01",
		"EndDate": "2019-01-01",	
		"ProfitComposition": {
			"OperatingIncome": 100000.0000,
			"OperatingCost": 100000.0000,
			"GrossProfit": 100000.0000,
			"ManagementCosts": 100000.0000,
			"SalesExpense": 100000.0000,
			"FinancialExpenses": 100000.0000,
			"OperatingProfit": 100000.0000,
			"Non-operatingIncome": 100000.0000,
			"OperatingExpenses": 100000.0000,
			"NetProfit": 100000.0000
		},
		"IncomeComposition": {
			"MainBusinessIncome": 100000.0000,
			"OtherOperatingIncome": 100000.0000
		},
		"CashFlowStatus": {
			"NetCashFlowFromOperatingActivities": 100000.0000,
			"NetCashFlowsFromInvestingActivities": 100000.0000,
			"NetCashFlowFromFinancingActivities": 100000.0000
		}
	 }
 
 .. 
 
 JSON Schema
 
 .. code:: json
	 
	 {
	  "$schema": "http://weiresearch.com/draft-021/schema#",
	  "type": "object",
	  "properties": {
		"ProfitComposition": {
		  "type": "object",
		  "properties": {
			"OperatingIncome": {
			  "type": "number"
			},
			"OperatingCost": {
			  "type": "number"
			},
			"GrossProfit": {
			  "type": "number"
			},
			"ManagementCosts": {
			  "type": "number"
			},
			"SalesExpense": {
			  "type": "number"
			},
			"FinancialExpenses": {
			  "type": "number"
			},
			"OperatingProfit": {
			  "type": "number"
			},
			"Non-operatingIncome": {
			  "type": "number"
			},
			"OperatingExpenses": {
			  "type": "number"
			},
			"NetProfit": {
			  "type": "number"
			}
		  },
		  "required": [
			"OperatingIncome",
			"OperatingCost",
			"GrossProfit",
			"ManagementCosts",
			"SalesExpense",
			"FinancialExpenses",
			"OperatingProfit",
			"Non-operatingIncome",
			"OperatingExpenses",
			"NetProfit"
		  ]
		},
		"IncomeComposition": {
		  "type": "object",
		  "properties": {
			"MainBusinessIncome": {
			  "type": "number"
			},
			"OtherOperatingIncome": {
			  "type": "number"
			}
		  },
		  "required": [
			"MainBusinessIncome",
			"OtherOperatingIncome"
		  ]
		},
		"CashFlowStatus": {
		  "type": "object",
		  "properties": {
			"NetCashFlowFromOperatingActivities": {
			  "type": "number"
			},
			"NetCashFlowsFromInvestingActivities": {
			  "type": "number"
			},
			"NetCashFlowFromFinancingActivities": {
			  "type": "number"
			}
		  },
		  "required": [
			"NetCashFlowFromOperatingActivities",
			"NetCashFlowsFromInvestingActivities",
			"NetCashFlowFromFinancingActivities"
		  ]
		}
	  },
	  "required": [
		"ProfitComposition",
		"IncomeComposition",
		"CashFlowStatus"
	  ]
	 }
 ..
 
