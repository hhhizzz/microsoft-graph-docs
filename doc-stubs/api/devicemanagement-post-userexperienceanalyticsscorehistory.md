---
title: "Create userExperienceAnalyticsScoreHistory"
description: "Create a new userExperienceAnalyticsScoreHistory object."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# Create userExperienceAnalyticsScoreHistory
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Create a new [userExperienceAnalyticsScoreHistory](../resources/userexperienceanalyticsscorehistory.md) object.

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
POST /deviceManagement/userExperienceAnalyticsScoreHistory
```

## Request headers
|Name|Description|
|:---|:---|
|Authorization|Bearer {token}. Required.|
|Content-Type|application/json. Required.|

## Request body
In the request body, supply a JSON representation of the [userExperienceAnalyticsScoreHistory](../resources/userexperienceanalyticsscorehistory.md) object.

You can specify the following properties when creating a **userExperienceAnalyticsScoreHistory**.

|Property|Type|Description|
|:---|:---|:---|
|appHealthOverallScore|Int32|The User experience analytics app health overall score. Required.|
|appHealthTotalDevices|Int32|The total device count of the user experience analytics category app health. Required.|
|coreBootScore|Int32|The user experience analytics device core boot score. Score will be in the range 0-100, 100 is the ideal score. Required.|
|coreSigninScore|Int32|The User experience analytics device core sign-in score. Score will be in the range 0-100, 100 is the ideal score. Required.|
|overallScore|Int32|User experience analytics overall score. Score will be in the range 0-100, 100 is the ideal score. Valid values 0 to 100 Required.|
|recommendedSoftwareScore|Int32|The User experience analytics device core sign-in score. Score will be in the range 0-100, 100 is the ideal score. Required.|
|recommendedSoftwareTotalDevices|Int32|The total device count of the user experience analytics category recommended software. Required.|
|restartScore|Int32|Restart score. Score will be in the range 0-100, 100 is the ideal score, 0 indicates excessive restarts. Valid values 0 to 9999999 Required.|
|startupDateTime|DateTimeOffset|The user experience analytics device startup date time. Required.|
|startupScore|Int32|User experience analytics device startup score. Score will be in the range 0-100, 100 is the ideal score. Required.|
|startupTotalDevices|Int32|The total device count of the user experience analytics category startup performance. Required.|



## Response

If successful, this method returns a `201 Created` response code and a [userExperienceAnalyticsScoreHistory](../resources/userexperienceanalyticsscorehistory.md) object in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "create_userexperienceanalyticsscorehistory_from_"
}
-->
``` http
POST https://graph.microsoft.com/beta/deviceManagement/userExperienceAnalyticsScoreHistory
Content-Type: application/json
Content-length: 481

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsScoreHistory",
  "appHealthOverallScore": "Integer",
  "appHealthTotalDevices": "Integer",
  "coreBootScore": "Integer",
  "coreSigninScore": "Integer",
  "overallScore": "Integer",
  "recommendedSoftwareScore": "Integer",
  "recommendedSoftwareTotalDevices": "Integer",
  "restartScore": "Integer",
  "startupDateTime": "String (timestamp)",
  "startupScore": "Integer",
  "startupTotalDevices": "Integer"
}
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.userExperienceAnalyticsScoreHistory"
}
-->
``` http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "@odata.type": "#microsoft.graph.userExperienceAnalyticsScoreHistory",
  "id": "7bec31c3-31c3-7bec-c331-ec7bc331ec7b",
  "appHealthOverallScore": "Integer",
  "appHealthTotalDevices": "Integer",
  "coreBootScore": "Integer",
  "coreSigninScore": "Integer",
  "overallScore": "Integer",
  "recommendedSoftwareScore": "Integer",
  "recommendedSoftwareTotalDevices": "Integer",
  "restartScore": "Integer",
  "startupDateTime": "String (timestamp)",
  "startupScore": "Integer",
  "startupTotalDevices": "Integer"
}
```
