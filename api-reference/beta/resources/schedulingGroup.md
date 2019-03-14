---
title: "schedulingGroup resource type"
description: "A logical grouping of members in the schedule (usually by role)."
author: "nkramer"
localization_priority: Priority
ms.prod: "microsoft-teams"
---

# schedulingGroup resource type

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

A logical grouping of members in the schedule (usually by role). 

## Methods

| Method       | Return Type  |Description|
|:---------------|:--------|:----------|
|[Create schedulingGroup](../api/schedule-post-schedulinggroup.md) | [schedulingGroup](schedulinggroup.md) | Create a new `schedulingGroup`.|
|[List schedulingGroup](../api/schedule-list-schedulinggroups.md) | [schedulingGroup](schedulinggroup.md) collection | Get the list of `schedulingGroups` in this schedule.|
|[Get schedulingGroup](../api/schedule-get-schedulinggroups.md) | [schedulingGroup](schedulinggroup.md) | Get a `schedulingGroup` by ID.|
|[Update schedulingGroup](../api/schedule-put-schedulinggroups.md) | [schedulingGroup](schedulinggroup.md) | Update a `schedulingGroup`.|
|[Delete schedulingGroup](../api/schedule-delete-schedulinggroups.md) | None | Marks a `schedulingGroup` as inactive.|

## Properties
|Name          |Type           |Description                                                                                 |
|--------------|---------------|--------------------------------------------------------------------------------------------|
| id			| `string`      |Id of the `schedulingGroup`.|
| displayName   | `string`      | The display name for the `schedulingGroup`.      |
| isActive 			|`bool`      | Indicates if the `schedulingGroup` can be used when creating new entities or updating existing ones.|
| userIds 		| `collection(string)`    |  The list of user ids that are a member of the `schedulingGroup`. |
| createdDateTime		|`DateTimeOffset`        |The time stamp in which this `schedulingGroup` was first created.|
| lastModifiedDateTime		|`DateTimeOffset`        |The time stamp in which this `schedulingGroup` was last updated.|
| lastModifiedBy		|`microsoft.graph.identitySet`        |The identity that last updated this `schedulingGroup`.|

## JSON representation

Here is a JSON representation of the resource.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.schedulingGroup"
}-->

```json
{
  "id": "string",
  "displayName": "string",
  "isActive": true,
  "userIds": [
    "string"
  ],
  "createdDateTime": "2018-10-04T00:58:45.340Z",
  "lastModifiedDateTime": "2018-10-04T00:58:45.340Z",
  "lastModifiedBy": {
    "user": {
      "id": "string",
      "displayName": "string"
    },
    "application": {
      "id": "string",
      "displayName": "string"
    },
    "device": {
      "id": "string",
      "displayName": "string"
    }
  }
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "schedulingGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/schedulinggroup.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->