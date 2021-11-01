## Retrieve all issues identified by Netsparker
Description: This endpoint lets you retrieve all issues identified by Netsparker.
## URL
GET https://www.netsparkercloud.com/api/1.0/issues/allissues
## Query Parameters
| Parameter | Description | Type | Required | Notes |
| --- | --- | --- | --- | --- |
| severity | The severity of the vulnerability identified | string | optional | 
| webSiteName | the name of the website | string | optional | 
| websiteGroupName | the name of the website group | string | optional |
| page | the number of the page | integer | optional | 
| pageSize | the number of vulnerabilities displayed in the single page | integer | optional | Page size can be any value between 1 and 200.|
| sortType | Sort by ascending and descending according to LastSeenDate. | string | optional | Default parameter is ascending. |
| lastSeenDate | the last date that the vulnerability is identified. | string | optional | You can use the date format defined in your account. You can visit /account/changesettings to view the current format.|   |
| rawDetails | ? | string | optional | If you want the vulnerability data response (remedy, description, etc.) to return without raw html, this field must be set false. |
| integration | ? | integer | optional | the default value is Jira.|
## Headers
| Header Name | Description | Required | Values |
| --- | --- | --- | --- |
| Accept | the format of the data to be returned | optional | application/json |
## Sample Request
```javascript
GET https://www.netsparkercloud.com/api/1.0/issues/allissues?Severity=low&page=1
```

## Sample Response
 ```javascript
 {
    "FirstItemOnPage": 1,
    "HasNextPage": true,
    "HasPreviousPage": false,
    "IsFirstPage": true,
    "IsLastPage": false,
    "LastItemOnPage": 20,
    "List": [
        {
            "AssigneeName": "Alan York",
            "FirstSeenDate": "01/12/2021 01:25 PM",
            "Id": "f11874b6-10ba-48fd-d4ed-acae03f40f92",
            "IsAddressed": false,
            "IsDetectedByShark": false,
            "IsPresent": true,
            "LastSeenDate": "01/12/2021 01:25 PM",
            "StateFixedConfirmedDate": null,
            "UpdatedDate": "02/17/2021 01:32 AM",
            "Severity": "Low",
            "State": "Present",
            "Title": "Apache MultiViews Enabled",
            "Url": "http://rest.testsparker.com/docs/css/style",
            "LatestVulnerabilityIsConfirmed": false,
            "WebsiteId": "294444f4-270a-42e1-5f54-abd4016a1e55",
            "WebsiteName": "Rest",
            "WebsiteRootUrl": "http://rest.testsparker.com/",
            "FixTimeInMinutes": null,
            "Certainty": 90,
            "Parameters": [],
            "VulnerabilityDetail": "&lt;p&gt;Netsparker Enterprise detected that Apache MultiViews is enabled.&lt;/p&gt;&lt;p&gt;This vulnerability can be used for locating and obtaining access to some hidden resources.&lt;/p&gt;",
            "Impact": "&lt;div&gt;&lt;div&gt;An attacker can use this functionality to aid in finding hidden files in the site and potentially gather further sensitive information.&lt;/div&gt;&lt;/div&gt;",
            "Actions": "&lt;div&gt;&lt;ol&gt;&lt;li&gt;&lt;p&gt;Change your server configuration file. A recommended configuration for the requested directory should be in the following format:&lt;/p&gt;&lt;pre class=&quot;xml code&quot;&gt;&amp;lt;Directory /{YOUR DIRECTORY}&amp;gt;\n\tOptions FollowSymLinks\n&amp;lt;/Directory&amp;gt;\n&lt;/pre&gt;&lt;p&gt;Remove the &lt;em&gt;MultiViews&lt;/em&gt; option from configuration.&lt;/p&gt;&lt;/li&gt;&lt;/ol&gt;&lt;/div&gt;",
            "Skills": "",
            "Remedy": "",
            "RemedyReferences": "",
            "ExternalReferences": "",
            "ProofOfConcept": "",
            "CustomData": null,
            "CustomFields": [],
            "ClassificationLinks": [
                "http%3a%2f%2fwww.owasp.org%2findex.php%2fTop_10_2013-A5",
                "http%3a%2f%2fwww.owasp.org%2findex.php%2fTop_10_2017-A6",
                "http%3a%2f%2fcwe.mitre.org%2fdata%2fdefinitions%2f16.html",
                "http%3a%2f%2fprojects.webappsec.org%2f",
                "https%3a%2f%2fwww.netsparker.com%2fcompliance-reports%2fiso27001%2fcontrol-objectives-and-controls%2f%2f%23A-9-4-1",
                "https%3a%2f%2fowasp.org%2fwww-pdf-archive%2fOWASP_Application_Security_Verification_Standard_4.0-en.pdf",
                "https%3a%2f%2fnvlpubs.nist.gov%2fnistpubs%2fSpecialPublications%2fNIST.SP.800-53r4.pdf",
                "https%3a%2f%2fwww.solarwinds.com%2ffederal-government%2fsolution%2fdisa-stig-compliance"
            ],
            "CvssVectorString": "",
            "Cvss31VectorString": "",
            "Type": "ApacheMultiViewsEnabled",
            "Classification": {
                "Asvs40": "4.3.2",
                "Capec": null,
                "Cwe": "16",
                "DisaStig": "6.9",
                "Hipaa": null,
                "IsEmpty": false,
                "Iso27001": "A.9.4.1",
                "Nistsp80053": "AC-6",
                "Owasp2013": "A5",
                "Owasp2017": "A6",
                "OwaspProactiveControls": null,
                "Pci32": null,
                "Wasc": "14"
            },
            "CvssVector": {},
            "VersionIssues": [],
            "IsRetest": false,
            "IsTodo": true,
            "LatestScanId": "714603f6-09bf-4286-1d46-acae03f2ea44",
            "History": null,
            "Tags": []
        },
      ]
   }
```
## Response
| Parameter | Description | Type | Notes |
| --- | --- | --- | --- |
| FirstItemOnPage | ? | string |  | 
| HasNextPage | Shows whether there is a next page | string | The value is true or false. | 
| HasPreviousPage | Shows whether there is a previous page | string | The value is true or false. | 
| IsFirstPage | Shows whether this is the first page | string | The value is true or false. | 
| IsLastPage | Shows whether this is the last page | string | The value is true or false. | 
| LastItemOnPage | Shows whether this is the last item on the page | string | The value is true or false. | 
| List| Array of data | string |  | 
| {List}/AssignName | the name of the person that is responsible for this vulnerability | string |  | 
| {List}/FirstSeenDate | the data in which Netsparker identified this vulnerability | string | You can use the date format defined in your account. You can visit /account/changesettings to view the current format.  | 
| {List}/Id | the id of the vulnerability | integer |  | 
| {List}/IsAddressed | the action has been taken or not | string |  The value is true or false. | 
| {List}/IsDetectedbyShark | the Netsparker Shark (IAST) identified this vulnerability or not | string |  The value is true or false. | 
| {List}/IsPresent | the case whether the vulnerability identified still is present | string |  The value is true or false. | 
| {List}/LastSeenDate | the last date that the vulnerability is identified. | string |  You can use the date format defined in your account. You can visit /account/changesettings to view the current format. | 

  ## Status Code and Errors
| Code | Description |  Notes |
| --- | --- |  --- |
| 200 | OK |  Success |
| 401 | Unauthorized |  The access is denied |
| 404 | Not Found |  Invalid type. |
