---
title: "List resourceActions"
description: "Get the unifiedRbacResourceAction resources from the resourceActions navigation property."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List resourceActions
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get the unifiedRbacResourceAction resources from the resourceActions navigation property.

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
GET /unifiedRbacResourceNamespace/resourceActions
```

## Optional query parameters
This method supports some of the OData query parameters to help customize the response. For general information, see [OData query parameters](/graph/query-parameters).

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|

## Request body
Do not supply a request body for this method.

## Response

If successful, this method returns a `200 OK` response code and a collection of [unifiedRbacResourceAction](../resources/unifiedrbacresourceaction.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_unifiedrbacresourceaction"
}
-->
``` http
GET https://graph.microsoft.com/beta/unifiedRbacResourceNamespace/resourceActions
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(Microsoft.DirectoryServices.unifiedRbacResourceAction)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#Microsoft.DirectoryServices.unifiedRbacResourceAction",
      "id": "3dfb6559-6559-3dfb-5965-fb3d5965fb3d",
      "actionVerb": "String",
      "description": "String",
      "isEnabledForCustomRole": "Boolean",
      "name": "String",
      "resourceScopeId": "String"
    }
  ]
}
```
