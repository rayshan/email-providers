# Email Providers

This repository provides list of email providers in csv format.

## CSV file
Check [email-providers.csv](https://github.com/edwin-zvs/email-providers/blob/master/email-providers.csv).

This list is useful when you want check if your user's email address is company mail address or not.

Please create a pullrequest to update the list.

## Rest API

This repository also provide free Rest API endpoint. The api endpoints serves up-to-dated data in the master branch.

When your pullrequest is merged, https://zarvis.ai will be automatically build and deploy the new version.


#### List all email providers

Request (GET)
```
https://email--providers-edwin--zvs.g1.zarvis.ai
```

Response (200, Content-Type: application/json)
```
[
    ...
    "gmail.com",
    "yahoo.com",
    ...
]
```

#### Query provider by email address or domain

Request
```
https://email--providers-edwin--zvs.g1.zarvis.ai/<email or domain>
```

Response

 - 200 - when email or domain is in the provider list
 - 404 - when email or domain is not in the provider list


Example request

```
https://email--providers-edwin--zvs.g1.zarvis.ai/foo@gmail.com
https://email--providers-edwin--zvs.g1.zarvis.ai/gmail.com
https://email--providers-edwin--zvs.g1.zarvis.ai/bar.com
```



### Thanks

Initial provider list is constructed based on
- https://gist.github.com/tbrianjones/5992856
- https://github.com/goware/emailproviders/blob/master/generate/domains.txt
- https://github.com/wesbos/burner-email-providers
