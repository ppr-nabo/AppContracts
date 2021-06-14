## Log in and Sign up

### Login

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

### Sign up

```