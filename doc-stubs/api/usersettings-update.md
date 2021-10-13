---
title: "Update userSettings"
description: "Update the properties of a userSettings object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Update userSettings
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Update the properties of a [userSettings](../resources/usersettings.md) object.

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
PATCH /me/settings
PATCH /users/{usersId}/settings
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
|contributionToContentDiscoveryAsOrganizationDisabled|Boolean|**TODO: Add Description** Required.|
|contributionToContentDiscoveryDisabled|Boolean|**TODO: Add Description** Required.|



## Response

If successful, this method returns a `200 OK` response code and an updated [userSettings](../resources/usersettings.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "update_usersettings"
}
-->
``` http
PATCH https://graph.microsoft.com/beta/me/settings
Content-Type: application/json
Content-length: 180

{
  "@odata.type": "#microsoft.graph.userSettings",
  "contributionToContentDiscoveryAsOrganizationDisabled": "Boolean",
  "contributionToContentDiscoveryDisabled": "Boolean"
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
  "@odata.type": "#microsoft.graph.userSettings",
  "id": "99d62a35-2a35-99d6-352a-d699352ad699",
  "contributionToContentDiscoveryAsOrganizationDisabled": "Boolean",
  "contributionToContentDiscoveryDisabled": "Boolean"
}
```
