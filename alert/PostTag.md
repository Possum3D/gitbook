### Create Tag [POST]

Create a tag. Keep in mind that a tag is created for a specific alert only.

+ Parameters
    + account_id (number) - Id of the account
    + alert_id (number) - Id of the alert

+ Request
    
    + Headers
    
            Authorization: Bearer YOUR_ACCESS_TOKEN_HERE
    
    + Body
            
            {
                "name": "foo tag"
            }

+ Response 200 (application/json)

        {
            "success": true
        }


<a name="put"/>
