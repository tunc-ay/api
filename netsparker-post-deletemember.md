## Delete a member in Netsparker.
Description: This endpoint lets you delete a member in your team.

## URL
POST https://www.netsparkercloud.com/api/1.0/members/delete/{id}
where {id} is a team member's Id.

## Headers
| Header Name | Description | Required | Values | Notes |
| --- | --- |  --- | --- | --- |
| Authorization | The authorization method | Required |  | Basic Authentication |
| Accept | The format of the data to be returned | Required |  | application/json |

## Path Parameters
| Parameters | Description | Required | Type | Notes |
| --- | --- |  --- | --- | --- |
| id | The id of the member you want to delete | Required | string |  |

## Sample Request
```javascript
POST https://www.netsparkercloud.com/api/1.0/websites/delete/28a539cf55e3439ff953adc50270c8cd/
```
## Sample Response
 ```javascript
{
  "The member has been deleted."
}
```
## Response Parameters
| Parameter | Description | Type | Notes |
| --- | --- |  --- | --- |
| Message | The message whether the action is succesful or not | string | --- |

  ## Status Code and Errors
| Code | Description |  Notes |
| --- | --- |  --- |
| 200 | OK |  Success |
| 400 | BadRequest |  The member does not exist in your team |
| 404 | Not Found |  Invalid type. |
