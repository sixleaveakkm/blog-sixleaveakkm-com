# OAuth2
What is OAuth2? 

In the traditional client-server authentication model, the client requests access to the server with resource owner's credentials, leading to security problems.

Typically resourece owner's password is given to third-party applications, any third-party applications server exploiting results to password change, and all other third-party applications requires reauthentication. 

OAuth2 is designed to solve this problem.


## OAuth2 Client Type
OAuth2 defines two client types, 
- confidential
- public,  
based on whether it has the ability to maintain client credentials.

Therefore typically, a new OAuth2 client will generate 
`client_id` only if it is a public type, and `client_id` with `client_secret` if it is confidential type.

`client_secret` should not be delieved to public therefore any application runs on resourece owner's device without server must be public type.


## Authorization Type
OAuth2 defines four grant types natively in [RFC6749](), 
- authorization code
- implicit
- resource owner password credentials
- client credentials.

`Resource owner password credentials` grant type is the same as the traditional authentication model, requires the resource owner's username/password. Basically this grant type is consider as a backward compact method and should not be used for new systems. And many OAuth2 provider are planning to stop support this grant type.

`Client credentials` grant type is another special method used by third-party server to access resources.

Which means for resource owner to


