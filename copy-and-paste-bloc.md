### _class_ edgeimpulse_api.api.auth_api.AuthApi(api_client=None)
Bases: `object`


#### discourse(sso: StrictStr[StrictStr], sig: StrictStr[StrictStr], \*\*kwargs)
Discourse

Log in a user to the forum. This function is only available through a JWT token.


* **Parameters**

    
    * **sso** (*str*) – Single sign-on token (required)


    * **sig** (*str*) – Verification signature (required)


    * **async_req** (*bool**, **optional*) – Whether to execute the request asynchronously.


    * **_preload_content** (*bool**, **optional*) – if False, the urllib3.HTTPResponse object will
    be returned without reading/decoding response
    data. Default is True.


    * **_request_timeout** – timeout setting for this request. If one
    number provided, it will be total request
    timeout. It can also be a pair (tuple) of
    (connection, read) timeouts.



* **Returns**

    Returns the result object.
    If the method is called asynchronously,
    returns the request thread.



* **Return type**

    None



#### readme(\*\*kwargs)
Readme.io

Log in a user to the docs. This function is only available through a JWT token.


* **Parameters**

    
    * **async_req** (*bool**, **optional*) – Whether to execute the request asynchronously.


    * **_preload_content** (*bool**, **optional*) – if False, the urllib3.HTTPResponse object will
    be returned without reading/decoding response
    data. Default is True.


    * **_request_timeout** – timeout setting for this request. If one
    number provided, it will be total request
    timeout. It can also be a pair (tuple) of
    (connection, read) timeouts.



* **Returns**

    Returns the result object.
    If the method is called asynchronously,
    returns the request thread.



* **Return type**

    None
