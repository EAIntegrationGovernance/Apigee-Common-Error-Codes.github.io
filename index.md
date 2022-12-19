|Error <img width=250/>| Cause|
|---------------------------------------|------------------------------------------------------------|
|401 Unauthorized |The credentials that you are using to make a request do not have the appropriate permissions to perform the operation. Verify the roles for the account you are using.|
|403 Forbidden |The username and password combination you are using is not valid for the organization you specified. To test your credentials, log in to login.apigee.com/login. If you need an account, sign up.|
|404 Not Found |Verify that the request URL is spelled correctly and that the API you are trying to access exists. For example, ensure that you are not trying to access the wrong revision of an API. See also 404 Unable to identify proxy for host: <virtual host name> and url: <path>.|
|405 Method not allowed |You specified a method that is not supported. For example, you used the GET verb for an API call that requires the POST verb.|
|406 Not Acceptable |The API cannot produce any responses that are supported by the application.|
|409 Conflict |Indicates a conflict with an existing entity. For example, you attempted to create a cache using a name that already exists.|
|415 Unsupported media type |Typically, this error occurs on POST or PUT requests when the Content-type HTTP header is set to the wrong value. For example, an HTTP 415 error is returned if you set application/xml to an API that only supports JSON|
