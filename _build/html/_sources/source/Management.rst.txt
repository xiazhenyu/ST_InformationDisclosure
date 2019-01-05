
Management Information
***********************
 #人员情况
  * 员工数量
 
 #管理层信息完备
  * 是否有董事会，监事会，股东会机制
  ** 如有此机制，每次会议决议记录
  * 高管名单，职位以及相应的社交媒体账号
  * 高管薪资水平
 
 #公司治理依据法律法规
  * 公司章程
  * 所属国家公司法
 
 .. code::json 
	
	{
		"StartDate": "2018-01-01",
		"EndDate": "2019-01-01",		
		"Staff": {
			"NumberOfEmployees": 100
		},
		"ManagementInformation": {
			"hasBoardOfDirectors": true,
			"hasBoardOfSupervisors": true,
			"hasShareholdersMeeting": false,
			"MeetingRecoreds": [{
					"name": "board of directors meeting",
					"date": "2018-01-01",
					"uri": "http://regtech.org/meeting/id/sample.txt"
				},
				{
					"name": "shareholders meeting",
					"date": "2018-01-01",
					"uri": "http://regtech.org/meeting/id/sample.txt"
				}
			],
			"ExectiveList": [{
					"Name": "Tom",
					"title": "CEO",
					"Salary": 1000.00
				},
				{
					"Name": "Jerry",
					"title": "CFO",
					"Salary": 1000.00
				}
			],
			"Compliance": [{
					"name": "Country Company Law",
					"uri": "http://regtech.org/meeting/id/sample.txt"
				},
				{
					"name": "the articles of incorporation",
					"uri": "http://regtech.org/meeting/id/sample.txt"
				}
			]
		}
	}
    ..
	
	JSON Schema
	
	.. code:: json
	
	{
	  "$schema": "http://weiresearch.com/draft-021/schema#",
	  "type": "object",
	  "properties": {
		"StartDate": {
		  "type": "string"
		},
		"EndDate": {
		  "type": "string"
		},
		"Staff": {
		  "type": "object",
		  "properties": {
			"NumberOfEmployees": {
			  "type": "integer"
			}
		  },
		  "required": [
			"NumberOfEmployees"
		  ]
		},
		"ManagementInformation": {
		  "type": "object",
		  "properties": {
			"hasBoardOfDirectors": {
			  "type": "boolean"
			},
			"hasBoardOfSupervisors": {
			  "type": "boolean"
			},
			"hasShareholdersMeeting": {
			  "type": "boolean"
			},
			"MeetingRecoreds": {
			  "type": "array",
			  "items": [
				{
				  "type": "object",
				  "properties": {
					"name": {
					  "type": "string"
					},
					"date": {
					  "type": "string"
					},
					"uri": {
					  "type": "string"
					}
				  },
				  "required": [
					"name",
					"date",
					"uri"
				  ]
				},
				{
				  "type": "object",
				  "properties": {
					"name": {
					  "type": "string"
					},
					"date": {
					  "type": "string"
					},
					"uri": {
					  "type": "string"
					}
				  },
				  "required": [
					"name",
					"date",
					"uri"
				  ]
				}
			  ]
			},
			"ExectiveList": {
			  "type": "array",
			  "items": [
				{
				  "type": "object",
				  "properties": {
					"Name": {
					  "type": "string"
					},
					"title": {
					  "type": "string"
					},
					"Salary": {
					  "type": "number"
					}
				  },
				  "required": [
					"Name",
					"title",
					"Salary"
				  ]
				},
				{
				  "type": "object",
				  "properties": {
					"Name": {
					  "type": "string"
					},
					"title": {
					  "type": "string"
					},
					"Salary": {
					  "type": "number"
					}
				  },
				  "required": [
					"Name",
					"title",
					"Salary"
				  ]
				}
			  ]
			},
			"Compliance": {
			  "type": "array",
			  "items": [
				{
				  "type": "object",
				  "properties": {
					"name": {
					  "type": "string"
					},
					"uri": {
					  "type": "string"
					}
				  },
				  "required": [
					"name",
					"uri"
				  ]
				},
				{
				  "type": "object",
				  "properties": {
					"name": {
					  "type": "string"
					},
					"uri": {
					  "type": "string"
					}
				  },
				  "required": [
					"name",
					"uri"
				  ]
				}
			  ]
			}
		  },
		  "required": [
			"hasBoardOfDirectors",
			"hasBoardOfSupervisors",
			"hasShareholdersMeeting",
			"MeetingRecoreds",
			"ExectiveList",
			"Compliance"
		  ]
		}
	  },
	  "required": [
		"StartDate",
		"EndDate",
		"Staff",
		"ManagementInformation"
	  ]
	}
	
 ..