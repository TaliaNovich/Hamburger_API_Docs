# Response Codes

The server supports the standard HTTP status codes. 
See [this website](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status) for details. 
In addition, the following status codes are customized to this API.


| Error Code Number 	| Text Shown                     	| Definition                                                                                          	|
|-------------------	|--------------------------------	|-----------------------------------------------------------------------------------------------------	|
| 601               	| Server busy. Please try again. 	| If more than 3 orders are being ordered at the same time the server will respond with this message. 	|
