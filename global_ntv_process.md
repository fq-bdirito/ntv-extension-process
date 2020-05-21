# Global NTV or Extension - Guest Template

Dear {!Opportunity.Primary_Tenant_copy__c},

Hello from Furnished Quarters! This is a reminder that Notice to Vacate on your lease ending on {!Opportunity.Departure_Date__c} at {!Opportunity.Primary_Product__c} is due on {!Opportunity.Notice_Due__c}.

We will process an auto extension for an additional 30 days if we do not hear from you.


CONFIRM DEPARTURE: https://cs.furnishedquarters.com/notices/confirm-departure?resid={!Opportunity.Id}

I WISH TO EXTEND: https://cs.furnishedquarters.com/notices/extend?resid={!Opportunity.Id}



FurnishedQuarters.com | 212.367.9400 | 158 West 27th Street. 8th Floor. New York, NY 10001

<br>

# Link button to Rails Route

<br>

# Partner Confirms Departure
* Email Template - OOM Departure Confirmed - Partner
* https://furnishedquarters--demo.lightning.force.com/lightning/setup/CommunicationTemplatesEmail/page?address=%2F00Xq0000000NrXl
* button url - https://client-solutions-staging.herokuapp.com/notices/confirm-departure?resid={!Opportunity.Id }


<a href="https://client-solutions-staging.herokuapp.com/notices/confirm-departure?resid={!Opportunity.Id}" target="_blank">Confirm Departure</a>


<br>

# Partner Confirms Extension
* Email Template - OOM Lease Extension - Partner
* https://furnishedquarters--demo.lightning.force.com/lightning/setup/CommunicationTemplatesEmail/page?address=%2F00Xq0000000NqBU
* https://client-solutions-staging.herokuapp.com/notices/partner-confirm-extension?extid={!Extension_Request__c.Id}


<a href="https://client-solutions-staging.herokuapp.com/notices/partner-confirm-extension?extid={!Extension_Request__c.Id}" target="_blank">Confirm Extension</a>

<br>

# Guest Confirms Extension
https://furnishedquarters--demo.lightning.force.com/lightning/setup/CommunicationTemplatesEmail/page?address=%2F00Xq0000000SGNT%3Fsetupid%3DCommunicationTemplatesEmail

<a target="_blank" href="https://client-solutions-staging.herokuapp.com/notices/guest-confirm-extension?extid={!Extension_Request__c.Id}">Confirm Extension Request</a>

