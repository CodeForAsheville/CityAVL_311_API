City of Asheville 311 api documentation
===============

#About 311#
311 systems is a non-emergency civic issue tracker.  Thinke potholes, water leaks, and graffitti, In this case 311 is not a phonenumber instead it is a technology that provides open channels of communication for issues that concern public space and public services.

This page will attempt to document the API the City of Asheville uses so we can create "civic hacks" on the 311 data. Think info graphics, predictive anyalsis, and maps.  

join us for a sersis of hack nights and talks to explore the City of Asheville 311 data. see our meetup at http://www.meetup.com/Code-for-Asheville/


#api Documention#

#Getting Started#
The Offical documentation is here tps://www.publicstuff.com/developers
Request an API key from https://www.publicstuff.com/developers/api

###The Offical API documetentation is here###
https://www.publicstuff.com/developers/api

for us the main things are as follows:
* Asheville City client_id is 819
* Asheville City city ID or space_id is 3737

###Sample API Calls###
All return type is set to json for the samples (valid types are xml, json, or jsonp)
All samples require a api key that you will need to get from https://www.publicstuff.com/developers/api

###city_view###
Get information about Asheville 

  https://www.publicstuff.com/api/2.0/city_view?return_type=json&space_id=3737&api_key=[your api key]
  
###request_types###
Get all request for service type valid for the City of Asheville note the request type for parks - 11345

  https://www.publicstuff.com/api/2.0/requesttypes_list?client_id=819&api_key=

###requests_list###  
Get the first 100 requests for service, to report problems a city park in this cae withn 100 meters around downtown

  http://www.publicstuff.com/api/2.0/requests_list?return_type=json&limit=100&lat=35.62336&request_type_id=11345&lon=-82.561531&nearby=250&api_key=[your api key]

###request_view###
From the returned JSON you might want to see the full request for service for the issue #98168

  https://www.publicstuff.com/api/2.0/request_view?return_type=json&request_id=98168&api_key=[your api key]

###comments_list###
For each reuquest for service there is likely comments about related to resloving the issue.  
In this case the citizen reporting and the City Employee commuicate via the app untill the issue is resolved.  In this case there are 6 comments associated with issue #98168

  https://www.publicstuff.com/api/2.0/comments_list?return_type=json&request_id=98168&api_key=[your api key]

  
