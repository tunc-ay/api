## Retrieves the account details, such as subscription start and end date, in Netsparker.
Description: This endpoint lets you retrieve your account information in Netsparker.
## URL
GET https://www.netsparkercloud.com/api/1.0/account/license

## Headers
| Header Name | Description | Required | Values | Notes |
| --- | --- |  --- | --- | --- |
| Authorization | the authorization method | required |  | Basic Authentication |
| Accept | the format of the data to be returned | required |  | application/json |

## Sample Request
```javascript
GET https://www.netsparkercloud.com/api/1.0/account/license
```
## Sample Response
 ```javascript
{
  "SubscriptionMaximumSiteLimit": 8,
  "SubscriptionSiteCount": 8,
  "SubscriptionEndDate": "12/30/2022 04:00 PM",
  "SubscriptionStartDate": "03/02/2020 04:00 PM",
  "IsAccountWhitelisted": true,
  "UsedScanCreditCount": 0,
  "ScanCreditCount": 0,
  "IsCreditScanEnabled": false,
  "IsSubscriptionEnabled": true,
  "PreVerifiedWebsites": [],
  "Licenses": [
    {
      "EndDate": "2022-12-30T21:00:00+00:00",
      "MaximumSiteLimit": 8,
      "ProductDefinition": "Team",
      "StartDate": "2020-03-02T21:00:00+00:00",
      "ValidForDays": 1033,
      "Id": "a08b2a8e-d131-46f3-cacd-ab7301d92d86",
      "IsActive": true,
      "Key": "CP0NDY7L291PTT4082GBD64KUTKY6WDW",
      "AccountCanCreateSharkScanTask": false
    }
  ]
}
```
## Response
| Parameter | Description | Type | Notes |
| --- | --- | --- | --- | --- |

  ## Status Code and Errors
| Code | Description |  Notes |
| --- | --- |  --- |
| 200 | OK |  Success |
| 401 | Unauthorized |  The access is denied |
| 404 | Not Found |  Invalid type. |
