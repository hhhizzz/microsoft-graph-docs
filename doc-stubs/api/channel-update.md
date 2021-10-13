---
title: "Update channel"
description: "Update the properties of a channel object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update channel
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [channel](../resources/channel.md) object.

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
PATCH /teams/{teamsId}/primaryChannel
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
|createdDateTime|DateTimeOffset|**TODO: Add Description** Optional.|
|description|String|**TODO: Add Description** Optional.|
|displayName|String|**TODO: Add Description** Required.|
|email|String|**TODO: Add Description** Optional.|
|filesFolderWebUrl|String|**TODO: Add Description** Optional.|
|isFavoriteByDefault|Boolean|**TODO: Add Description** Optional.|
|membershipType|channelMembershipType|**TODO: Add Description**. The possible values are: `standard`, `private`, `unknownFutureValue`, `shared`. Note that you must use the `Prefer: include - unknown -enum-members` request header to get the following value(s) in this [evolvable enum](/graph/best-practices-concept#handling-future-members-in-evolvable-enumerations): `shared`. Optional.|
|moderationSettings|[channelModerationSettings](../resources/channelmoderationsettings.md)|**TODO: Add Description** Optional.|
|tenantId|String|**TODO: Add Description** Optional.|
|webUrl|String|**TODO: Add Description** Optional.|



## Response

If successful, this method returns a `200 OK` response code and an updated [channel](../resources/channel.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_channel"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/teams/{teamsId}/primaryChannel
Content-Type: application/json
Content-length: 374

{
  "@odata.type": "#microsoft.graph.channel",
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
```
