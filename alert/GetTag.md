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


