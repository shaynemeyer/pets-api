# Auth - Controlling access

Every app has two global variables:
* APP-ID (username)
* APP-SECRET (password)

## Step 1
Navigate to token generator url:
```
POST /get_token 

body:
{
    "APP_ID": "myapp",
    "APP_SECRET": "somesecret"
}
```

Returns:
Reponse will contain the token and its expiration time.
```
TOKEN: alsjkfasldfalsdfjlasdjflaskdf
       Expires: x hours
```


## Step 2
Once the token has been generated, attach it to each request in the HEADERS

HEADERS:

    APP-ID
    TOKEN

