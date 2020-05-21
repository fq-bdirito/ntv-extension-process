# Global NTV or Extension - Guest Template
```
Dear {!Opportunity.Primary_Tenant_copy__c},

Hello from Furnished Quarters! This is a reminder that Notice to Vacate on your lease ending on {!Opportunity.Departure_Date__c} at {!Opportunity.Primary_Product__c} is due on {!Opportunity.Notice_Due__c}.

We will process an auto extension for an additional 30 days if we do not hear from you.


CONFIRM DEPARTURE: https://cs.furnishedquarters.com/notices/confirm-departure?resid={!Opportunity.Id}

I WISH TO EXTEND: https://cs.furnishedquarters.com/notices/extend?resid={!Opportunity.Id}



FurnishedQuarters.com | 212.367.9400 | 158 West 27th Street. 8th Floor. New York, NY 10001
```


# Link button to Rails Route - Link to Client Solutions Staging

<br>

# Partner Confirms Departure
* Email Template - OOM Departure Confirmed - Partner
* https://furnishedquarters--demo.lightning.force.com/lightning/setup/CommunicationTemplatesEmail/page?address=%2F00Xq0000000NrXl
* button url - https://client-solutions-staging.herokuapp.com/notices/confirm-departure?resid={! OOM__c.Id }

```html
<a href="https://client-solutions-staging.herokuapp.com/notices/confirm-departure?resid={!Opportunity.Id}" target="_blank">Confirm Departure</a>
```

<br>

# Partner Confirms Extension
* Email Template - OOM Lease Extension - Partner
* https://furnishedquarters--demo.lightning.force.com/lightning/setup/CommunicationTemplatesEmail/page?address=%2F00Xq0000000NqBU
* https://client-solutions-staging.herokuapp.com/notices/partner-confirm-extension?extid={! extension_req_id }

```html
<a href="https://client-solutions-staging.herokuapp.com/notices/partner-confirm-extension?extid={!Extension_Request__c.Id}" target="_blank">Confirm Extension</a>
```

#### An Opportunity can have multiple extension requests
#### Select all extensions related to a given opportunity that partner did not confirm yet
```
select id, opportunity__c, partner_extension_confirmed_by__c from extension_request__c where opportunity__c='006q000000Kaie9AAB' and partner_extension_confirmed_by__c=null
```

# Guest Confirms Extension
https://furnishedquarters--demo.lightning.force.com/lightning/setup/CommunicationTemplatesEmail/page?address=%2F00Xq0000000SGNT%3Fsetupid%3DCommunicationTemplatesEmail

```html
<a target="_blank" href="https://client-solutions-staging.herokuapp.com/notices/guest-confirm-extension?extid={!Extension_Request__c.Id}">Confirm Extension Request</a>
```