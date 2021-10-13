---
title: "List teams"
description: "Get a list of the team objects and their properties."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List teams
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [team](../resources/team.md) objects and their properties.

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
GET /teams
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

If successful, this method returns a `200 OK` response code and a collection of [team](../resources/team.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_team"
}
-->
``` http
GET https://graph.microsoft.com/beta/teams
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.team)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.team",
      "id": "ed123398-3398-ed12-9833-12ed983312ed",
      "classification": "String",
      "createdDateTime": "String (timestamp)",
      "description": "String",
      "discoverySettings": {
        "@odata.type": "microsoft.graph.teamDiscoverySettings"
      },
      "displayName": "String",
      "funSettings": {
        "@odata.type": "microsoft.graph.teamFunSettings"
      },
      "guestSettings": {
        "@odata.type": "microsoft.graph.teamGuestSettings"
      },
      "internalId": "String",
      "isArchived": "Boolean",
      "isMembershipLimitedToOwners": "Boolean",
      "memberSettings": {
        "@odata.type": "microsoft.graph.teamMemberSettings"
      },
      "messagingSettings": {
        "@odata.type": "microsoft.graph.teamMessagingSettings"
      },
      "specialization": "String",
      "tenantId": "String",
      "visibility": "String",
      "webUrl": "String"
    }
  ]
}
```
