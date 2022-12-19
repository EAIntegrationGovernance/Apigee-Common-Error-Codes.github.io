|Error <img width=250/>| Cause|
|-------------------------|----------|
|401 Unauthorized |The credentials that you are using to make a request do not have the appropriate permissions to perform the operation. Verify the roles for the account you are using.|
|403 Forbidden |The username and password combination you are using is not valid for the organization you specified. To test your credentials, log in to login.apigee.com/login. If you need an account, sign up.|
|404 Not Found |Verify that the request URL is spelled correctly and that the API you are trying to access exists. For example, ensure that you are not trying to access the wrong revision of an API. See also 404 Unable to identify proxy for host: <virtual host name> and url: <path>.|
|405 Method not allowed |You specified a method that is not supported. For example, you used the GET verb for an API call that requires the POST verb.|
|406 Not Acceptable |The API cannot produce any responses that are supported by the application.|
|409 Conflict |Indicates a conflict with an existing entity. For example, you attempted to create a cache using a name that already exists.|
|415 Unsupported media type |Typically, this error occurs on POST or PUT requests when the Content-type HTTP header is set to the wrong value. For example, an HTTP 415 error is returned if you POST the following to an API that only supports JSON:

  $ curl https://api.company.com/v1/json_service
    -X POST
    -H "Content-type:text/xml"
    -d '<SomeXML>'
  For GET requests, use the Accept header instead of the Content-type header.|
|429 Too Many Requests |The rate limit was exceeded on Quota or Spike Arrest policies. The current default status code for exceeding the rate limit is 500, but the default may change to 429 in the future. See Spike Arrest policy and Quota policy for information on how to change the 500 to a 429.|
|500 Internal Server Error |Note: Apigee Edge organizations can be configured to return an HTTP status code of 429 (Too Many Requests) instead of 500 for all requests that exceed a rate limit set by some rate-limiting policies. For more information, see Spike Arrest policy and Quota policy.|
|502 Bad Gateway| See 502 Bad Gateway.]
|503 Service Unavailable |See 503 Service Unavailable.]  
|503 Gateway Timeout|See 504 Gateway Timeout.]  
<br/>
Example Payload<br/>
{<br/>
"httpCode": "401",<br/>
"httpMessage": "Unauthorized",<br/>
"moreInformation": "This server could not verify that you are authorized to access the URL"<br/>
}<br/>
