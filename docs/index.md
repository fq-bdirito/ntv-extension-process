# Overview

GOAL: Automate the Global Notice and Extension Processes

<br>

## Global Notice Process
* <a href="/notice" target="_blank">More Details</a>
* Process For Partner types - **Corporate Housing, Property Direct Furnished, Hotel**
* Auto email goes out to notice contact (client or guest)
* Guest confirms departure
* The following `Reservation` fields are updated on Salesforce:
    * `Provider Notice Given` checkbox is checked
    * `Departure Confirmed` checkbox is checked
    * `Departure Confirmed By` text field captures Guest's signature and date
    * `Notice Status` changes to `Notice`
    * `Notice Contact Partner By` date field captures the date guest confirmed departure
* Once `Departure Confirmed` checkbox is checked off, an auto email is sent to Partner
* Partner will confirm guest's departure
    * If partner does not respond, a reminder email will be sent 32 hrs (8am EST next day) after guest confirmed departure
    * References the `Notice Contact Partner By` field to determine when guest confirmed departure
* Once partner has confirmed guest's departure, the following fields are updated in Salesforce:
    * `Partner NTV Confirmed` checkbox is checked off
    * `Partner NTV Confirmed By` text field captures partner's signature and date
* An auto email is sent to Global Leasing team to notify partner has confirmed guest's departure

<br>

## Global Extension Process
* <a href="/extend" target="_blank">More Details</a>
* Process For Partner types - **Corporate Housing, Property Direct Furnished, Hotel**
* Auto email goes out to notice contact (client or guest)
* Guest requests for an extension via the Client Solutions app
* Once the guest submits their request, a new `Extension Request` record is created
* And the following fields are updated on Salesforce:
    * `Request` text field that captures guest's full name and their requested end date
    * `Start Date` date field that is set to their departure date
    * `End Date` date field is set to the guest's requested end date
    * `Opportunity` related look up field is populated
    * `Primary Partner Contact` look up field is set to its associated Reservation's Primary Partner Contact
* Upon creation of a new Extension Request record, an auto email gets sent to partner
* If partner does not confirm extension availabilty, a reminder email is sent 24hrs after the extension request record has been created
* After partner confirms extension availability via Client Solutions app the following fields will be updated on Salesforce:
    * `Partner Extension Option`
    * `Is Available`
    * `Rate Change`
        * `Partner Confirmed New Rate`
    * `Partner Confirmed End Date`
    * `Partner Extension Confirmed By`
* Once partner signs off, an auto email will be sent to Global Leasing team
* If Furnished Quarters approves extension the `FQ Accept Partner Terms` checkbox will be checked off
* And an auto email will be sent to the partner to display the detailed information of extension
* Note: this automated process is only in effect if there is **no rate change**
* Process will remain manual for any rate changes.