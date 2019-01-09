---

eip: ERC-ST-D001
title: Base on International Financial Reporting Standards to do information diclosure
author: xiazy@weiresearch
discussions-to: #
status: Draft
type: Standards Track
category: ERC
created: 2018-12-28
require: None

---

## Simple Summary

This standard sits under the ERC-1400 (#1411) umbrella set of standards related to security tokens.

Provides a standard to support information disclosure on tokens.

## Abstract

Allows information of token issue entity information be disclosed for investers.

## Motivation

Since security tokens are subject to regulatory and legal oversight (the details of which will vary depending on jurisdiction, regulatory framework and underlying asset) 

Investors need a easy way to check financial report, management team, and litigation report of the company or the entity.  

## Requirements

See ERC-1400 or ERC-20 for a full set of requirements across the library of standards.

The following requirements have been compiled following discussions with parties across the Security Token ecosystem.

- MUST be able to perform forced transfer for legal action or fund recovery.


## Rationale

Investors can continue to check updated information on the issuer. The invested company or organization is obliged to disclose its true information in a timely manner.

## Specification

This standard will try to meet the legal information disclosure system in different countries.

#### hasBasicInformation

This function return false means no legal representive or organization register information available. return true means invoke function getBasicaInformation() will return related information

``` solidity
function function hasBasicInformation() external view returns (bool)
```

#### hasFinancialReport

This function return false means no financial report available. return true means invoke function getFinancialReport() will return related information

``` solidity
function hasFinancialReport() external view returns (bool)
```


#### hasManagementReport

This function return false means no management report available. return true means invoke function getManagementReport() will return related information

``` solidity
function hasManagementReport() external view returns (bool)
```

#### hasLitigationDisclosure

This function return false means no litigation information available. return true means invoke function getLitigationReport() will return related information

``` solidity
function getLitigationReport() external view returns (bool)
```

#### hasLitigationDisclosure

This function return false means no litigation information available. return true means invoke function getLitigationReport() will return related information

``` solidity
function getLitigationReport() external view returns (bool)
```

#### hasLitigationDisclosure

This function return false means no litigation information available. return true means invoke function getLitigationReport() will return related information

``` solidity
function getLitigationReport() external view returns (bool)
```

#### setBasicaInformation

Used to attach a organization document the contract, or update the URI or hash of an existing attached document.

setBasicaInformation MUST throw if the document is not successfully stored.

setBasicaInformation MUST emit a DocumentUpdated event with details of the document being attached or modified.

``` solidity
function setBasicaInformation(bytes32 _name, string _uri, bytes32 _documentHash) external;
```

#### getBasicaInformation

Used to return the details of a document with a known name (bytes32). Returns the URI associated with the document (string), the hash (of the contents) of the document (bytes32), and the timestamp at which the document was last modified via setFinancialReport (uint256).

``` solidity
function getBasicaInformation(bytes32 _name, string _uri, bytes32 _documentHash) external;
```


#### setFinancialReport

Used to attach a new financial report to the contract, or update the URI or hash of an existing attached document.

setFinancialReport MUST throw if the document is not successfully stored.

setFinancialReport MUST emit a DocumentUpdated event with details of the document being attached or modified.

``` solidity
function setFinancialReport(bytes32 _name, string _uri, bytes32 _documentHash) external;
```

#### getFinancialReport

Used to return the details of a document with a known name (bytes32). Returns the URI associated with the document (string), the hash (of the contents) of the document (bytes32), and the timestamp at which the document was last modified via setFinancialReport (uint256).

``` solidity
function getFinancialReport(bytes32 _name, string _uri, bytes32 _documentHash) external;
```


#### setManagementReport

Used to attach a new management report to the contract, or update the URI or hash of an existing attached document.

setManagementReport MUST throw if the document is not successfully stored.

setManagementReport MUST emit a DocumentUpdated event with details of the document being attached or modified.

``` solidity
function setManagementReport(bytes32 _name, string _uri, bytes32 _documentHash) external;
```

#### getManagementReport

Used to return the details of a document with a known name (bytes32). Returns the URI associated with the document (string), the hash (of the contents) of the document (bytes32), and the timestamp at which the document was last modified via setManagementReport (uint256).

``` solidity
function ManagementReport(bytes32 _name, string _uri, bytes32 _documentHash) external;
```


#### setLitigationReport

Used to attach a new  iltigation report to the contract, or update the URI or hash of an existing attached document.

LitigationReport MUST throw if the document is not successfully stored.

LitigationReport MUST emit a DocumentUpdated event with details of the document being attached or modified.

``` solidity
function LitigationReport(bytes32 _name, string _uri, bytes32 _documentHash) external;
```

#### getLitigationReport

Used to return the details of a document with a known name (bytes32). Returns the URI associated with the document (string), the hash (of the contents) of the document (bytes32), and the timestamp at which the document was last modified via setFinancialReport (uint256).

``` solidity
function getLitigationReport(bytes32 _name, string _uri, bytes32 _documentHash) external;
```


#### isControllable

In order to provide transparency over whether `controllerTransfer` / `controllerRedeem` are useable, the function `isControllable` can be used.

If a token returns FALSE for `isControllable()` then it MUST:
  - always return FALSE in the future.
  - `controllerTransfer` must revert
  - `controllerRedeem` must revert  

In other words, if an issuer sets `isControllable` to return FALSE, then there can be no further controller transactions for this token contract.
`controllerRedeem` MUST emit a `ControllerRedemption` event.
``` solidity
function isControllable() external view returns (bool);
```

## Interface

``` solidity
/// @title International Financial Reporting Standards, information  (part of the ERC1400 Security Token Standards)
/// @dev See https://github.com/SecurityTokenStandard/EIP-Spec
/// Reference https://www.growthforce.com/blog/financial-reports-management-reports-differences

interface IERCxxxx is IERC20 {

    // Regular Operation
	function hasBasicInformation() external view returns (bool);

	//      Profit and Loss Statement
    //      Balance Sheet
    //      Accounts Payable
    //      Accounts Receivable
    //      Statement of Cash Flows
	function hasFinancialReport() external view returns (bool);
	//  Optional
	//      Profit and Loss by Class  
	//      Department
    //       Team
    //       Job
    //      Realization Rate     
    //      Utilization Rate
	function hasManagementReport() external view returns (bool);
	//  Optional 
	//      pending
	//      completed
	function hasLitigationDisclosure() external view returns (bool);

	
	function setBasicaInformation(bytes32 _name, string _uri, bytes32 _documentHash) external;
    // Document Management
    function getBasicaInformation(bytes32 _name) external view returns (string, bytes32, uint256);
	
	
	function setBasicaInformation(bytes32 _name, string _uri, bytes32 _documentHash) external;
    // Document Management
    function getBasicaInformation(bytes32 _name) external view returns (string, bytes32, uint256);

	
	function setFinancialReport(bytes32 _name, string _uri, bytes32 _documentHash) external;
    // Document Management
    function getFinancialReport(bytes32 _name) external view returns (string, bytes32, uint256);
	
	function setManagementReport(bytes32 _name, string _uri, bytes32 _documentHash) external;
    // Document Management
    function getManagementReport(bytes32 _name) external view returns (string, bytes32, uint256);


	function setLitigationReport(bytes32 _name, string _uri, bytes32 _documentHash) external;
    // Document Management
    function getLitigationReport(bytes32 _name) external view returns (string, bytes32, uint256);
	

}
```

## References
- [EIP 1400: Security Token Standard With Partitions](https://github.com/ethereum/EIPs/issues/1411)
- [EIP Draft](https://github.com/SecurityTokenStandard/EIP-Spec)
