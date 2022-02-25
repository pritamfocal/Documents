## Integration

> **Note**: 
-  This  authentication process to add more security who can access to our API's


### Get Secret key and client ID

1. Please send mail to contact@focalx.ai to with following details from your company mail
- Company name
- Application name
- Application bundle identifiier (in case if your using ios)
- Application package name (in case if your using Android)

We will send you the details with client ID, Client secrete, API key and API address to use to generate the token

2. Please generate token using following details

- Use the API domain address you got from US
- Send following parameters as request in json formate

        {
           clientID:"Client ID you got from us"
           clientSecret:"Client Secrete you got from us"
           apiKey:"key that we will change once a month and you will get updated apiKey from this API responce only"
           hashKey:"Some user unique identifier"
           scope:"check scope values below"
        }
     
> **Note**: 

        scope=upload
        scope=readReports
        scope=deleteReports
        scope=deleteAccount

      hashKey: this is Generated using hash and it will be unque to perticular user in you'r system. Either you can use your user's id or mail address and once you hash it we will not know what is it. This is helpul if you want to know the pertical user's reports and his activities in our system. 

- The Responce you will get from above request will be 

        {
           apiKey:"updated key"
           token:"api access token"
        }
