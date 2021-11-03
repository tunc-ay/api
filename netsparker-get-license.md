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
## Response Parameters
| Parameter | Description | Type | Notes |
| --- | --- |  --- | --- |
| SubscriptionMaximumSiteLimit | the number of websites that you can add to your account | integer | --- |
| SubscriptionSiteCount | the number of websites that you added to your account | integer | --- |
| SubscriptionEndDate | the date in which your account will expire | string | You can use the date format defined in your account. You can visit /account/changesettings to view the current format. |
| SubscriptionStartDate | the date you joined Netsparker | string | You can use the date format defined in your account. You can visit /account/changesettings to view the current format. |
| IsAccountWhitelisted | whether you can add websites directly or you require to verify your website | boolean | --- |
| UsedScanCreditCount | whether you use any scan credit to scan your websites | integer | --- |
| ScanCreditCount | the total scan credit you have | integer | --- |
| IsCreditScanEnabled | whether you enabled the scan credit for your account | boolean | --- |
| IsSubscriptionEnabled | whether you enabled the subscription for your account | boolean | --- |
| PreVerifiedWebsites | whether you have any pre-verified websites | string | --- |
| Licenses | array of information about your license detail | string | --- |
| Licenses/EndDate | the date in which your subscription will expire in Netsparker  | string | --- |
| Licenses/MaximumSiteLimit | the maximum number of websites you can add to your websites | integer | --- |
| Licenses/ProductDefinition | the Netsparker license you have | string | --- |
| Licenses/StartDate | the date you joined Netsparker | string | You can use the date format defined in your account. You can visit /account/changesettings to view the current format. |
| Licenses/ValidForDays | the days your account will be valid for | string | --- |
| Licenses/Id | the identification number of your account | integer | --- |
| Licenses/IsActive | whether your account is active or not | boolean | --- |
| Licenses/Key | your account key | string | --- |
| Licenses/AccountCanCreateSharkScanTask | whether you can use IAST capabilities in your account | boolean | --- |

  ## Status Code and Errors
| Code | Description |  Notes |
| --- | --- |  --- |
| 200 | OK |  Success |
| 401 | Unauthorized |  The access is denied |
| 404 | Not Found |  Invalid type. |
