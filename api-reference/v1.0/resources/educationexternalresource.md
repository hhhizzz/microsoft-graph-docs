---
title: "educationExternalResource resource type"
description: "A subclass of educationResource. This is the default Resource type assignments service use to map all those resources we don't expose to graph. This allows all SDK callers to work seamlessly."
ms.localizationpriority: medium
author: "cristobal-buenrostro"
ms.prod: "education"
doc_type: resourcePageType
---

# educationExternalResource resource type

Namespace: microsoft.graph

Represents a generic type to map resources not exposed in Microsoft Graph.

Inherits from [educationResource](educationresource.md).

This complex type allows all SDK callers to work seamlessly.

## Properties
| Property	   | Type	|Description|
|:---------------|:--------|:----------|
|webUrl|String|Location of the resource. Required|

## JSON representation

The following is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.educationExternalResource"
}-->

```json
{
  "webUrl": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2021-09-21 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "educationExternalResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->