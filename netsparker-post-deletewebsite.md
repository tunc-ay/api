## Delete a website in Netsparker.
Description: This endpoint lets you delete a website, including with its scan data and configuration, in Netsparker. 
## URL
POST https://www.netsparkercloud.com/api/1.0/websites/delete

## Headers
| Header Name | Description | Required | Values | Notes |
| --- | --- |  --- | --- | --- |
| Authorization | The authorization method | Required |  | Basic Authentication |
| Accept | The format of the data to be returned | Required |  | application/json |

## Body Parameters
| Parameters | Description | Required | Type | Notes |
| --- | --- |  --- | --- | --- |
| URL | The URL of the website you want to delete | Required | string | Basic Authentication |

## Sample Request
```javascript
GET https://www.netsparkercloud.com/api/1.0/websites/delete
```
## Sample Response
 ```javascript
{
  "RootUrl": "http://rest.testsparker.com/"
}
```
## Response Parameters
| Parameter | Description | Type | Notes |
| --- | --- |  --- | --- |
| RootUrl | The URL of the website you want to delete | string | --- |

  ## Status Code and Errors
| Code | Description |  Notes |
| --- | --- |  --- |
| 200 | OK |  Success |
| 401 | Unauthorized |  The access is denied |
| 404 | Not Found |  Invalid type. |
