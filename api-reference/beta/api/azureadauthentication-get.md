---
title: "Get azureADAuthentication"
description: "List all available Azure AD SLA performance information for the Azure AD tenant."
author: "besiler"
ms.localizationpriority: medium
ms.prod: "identity-and-access-reports"
doc_type: apiPageType
---

# Get azureADAuthentication
Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

List all available Azure AD SLA performance information for the Azure AD tenant. Azure AD SLA performance is measured by calendar month. Details on the Azure AD SLA can be found on the [Microsoft Azure SLA page](https://azure.microsoft.com/support/legal/sla/active-directory/v1_1/).

## Permissions
One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).

|Permission type|Permissions (from least to most privileged)|
|:---|:---|
| Delegated (work or school account) | AuditLog.Read.All and Directory.Read.All |
| Delegated (personal Microsoft account) | Not supported |
| Application | AuditLog.Read.All and Directory.Read.All | 

## HTTP request

<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/sla/azureADAuthentication

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

If successful, this method returns a `200 OK` response code and an [azureADAuthentication](../resources/azureadauthentication.md) object in the response body.

## Examples

### Request
The following is an example of a request.
<!-- {
  "blockType": "request",
  "name": "get_azureadauthentication"
}
-->
``` http
GET https://graph.microsoft.com/beta/reports/sla/azureADAuthentication
```


### Response
The following is an example of the response
>**Note:** The response object shown here might be shortened for readability.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.azureADAuthentication"
}
-->
``` http
HTTP/1.1 200 OK
Content-Type: application/json

{
  "value": {
    "@odata.type": "#microsoft.graph.azureADAuthentication",
    "attainments": [
      {
        "startDate": "2022-01-01",
        "endDate": "2022-01-31",
        "score": 99.993
      },
      {
        "startDate": "2022-02-01",
        "endDate": "2022-02-28",
        "score": 99.998
      }
    ]
  }
}
```

