[MS Teams Apps and App Studio](https://docs.microsoft.com/en-us/microsoftteams/platform/overview)

[MS Graph documentation ](https://docs.microsoft.com/en-us/graph/)

[MS Graph API ](https://docs.microsoft.com/en-us/graph/overview)

[MS Graph API Tutorials](https://docs.microsoft.com/en-us/graph/tutorials)

[MS Graph USERS API ](https://docs.microsoft.com/en-us/graph/api/resources/user?view=graph-rest-1.0)

[Call MS Graph API from JS SPA ](https://docs.microsoft.com/en-us/azure/active-directory/develop/tutorial-v2-javascript-spa)

[Sign in users and get an access token in a JS SPA ](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-v2-javascript)

[MS Authentication Library ](https://www.npmjs.com/package/msal)

[Register a new application ](https://docs.microsoft.com/en-us/azure/active-directory/develop/scenario-spa-app-registration)

[Configure Authentication for multi-tenant ](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-implicit-grant-flow)

[Lucid App](https://lucid.app/documents#/dashboard)

Find port?
```sh
fuser -k 8080/tcp 
```
```sh
lsof -i :9000 
```
Docker list container
```sh
ps --format "table {{.Names}} \t {{.Ports}}"
```
Run in background linux[More here](https://www.tecmint.com/run-linux-command-process-in-background-detach-process/)
```
npm run watch . & 
```

[Sample mongo db node express](https://github.com/maitraysuthar/rest-api-nodejs-mongodb)


## Terraform

Terraform Azure Quickstart 

https://github.com/Azure/terraform/tree/master/quickstart
https://github.com/SlOrbA/ng-az-tf-example/blob/master/terraform/main.tf 
https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs 

Azure CLI 
https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli 

Azure AD doc 
https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-handling-exceptions?tabs=javascript 

Passport azure ad node 
https://github.com/AzureAD/passport-azure-ad 

Sample passport azure ad 
https://github.com/AzureADQuickStarts/AppModelv2-WebAPI-nodejs/blob/master/node-server/app.js 
https://github.com/AzureADQuickStarts/AppModelv2-WebAPI-nodejs/blob/master/node-server/config.js 

Permissions Reference 
https://docs.microsoft.com/en-us/graph/permissions-reference 
https://developer.microsoft.com/en-us/graph/graph-explorer 

```sh
php artisan core:service:jwt:issue service-core <client-id> <request-url> --ttl=<ttl-in-minutes> --impersonatedUserId=<user-id> 
```
Swagger Specifications 
https://swagger.io/specification/v2/ 


## git

```sh
git push
```
```sh
git push -f
```
```sh
git pull
```
```sh
gitk --all &
```

```sh
git ls-remote origin
```
```sh
git rebase -i HEAD~2
```
```sh
git reset --soft origin/develop
```
```sh
git commit --amend --no-edit
```
```sh
git commit --reuse-message @{​u}​~ ​
```
```sh
git diff @{​u}​
```
```sh
git show
```

### rebaseing

```sh
git checkout develop
```
```sh
git pull
```
```sh
git checkout technical/8781959
```
```sh
git rebase develop
```
```sh
git push -f
```


# Windows safa mode [Youtube](https://www.youtube.com/watch?v=9ngnIKqPOc4)
Command prompt code to boot to safe mode minimal:
`bcdedit /set safeboot minimal`
Command prompt code to boot back to normal windows:
`bcdedit /deletevalue safeboot`


https://docs.docker.com/engine/install/linux-postinstall/ 

# JWT

```json
[
  {
    "typ": "JWT",
    "nonce": "TJDoIuGiCE1alo1oteuRU5Ye-FXbH9l5tB8U7-5aMjE",
    "alg": "RS256",
    "x5t": "kg2LYs2T0CTjIfj4rt6JIynen38",
    "kid": "kg2LYs2T0CTjIfj4rt6JIynen38"
  },
  {
    "aud": "00000003-0000-0000-c000-000000000000",
    "iss": "https://sts.windows.net/f33abe27-86cd-46d6-ae2b-b918362ab160/",
    "iat": 1605500358,
    "nbf": 1605500358,
    "exp": 1605504258,
    "acct": 0,
    "acr": "1",
    "acrs": [
      "urn:user:registersecurityinfo",
      "urn:microsoft:req1",
      "urn:microsoft:req2",
      "urn:microsoft:req3",
      "c1",
      "c2",
      "c3",
      "c4",
      "c5",
      "c6",
      "c7",
      "c8",
      "c9",
      "c10",
      "c11",
      "c12",
      "c13",
      "c14",
      "c15",
      "c16",
      "c17",
      "c18",
      "c19",
      "c20",
      "c21",
      "c22",
      "c23",
      "c24",
      "c25"
    ],
    "aio": "E2RgYDgR0xb19rTMgXiteQFx7TOiZ0T8YHDwfCr4dFOMvcQr2XkA",
    "amr": [
      "pwd"
    ],
    "app_displayname": "erwin WebModeller",
    "appid": "98f8c827-4503-470e-9728-efa36f2ab35e",
    "appidacr": "0",
    "family_name": "Sharma",
    "given_name": "Ayushman",
    "idtyp": "user",
    "ipaddr": "157.42.38.75",
    "name": "Ayushman Sharma",
    "oid": "602361d8-bf61-45a6-8e60-0464697a6138",
    "platf": "3",
    "puid": "10032000EAD279C4",
    "rh": "0.AAAAJ746882G1kauK7kYNiqxYCfI-JgDRQ5Hlyjvo28qs14YANQ.",
    "scp": "email openid profile User.Read",
    "sub": "-3Z0lvtdvEkyvqdfS3my8Tkn1WHDU5ol_euKrUjHg6Y",
    "tenant_region_scope": "NA",
    "tid": "f33abe27-86cd-46d6-ae2b-b918362ab160",
    "unique_name": "aysharma@erwin.com",
    "upn": "aysharma@erwin.com",
    "uti": "lZeNOIURa0aN69l7Cdc7AA",
    "ver": "1.0",
    "xms_st": {
      "sub": "7KuSBMmOTy1xSwyYMbZog4xnBdE7yYoIhBgpCU-IhGE"
    },
    "xms_tcdt": 1457627961
  }
]
[
  {
    "aud": "00000003-0000-0000-c000-000000000000",
    "iss": "https://sts.windows.net/f33abe27-86cd-46d6-ae2b-b918362ab160/",
    "iat": 1607346081,
    "nbf": 1607346081,
    "exp": 1607349981,
    "acct": 0,
    "acr": "1",
    "acrs": [
      "urn:user:registersecurityinfo",
      "urn:microsoft:req1",
      "urn:microsoft:req2",
      "urn:microsoft:req3",
      "c1",
      "c2",
      "c3",
      "c4",
      "c5",
      "c6",
      "c7",
      "c8",
      "c9",
      "c10",
      "c11",
      "c12",
      "c13",
      "c14",
      "c15",
      "c16",
      "c17",
      "c18",
      "c19",
      "c20",
      "c21",
      "c22",
      "c23",
      "c24",
      "c25"
    ],
    "aio": "ASQA2/8RAAAAtpFSXIG5RX7PujTx7VPFrs8b4e8+CRuQFFim+aFAllY=",
    "amr": [
      "pwd"
    ],
    "app_displayname": "erwin WebModeller",
    "appid": "98f8c827-4503-470e-9728-efa36f2ab35e",
    "appidacr": "0",
    "family_name": "Sharma",
    "given_name": "Ayushman",
    "idtyp": "user",
    "ipaddr": "157.35.243.130",
    "name": "Ayushman Sharma",
    "oid": "602361d8-bf61-45a6-8e60-0464697a6138",
    "platf": "3",
    "puid": "10032000EAD279C4",
    "rh": "0.AAAAJ746882G1kauK7kYNiqxYCfI-JgDRQ5Hlyjvo28qs14YANQ.",
    "scp": "email openid profile User.Read",
    "sub": "-3Z0lvtdvEkyvqdfS3my8Tkn1WHDU5ol_euKrUjHg6Y",
    "tenant_region_scope": "NA",
    "tid": "f33abe27-86cd-46d6-ae2b-b918362ab160",
    "unique_name": "aysharma@erwin.com",
    "upn": "aysharma@erwin.com",
    "uti": "eLEmR57zREqta0ijrfgEAA",
    "ver": "1.0",
    "xms_st": {
      "sub": "7KuSBMmOTy1xSwyYMbZog4xnBdE7yYoIhBgpCU-IhGE"
    },
    "xms_tcdt": 1457627961
  },
  {
    "typ": "JWT",
    "nonce": "bGE1qv4pnqPatPhnD15Z_Wg7fhW4z00ujZebNNeBCl8",
    "alg": "RS256",
    "x5t": "kg2LYs2T0CTjIfj4rt6JIynen38",
    "kid": "kg2LYs2T0CTjIfj4rt6JIynen38"
  }
]
```


https://kubernetes.io/docs/concepts/windows/intro/ 

# Windows
Search CLASSNAME in registry 

reg query HKLM\SOFTWARE\Classes /s /f CLASSNAME 
https://powershellmagazine.com/2013/06/27/pstip-get-a-list-of-all-com-objects-available/ 
