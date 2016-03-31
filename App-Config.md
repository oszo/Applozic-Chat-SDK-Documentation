#Message Fallback Time

Message Fallback Time is the duration in which if message is not delivered to end user then message will be delivered though mail as a fallback. For message fallback our api requires receiver user emailId which need to pass during registration and also you have to configure message delivery fallback time in dashboard for your app.  




#Webhook Url

Webhook Url can be configured by application admin in the applozic dashboard.All messages will be forwarded to the webhook url in JSON format.


**Request Body**: Posted Json to configured Url :


 ```  
{"key":"5-67f73984-2efe-4422-a522-d181cec5bd5d-1457958424015",      
"from":"lee","to":"kevin","message":"hello kevin",
"timeStamp":1457958424000}
 ```
 
#Authentication Url

Authentication Url is configured by application admin in Applozic Dashbaord for authenticating users from your side. The Url should accept POST request with following two paramters.
The user should provide the access token in the "accessToken" option while plugin initialization.

| Parameter  | Description |
| ------------- | ------------- |
| username | UserName of the user who should be authenticated |
| token | Access token for the specified user |

**Response**: Response text received on configured url:

 ```  
true : If user is authenticated
false : If user is not authenticated.
 ```