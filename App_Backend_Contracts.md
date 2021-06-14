## Log in and Sign up

### Login

Path: `/user/auth`

Input
```
{
    "userName": String,
    "password": Encrypted String	
}
```

Output
```
{	
   "DisplayName": String
}
```

Error
```
{
    "errorCause": {refer Error Cause},
    "errorDetail": String
}
```

Error Cause  
* InvalidPathParameter
* EmptyLoginCredentials
* UserNotFound

### Address verification

Path: `/address/verify`

Input
```
{
	firstName: String,
	lastName: String,
	street1: String,
	street2: String,
	city: String,
	zip: String
}
```

Output
```
{
	"verifiedAddress": Boolean
}
```

Error
```
{
	"errorCause": {refer Error Cause},
	"errorDetail": String
}

```

Error Cause  
* UnsupportedLocation
* ProviderCallFailure
