---
title: "CreateItemResponseMessage"
 
 
manager: sethgros
ms.date: 9/17/2015
ms.audience: Developer
ms.topic: reference
 
localization_priority: Normal
api_name:
- CreateItemResponseMessage
api_type:
- schema
ms.assetid: 595d36c2-f87a-4d50-8e8b-f58d7641564b
description: "The CreateItemResponseMessage element contains the status and result of a single CreateItem operation request."
---

# CreateItemResponseMessage

The **CreateItemResponseMessage** element contains the status and result of a single [CreateItem operation](createitem-operation.md) request. 
  
[CreateItemResponse](createitemresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[CreateItemResponseMessage](createitemresponsemessage.md)
  
```
<CreateItemResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Items/>
</CreateItemResponseMessage>
```

 **ItemInfoResponseMessageType**
## Attributes and elements

The following sections describe attributes, child elements, and parent elements.
  
#### Attributes

|**Attribute**|**Description**|
|:-----|:-----|
|**ResponseClass** <br/> | Describes the status of a [CreateItem operation](createitem-operation.md) response. The following values are valid for this attribute:  <br/>  Success  <br/>  Warning  <br/>  Error  <br/> |
   
#### ResponseClass Attribute Values

|**Value**|**Description**|
|:-----|:-----|
|**Success** <br/> |Describes a request that is fulfilled.  <br/> |
|**Warning** <br/> | Describes a request that was not processed. A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed. The following are examples of sources of warnings:  <br/>  The Exchange store is offline during the batch.  <br/>  Active Directory Domain Services (AD DS) is offline.  <br/>  Mailboxes are moved.  <br/>  The message database (MDB) is offline.  <br/>  A password is expired.  <br/>  A quota is exceeded.  <br/> |
|**Error** <br/> | Describes a request that cannot be fulfilled. The following are examples of sources of errors:  <br/>  Invalid attributes or elements  <br/>  Attributes or elements out of range  <br/>  Unknown tag  <br/>  Attribute or element not valid in the context  <br/>  Unauthorized access attempt by any client  <br/>  Server-side failure in response to a valid client-side call  <br/>  Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.  <br/> |
   
#### Child elements

|**Element**|**Description**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Provides a text description of the status of the response.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Provides an error code that identifies the specific error that the request encountered.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Currently unused and is reserved for future use. It contains a value of 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Provides additional error response information.  <br/> |
|[Items](items.md) <br/> |Contains an array of created items.  <br/> |
   
#### Parent elements

|**Element**|**Description**|
|:-----|:-----|
|[ResponseMessages](responsemessages.md) <br/> |Contains the response messages for an Exchange Web Services request.  <br/> |
   
## Remarks

The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.
  
## Element information

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Schema Name  <br/> |Messages schema  <br/> |
|Validation File  <br/> |Messages.xsd  <br/> |
|Can be Empty  <br/> |False  <br/> |
   
## See also

#### Reference

[CreateItem operation](createitem-operation.md)
#### Concepts

[EWS reference for Exchange](ews-reference-for-exchange.md)
  
[EWS XML elements in Exchange](ews-xml-elements-in-exchange.md)
