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

### Sign up

Path: `/user/register`

Input
```
{
	userName: String,
        email: String,
	phone: String,
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
	success: Boolean
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
* DuplicateRegistrationAttempt


### Get user profile

Path: `/user/profile`

Input
```
{
	userName: String
}
```

Output
```
{
        email: String,
	phone: String,
	firstName: String,
	lastName: String,
	street1: String,
	street2: String,
	city: String,
	zip: String,
        createdTimestamp: DataTime
	displayName: String
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
* EmptyLoginCredentials
* UserNotFound

### Delete user profile

Path: `/user/delete`

Input
```
{
	userName: String,
        email: String
}
```

Output
```
{
    success: Boolean
}
```


### Skills

#### Get all skills
Path: `/skills`

Input: Empty body

Output
```
[ // List of skills
  {
    id: String,
    name: String,
    description: String
  }
]
```
#### Add skills to user
Path: `/skills/user`

Input
```
{
    "userName": String,
    "skills": [Int] // Skill ID
}
```

Output
```
{
    "success": Boolean
}
```

#### Get user skills
Path: `/skills/user/<username>`

Input: Empty body

Output:
```
[ // List of skills
  {
    id: String,
    name: String,
    description: String
  }
]
```
