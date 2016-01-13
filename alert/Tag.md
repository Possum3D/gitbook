# Alert tags


- [bottom](#bottom-up)
- [PUT Tag](#put-tag)

Obviously, you should keep in mind the good practices:

{% include "../GoodPractice.md" %}

## Tag [/api/accounts/{account_id}/alerts/{alert_id}/tags]

- name: foo (string) - the name of the tag


### Get Tags [GET]


Fetch the list of tags for a given alert of a given account.
Notice that tags are associated to an alert; all accounts sharing this alert will be aware of the tags.


+ Request

    + Headers
    
{% include "../typicalRequest.md" %}
            SPECIAL-HEADER: toto 
        
 
+ Response 200 (application/json)

        {
            "tags": [
                {
                    "id": 321,
                    "name": "Semester1"
                },
                {
                    ..
                }
            ]
        }

{% include "./PostTag.md"  %}


### PUT Tag [PUT /api/accounts/{account_id}/alerts/{alert_id}/tags/{tag_id}]

Modify a tag. If you do so, all mentions tagged with the old tag will be turned to mentions tagged with the new tag.

Attribute     | Explanation
------------- | -------------
name          | the label you want to give to your tag


+ Parameters
    + account_id (number) - Id of the account
    + alert_id (number) - Id of the alert
    + tag_id (number) - Id of the tag
<!-- <dev> -->
    + stats (bool) - indicates that you want all associated stats (DEV ONLY)
<!-- </dev>  -->


+ Attributes (Tag)
    

+ Request

    + Headers
        
            Authorization: Bearer YOUR_ACCESS_TOKEN_HERE

    + Body
            
            {
                "name": "foo2"
            }

+ Response 200 (application/json)

        {
            "success": true
        }


```php
<?php
    echo($toto);

```


### bottom up

this is the bottom
