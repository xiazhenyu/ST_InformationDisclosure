
Litigations
***********************

我们会关注公司或组织的法律诉讼情况。以公司运营主体和实际控制人，高级管理人员的涉诉情况，需要公开。
 
 * 是否有涉诉情况
 * 具体涉诉情况公告

.. code:: json
	
	litigation
	{
		"litigations": [{
				"name": "",
				"date": "2018-08-08",
				"uri": "http://legal.org/information/?id=1234"
			},
			{
				"name": "",
				"date": "2018-09-09",
				"uri": "http://legal.org/information/?id=5678"
			}
		]
	}
	
..

.. code:: json

	{
	  "$schema": "http://weiresearch.com/draft-021/schema#",
	  "type": "object",
	  "properties": {
		"litigations": {
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
		}
	  },
	  "required": [
		"litigations"
	  ]
	}

..