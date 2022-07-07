---
title: "serviceLevelAgreementAttainment resource type"
description: "Provides the SLA performance for an Azure AD tenant for one calendar month"
author: "besiler"
ms.localizationpriority: medium
ms.prod: "identity-and-access-reports"
doc_type: resourcePageType
---

# serviceLevelAgreementAttainment resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Provides the SLA performance for an Azure AD tenant for one calendar month. The month represented is identified by the startDate and endDate properties, which always align with the beginning and end of a calendar month. 

## Properties
|Property|Type|Description|
|:---|:---|:---|
|endDate|Date|The last day of the calendar month measured for SLA performance.|
|score|Double|The SLA performance for the Azure AD tenant for the calendar month. The score is given in percentage points and truncated at five digits. The value in score is never rounded up. Therefore, a score of 99.999 means that SLA performance for the month was greater than or equal to 99.999%. |
|startDate|Date|The first day of the calendar month measured for SLA performance.|

## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.serviceLevelAgreementAttainment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.serviceLevelAgreementAttainment",
  "startDate": "Date",
  "endDate": "Date",
  "score": "Double"
}
```

