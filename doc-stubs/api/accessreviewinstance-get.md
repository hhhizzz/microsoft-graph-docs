---
title: "Get accessReviewInstance"
description: "Read the properties and relationships of an accessReviewInstance object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Get accessReviewInstance
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Read the properties and relationships of an [accessReviewInstance](../resources/accessreviewinstance.md) object.

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
GET /me/pendingAccessReviewInstances/{accessReviewInstanceId}
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

If successful, this method returns a `200 OK` response code and an [accessReviewInstance](../resources/accessreviewinstance.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "get_accessreviewinstance"
}
-->
``` http
GET https://graph.microsoft.com/beta/me/pendingAccessReviewInstances/{accessReviewInstanceId}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.accessReviewInstance"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.accessReviewInstance",
    "id": "c65757e6-57e6-c657-e657-57c6e65757c6",
    "customData": {
      "@odata.type": "microsoft.graph.accessReviewCustomData"
    },
    "endDateTime": "String (timestamp)",
    "errors": [
      {
        "@odata.type": "microsoft.graph.accessReviewError"
      }
    ],
    "fallbackReviewers": [
      {
        "@odata.type": "microsoft.graph.accessReviewReviewerScope"
      }
    ],
    "isDraft": "Boolean",
    "reviewers": [
      {
        "@odata.type": "microsoft.graph.accessReviewReviewerScope"
      }
    ],
    "scope": {
      "@odata.type": "microsoft.graph.accessReviewScope"
    },
    "startDateTime": "String (timestamp)",
    "status": "String"
  }
}
```
