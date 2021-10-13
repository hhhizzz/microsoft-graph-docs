---
title: "List channels"
description: "Get a list of the channel objects and their properties."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List channels
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [channel](../resources/channel.md) objects and their properties.

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
GET /teams/{teamsId}/channels
GET /teams/{teamsId}/allChannels
GET /teams/{teamsId}/incomingChannels
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

If successful, this method returns a `200 OK` response code and a collection of [channel](../resources/channel.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_channel"
}
-->
``` http
GET https://graph.microsoft.com/beta/teams/{teamsId}/channels
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.channel)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.channel",
      "id": "4bff4816-4816-4bff-1648-ff4b1648ff4b",
      "createdDateTime": "String (timestamp)",
      "description": "String",
      "displayName": "String",
      "email": "String",
      "filesFolderWebUrl": "String",
      "isFavoriteByDefault": "Boolean",
      "membershipType": "String",
      "moderationSettings": {
        "@odata.type": "microsoft.graph.channelModerationSettings"
      },
      "tenantId": "String",
      "webUrl": "String"
    }
  ]
}
```
