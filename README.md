# Odd README.md

## login

- url : /api/auth/login

- method : POST

- request:

| param name | param type | param value |  
|------------|------------|-------------|  
| mailbox    |   String   |user's mailbox|
| password   |   String   |user's password|


- response:

status code :  
   - 200 => succeed 
   - 700 => mailbox and password unmatch
   - 702 => illegal param
   
if status code == 200:
    will return 
    
```json

  {"token":"token_string..."}

``` 
  
## register

- url : /api/auth/register

- method : POST

- request:

| param name | param type | param value |  
|------------|------------|-------------|  
|  mailbox   |   String   |user's mailbox|
|  name      |   String   |user's name|
| password   |   String   |user's password|


- response:

status code :  
   - 200 => succeed
   - 701 => user exist
   - 702 => illegal param
   
   
     
mapping:
   - 200 => succeed
   - 700 => password unmatch mailbox
   - 701 => user exist
   - 702 => illegal param
   - 703 => file not find