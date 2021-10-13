---
title: "Update externalItem"
description: "Update the properties of an externalItem object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update externalItem
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of an [externalItem](../resources/externalitem.md) object.

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
|Delegated (work or school account)|**TODO: Provide applicable permissions.**|
|Delegated (personal Microsoft account)|**TODO: Provide applicable permissions.**|
|Application|**TODO: Provide applicable permissions.**|

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /external/connections/{externalConnectionId}/items/{externalItemId}
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
[!INCLUDE [table-intro](../../includes/update-property-table-intro.md)]


|Property|Type|Description|
|:---|:---|:---|
|acl|[acl](../resources/acl.md) collection|**TODO: Add Description** Optional.|
|content|[externalItemContent](../resources/externalitemcontent.md)|**TODO: Add Description** Optional.|
|properties|[properties](../resources/properties.md)|**TODO: Add Description** Optional.|



## Response

If successful, this method returns a `200 OK` response code and an updated [externalItem](../resources/externalitem.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_externalitem"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/external/connections/{externalConnectionId}/items/{externalItemId}
Content-Type: application/json
Content-length: 284

{
  "@odata.type": "#microsoft.graph.externalItem",
  "acl": [
    {
      "@odata.type": "microsoft.graph.acl"
    }
  ],
  "content": {
    "@odata.type": "microsoft.graph.externalItemContent"
  },
  "properties": {
    "@odata.type": "microsoft.graph.properties"
  }
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.externalItem",
  "id": "4f157033-7033-4f15-3370-154f3370154f",
  "acl": [
    {
      "@odata.type": "microsoft.graph.acl"
    }
  ],
  "content": {
    "@odata.type": "microsoft.graph.externalItemContent"
  },
  "properties": {
    "@odata.type": "microsoft.graph.properties"
  }
}
```
