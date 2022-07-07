---
title: "azureADAuthentication resource type"
description: "Provides Azure AD SLA performance for each calendar month for an Azure AD tenant"
author: "besiler"
ms.localizationpriority: medium
ms.prod: "identity-and-access-reports"
doc_type: resourcePageType
---

# azureADAuthentication resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Provides Azure AD SLA performance for your tenant for each calendar month. Details on the Azure AD SLA can be found on the [Microsoft Azure SLA page](https://azure.microsoft.com/support/legal/sla/active-directory/v1_1/). 


Inherits from [entity](../resources/entity.md).

## Methods
|Method|Return type|Description|
|:---|:---|:---|
|[Get azureADAuthentication](../api/azureadauthentication-get.md)|[azureADAuthentication](../resources/azureadauthentication.md)|Returns a collection of [serviceLevelAgreementAttainment](../resources/servicelevelagreementattainment.md) resources, which describe the Azure AD tenant's SLA performance for each calendar month.|


## Properties
|Property|Type|Description|
|:---|:---|:---|
|attainments|[serviceLevelAgreementAttainment](../resources/servicelevelagreementattainment.md) collection|A collection of [serviceLevelAgreementAttainment](../resources/servicelevelagreementattainment.md) resources, each of which describes the SLA performance for one calendar month for the Azure AD tenant.|


## Relationships
None.

## JSON representation
The following is a JSON representation of the resource.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.azureADAuthentication",
  "baseType": "microsoft.graph.entity",
  "openType": false
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.azureADAuthentication",
  "attainments": [
    {
      "@odata.type": "microsoft.graph.serviceLevelAgreementAttainment"
    }
  ]
}
```

