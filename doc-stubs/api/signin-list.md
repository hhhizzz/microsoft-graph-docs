---
title: "List signIns"
description: "Get a list of the signIn objects and their properties."
author: "**TODO: Provide Github Name. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
ms.localizationpriority: medium
ms.prod: "**TODO: Add MS prod. See [topic-level metadata reference](https://msgo.azurewebsites.net/add/document/guidelines/metadata.html#topic-level-metadata)**"
doc_type: apiPageType
---

# List signIns
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Get a list of the [signIn](../resources/signin.md) objects and their properties.

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
GET /auditLogs/signIns
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

If successful, this method returns a `200 OK` response code and a collection of [signIn](../resources/signin.md) objects in the response body.

## Examples

### Request
<!-- {
  "blockType": "request",
  "name": "list_signin"
}
-->
``` http
GET https://graph.microsoft.com/beta/auditLogs/signIns
```


### Response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Collection(microsoft.graph.signIn)"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.signIn",
      "id": "040bde92-de92-040b-92de-0b0492de0b04",
      "appDisplayName": "String",
      "appId": "String",
      "appliedConditionalAccessPolicies": [
        {
          "@odata.type": "microsoft.graph.appliedConditionalAccessPolicy"
        }
      ],
      "authenticationDetails": [
        {
          "@odata.type": "microsoft.graph.authenticationDetail"
        }
      ],
      "authenticationMethodsUsed": [
        "String"
      ],
      "authenticationProcessingDetails": [
        {
          "@odata.type": "microsoft.graph.keyValue"
        }
      ],
      "authenticationProtocol": "String",
      "authenticationRequirement": "String",
      "authenticationRequirementPolicies": [
        {
          "@odata.type": "microsoft.graph.authenticationRequirementPolicy"
        }
      ],
      "autonomousSystemNumber": "Integer",
      "clientAppUsed": "String",
      "conditionalAccessStatus": "String",
      "correlationId": "String",
      "createdDateTime": "String (timestamp)",
      "crossTenantAccessType": "String",
      "deviceDetail": {
        "@odata.type": "microsoft.graph.deviceDetail"
      },
      "flaggedForReview": "Boolean",
      "homeTenantId": "String",
      "homeTenantName": "String",
      "incomingTokenType": "String",
      "ipAddress": "String",
      "ipAddressFromResourceProvider": "String",
      "isInteractive": "Boolean",
      "isTenantRestricted": "Boolean",
      "location": {
        "@odata.type": "microsoft.graph.signInLocation"
      },
      "mfaDetail": {
        "@odata.type": "microsoft.graph.mfaDetail"
      },
      "networkLocationDetails": [
        {
          "@odata.type": "microsoft.graph.networkLocationDetail"
        }
      ],
      "originalRequestId": "String",
      "privateLinkDetails": {
        "@odata.type": "microsoft.graph.privateLinkDetails"
      },
      "processingTimeInMilliseconds": "Integer",
      "resourceDisplayName": "String",
      "resourceId": "String",
      "resourceTenantId": "String",
      "riskDetail": "String",
      "riskEventTypes_v2": [
        "String"
      ],
      "riskLevelAggregated": "String",
      "riskLevelDuringSignIn": "String",
      "riskState": "String",
      "servicePrincipalCredentialKeyId": "String",
      "servicePrincipalCredentialThumbprint": "String",
      "servicePrincipalId": "String",
      "servicePrincipalName": "String",
      "sessionLifetimePolicies": [
        {
          "@odata.type": "microsoft.graph.sessionLifetimePolicy"
        }
      ],
      "signInEventTypes": [
        "String"
      ],
      "signInIdentifier": "String",
      "signInIdentifierType": "String",
      "status": {
        "@odata.type": "microsoft.graph.signInStatus"
      },
      "tokenIssuerName": "String",
      "tokenIssuerType": "String",
      "uniqueTokenIdentifier": "String",
      "userAgent": "String",
      "userDisplayName": "String",
      "userId": "String",
      "userPrincipalName": "String",
      "userType": "String"
    }
  ]
}
```
