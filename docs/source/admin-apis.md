# Admin Configuration APIs

## Overview

This page is a work in progress. While it's being constructed, temporary API documentation can be found [here](https://gluu.org/docs/oxtrustapi/)

!!! Important
    oxTrust API support is only guaranteed for customers with a [VIP subscription](https://www.gluu.org/pricing#vip).
    
## Available APIs

| API | Description |
| --- | ----------- |
| [addClientToUmaResource](#addclienttoumaresource) | Add client to an UMA resource |
| [addGroupMember](#addgroupmember)| Add a group member |
| [addRadiusClient](#addradiusclient) | Add a new RADIUS client |
| [addScopeToClient](#addscopetoclient) | Add a scope to an OIDC client|
| [addScopeToUmaResource](#addscopetoumaresource) | Add a scope to an UMA resource |
| [create](#create) | Create a new configuration |
| [createAttribute](#createattribute) | Add a new attribute |
| [createClient](#createclient) | Add a new OpenID Connect client |
| [createCustomScript](#createcustomscript) | Add a new custom script |
| [createGroup](#creategroup) | Add a new group |
| [createPassportProvider](#createpassportprovider) | Add a new passport provider |
| [createPerson](#createperson) | Add a new person |
| [createScope](#createscope) | Add a new OpenID Connect scope |
| [createSectorIdentifier](#createsectoridentifier) | Add a new sector identifier |
| [createUmaResource](#createumaresource) | Add a new UMA resource|
| [createUmaScope](#createumascope) | Add a new UMA scope |
| [delete](#delete) | Delete an existing configuration |
| [deleteAllProviders](#deleteallproviders) | Delete all providers |
| [deleteAllUmaScopes](#deleteallumascopes) | Delete all UMA scopes |
| [deleteAttribute](#deleteattribute) | Delete an attribute |
| [deleteAttributes](#deleteattributes) | Delete all attributes |
| [deleteClient](#deleteclient) | Delete an OpenID Connect client |
| [deleteClientScopes](#deleteclientscopes) | Delete the scopes in an OpenID Connect Client |
| [deleteClients](#deleteclients) | Delete all clients|
| [deleteCustomScript](#deletecustomscript) | Delete a custom script |
| [deleteGroup](#deletegroup) | Delete a group |
| [deleteGroupMembers](#deletegroupmembers) | Delete the members of a group |
| [deleteGroups](#deletegroups) | Delete all groups |
| [deletePeople](#deletepeople) | Delete all people |
| [deletePerson](#deleteperson) | Delete a person |
| [deleteProvider](#deleteprovider) | Delete a passport provider|
| [deleteRadiusClient](#deleteradiusclient) | Delete a RADIUS client |
| [deleteScope](#deletescope) | Delete an OpenID Connect scope|
| [deleteScopes](#deletescopes) | Delete all OpenID Connect scopes |
| [deleteSectorIdentifier](#deletesectoridentifier) | Delete a Sector Identifier |
| [deleteUmaResource](#deleteumaresource) | Delete an UMA resource |
| [deleteUmaScope](#deleteumascope) | Delete an UMA scope |
| [getAllActiveAttributes](#getallactiveattributes) | Get all active attributes |
| [getAllAttributes](#getallattributes) | Get all attributes |
| [getAllInactiveAttributes](#getallinactiveattributes) | Get all inactive attributes |
| [getAllScopes](#getallscopes) | Get all scopes |
| [getAllSectorIdentifiers](#getallsectoridentifiers) | Get all sector identifiers |
| [getAttributeByInum](#getattributebyinum) | Get a specific attribute |
| [getCasConfig](#getcasconfig) | Get the existing configuration |
| [getClientByInum](#getclientbyinum) | Get a specific OpenID Connect client |
| [getClientScope](#getclientscope) | Get scopes assigned to an OpenID client |
| [getConfiguration](#getconfiguration) | Get Gluu configuration |
| [getCurrentAuthentication](#getcurrentauthentication) | Get current authentication methods |
| [getCustomScriptsByInum](#getcustomscriptsbyinum) | Get specific custom scripts |
| [getGroupByInum](#getgroupbyinum) | Get a specific group|
| [getGroupMembers](#getgroupmembers) | Get members of a specific group |
| [getOxAuthJsonSettings](#getoxauthjsonsettings) | Get oxAuth JSON configuration settings |
| [getOxtrustJsonSettings](#getoxtrustjsonsettings) | Get oxTrust JSON configuration settings |
| [getOxtrustSettings](#getoxtrustsettings) | get oxTrust configuration settings |
| [getPassportBasicConfig](#getpassportbasicconfig) | Get Passport's basic configuration |
| [getPersonByInum](#getpersonbyinum) | Get a specific person |
| [getProviderById](#getproviderbyid) | Get a specific Passport provider |
| [getRadiusClient](#getradiusclient) | Get a specific RADIUS client |
| [getScopeByInum](#getscopebyinum) | Get a specific OpenID Connect scope |
| [getScopeClaims](#getscopeclaims) | List all claims for a scope |
| [getSectorIdentifierById](#getsectoridentifierbyid) | Get a specific Sector Identifier |
| [getServerConfig](#getserverconfig) | Get RADIUS server configuration |
| [getServerStatus](#getserverstatus) | Get current server status|
| [getSmtpServerConfiguration](#getsmtpserverconfiguration) | Get SMTP server configuration|
| [getUmaResourceById](#getumaresourcebyid) | Get a specific UMA resource |
| [getUmaResourceClients](#getumaresourceclients) | Get the clients for a specific UMA resource |
| [getUmaResourceScopes](#getumaresourcescopes) | Get the scopes for a specific UMA resource |
| [getUmaScopeByInum](#getumascopebyinum) | Get a specific UMA scope |
| [listCertificates](#listcertificates) | List descriptions of the Gluu Server's certificates |
| [listClients](#listclients) | List all OpenID Connect clients |
| [listCustomScripts](#listcustomscripts) | List all custom scripts |
| [listCustomScriptsByType](#listcustomscriptsbytype) | List all person authentication scripts |
| [listGroups](#listgroups) | List all groups |
| [listPeople](#listpeople) | List all people |
| [listProviders](#listproviders) | List all Passport providers |
| [listRadiusClients](#listradiusclients) | List all RADIUS clients |
| [listUmaResources](#listumaresources) | List all UMA resources |
| [listUmaScopes](#listumascopes) | List UMA scopes |
| [read](#read) | Get the existing configuration |
| [removeClientToUmaResource](#removeclienttoumaresource) | Remove a client from an UMA resource |
| [removeGroupMember](#removegroupmember) | Remove a member from a group |
| [removeScopeToClient](#removescopetoclient) | Remove an existing scope from a client |
| [removeScopeToUmaResource](#removescopetoumaresource) | Remove a scope from an UMA resource |
| [searchAttributes](#searchattributes) | Search attributes |
| [searchGroups](#searchgroups) | Search OpenID Connect clients |
| [searchGroups1](#searchgroups1) | Search groups |
| [searchGroups2](#searchgroups2) | Search person |
| [searchScope](#searchscope) | Search OpenID Connect scopes |
| [searchSectorIdentifier](#searchsectoridentifier) | Search sector identifiers |
| [searchUmaResources](#searchumaresources) | Search UMA resources |
| [searchUmaScopes](#searchumascopes) | Search UMA scopes |
| [status](#status) | Check the status of a configuration |
| [status1](#status1) | Check the status of an existing configuration |
| [testSmtpConfiguration](#testsmtpconfiguration) | Test the SMTP configuration |
| [update](#update) | Update the configuration |
| [update1](#update1) | Update an existing configuration |
| [updateAttribute](#updateattribute) | Update a new attribute | 
| [updateAuthenticationMethod](#updateauthenticationmethod) | Update the authentication methods | 
| [updateClient](#updateclient) | Update an OpenID Connect client | 
| [updateCustomScript](#updatecustomscript) | Update a custom script | 
| [updateGroup](#updategroup) | Update a group |
| [updateGroup1](#updategroup1) | Update a person |
| [updateOxauthJsonSetting](#updateoxauthjsonsetting) | Update an oxAuth JSON configuration setting | 
| [updateOxtrustJsonSetting](#updateoxtrustjsonsetting) | Update an oxTrust JSON configuration setting |
| [updateOxtrustSetting](#updateoxtrustsetting) | Update oxTrust settings |
| [updatePassportBasicConfig](#updatepassportbasicconfig) | Update Passport basic configuration |
| [updatePassportProvider](#updatepassportprovider) | Update a Passport provider |
| [updateRadiusClient](#updateradiusclient) | Update RADIUS client |
| [updateScope](#updatescope) | Update an OpenID Connect scope|
| [updateSectorIdentifier](#updatesectoridentifier) | Update a sector identifier | 
| [updateServerConfiguration](#updateserverconfiguration) | Update the RADIUS server configuration |
| [updateSmtpConfiguration](#updatesmtpconfiguration) | Update the SMTP configuration |
| [updateUmaResource](#updateumaresource) | Update an UMA Resource |
| [updateUmaScope](#updateumascope)| Update an UMA scope |


## API References

### addClientToUmaResource

**URL**

```
//api/v1/uma/resources/{id}/clients/{inum}
```

**HTTP Method**
`POST`

**Response Type**

UmaResource

| Field | Data Type |
|---    | --- |
| `dn` | String |
| `inum` | String |
| `id` | String |
| `name` | String |
| `iconUri` | String |
| `scopes` | List |
| `scopeExpression` | String |
| `clients` | List|
| `resources` | List |
| `rev` | String |
| `creator` | String |
| `description` | String |
| `type` | String |
| `creationDate` | Date |
| `expirationDate` | Date |
| `deletable` | Boolean |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Path | `id` | String |
| Path | `inum` | String |

### addGroupMember

**URL**

```
//api/v1/groups/{inum}/members/{minum}
```

**HTTP Method**
`POST`

**Response Type**

String

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Path | `inum` | String |
| Path | `minum` | String |

### addRadiusClient

**URL**

```
//api/v1/radius/clients
```

**HTTP Method**
`POST`

**Response Type**

| Field | Data Type |
|---    | --- |
| `dn` | String | 
| `inum` | String |
| `name` | String | 
| `ipAddress` | String |
| `secret` | String | 
| `priority` | Integer |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Body | body | `RadiusClient(RadiusClient)` |

### addScopeToClient

**URL**

```
//api/v1/clients/{inum}/scopes/{sinum}
``` 

**HTTP Method**
`POST`

**Response Type**

string

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Path | `inum` | String |
| Path | `sinum` | String |

### addScopeToUmaResource

**URL**

```
//api/v1/uma/resources/{id}/scopes/{inum}
```

**HTTP Method**

`POST`

**Response Type**

UmaResource

| Field | Data Type |
|---    | --- |
| `dn` | String |
| `inum` | String |
| `id` | String |
| `name` | String |
| `iconUri` | String |
| `scopes` | List |
| `scopeExpression` | String
| `clients` | List|
| `resources` | List |
| `rev` | String |
| `creator` | String |
| `description` | String |
| `type` | String |
| `creationDate` | Date |
| `expirationDate` | Date |
| `deletable` | Boolean |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Path | `id` | String |
| Path | `inum` | String |

### create

**URL**

```
//api/v1/configuration/ldap
```

**HTTP Method**
`POST`

**Response Type**

LdapConfigurationDTO

| Field | Data Type |
|---    | --- |
| `configId` | String | 
| `bindDN` | String |
| `bindPassword` | String | 
| `servers` | List |
| `maxConnections` | Integer | 
| `useSSL` | Boolean |
| `baseDNs` | List |
| `primaryKey` | String | 
| `localPrimaryKey` | String | 
| `useAnonymousBind` | Boolean | 
| `enabled` | Boolean | 
| `level` | Integer |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Body | body | `LdapConfigurationDTO(LdapConfigurationDTO)` |

### createAttribute

**URL**

```
//api/v1/attributes
```

**HTTP Method**
`POST`

**Response Type**

GluuAttribute

| Field | Data Type | Options |
|---    | --- | --- |
| `dn` | String | |
| `selected` | Boolean | | 
| `inum` | String | | 
| `type` | String | | 
| `lifetime` | String | | 
| `sourceAttribute` | String | 
| `salt` | String |
| `nameIdType` | String | 
| `name` | String |
| `displayName` | String |  
| `description` | String |
| `origin` | String | 
| `dataType` | String | `string` |
| | | `numeric` |
| | | `boolean` |
| | | `binary` |
| | | `certificate` |
| | | `generalizedTime` |
| `editType` | List | |
| `viewType` | List | |
| `usageType` | List | |
| `oxAuthClaimName` | String | | 
| `seeAlso` | String | | 
| `status` | String | `active` | |
| | | `inactive` | |
| | | `expired` | | 
| | | `register` | |
| `saml1Uri` | String | |
| `saml2Uri` | String | |
| `urn` | String | |
| `oxSCIMCustomAttribute` | Boolean |  |
| `oxMultivaluedAttribute` | Boolean | |
| `custom` | Boolean | |
| `requred` | Boolean | |
| `attributeValidation` | AttributeValidation | | 
| `gluuTooltip` | String | |
| `adminCanAccess` | Boolean | |
| `adminCanView` | Boolean | |
| `adminCanEdit` | Boolean | |
| `userCanAccess` | Boolean | |
| `userCanView` | Boolean | |
| `whitePagesCanView` | Boolean | |  
| `userCanEdit` | Boolean | | 
| `baseDn` : String | | 

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Body | body | `GluuAttribute(GluuAttribute)` |

### createClient

**URL**

```
//api/v1/clients
```

**HTTP Method**
`POST`

**Response Type**

OxAuthClient

| Field | Data Type | Options |
|---    | --- | --- |
| `dn` | String | |
| `selected` | Boolean | | 
| `inum` | String | |
| `iname` | String | |
| `displayName` | String | | 
| `description` | String  | |
| `oxAuthAppType` | String | `web` |
| | | `native` |
| `contacts` | List | |
| `oxAuthRedirectURIs` | List | | 
| `oxAuthPostLogoutRedirectURIs` | List | |
| `oxAuthScopes` | List | |
| `oxAuthClaims` | List | |
| `encodedClientSecret` | String | | 
| `userPassword` | String | |
| `associatedPersons` | List | |
| `oxAuthTrustedClient` | Boolean | |
| `responseTypes` | List | |
| `grantTypes` | List | |
| `logoUri` | String | |
| `clientUri` | String | |
| `policyUri` | String | |
| `tosUri` | String | |
| `jwksUri` | String | |
| `jwks` | String | |
| `sectorIdentifierUri` | String | | 
| `subjectType` | String | `pairwise` |
| | | `public` |
| `idTokenTokenBindingCnf` | String | | 
| `rptAsJwt` | Boolean | |
| `accessTokenAsJwt` | Boolean | | 
| `accessTokenSigningAlg` | String | `none` |
| | | `HS256` |
| | | `HS384` |
| | | `HS512` |
| | | `RS256` |
| | | `RS384` |
| | | `RS512` |
| | | `ES256` |
| | | `ES384` |
| | | `ES512` |
| `idTokenSignedResponseAlg` | String |`none` |
| | | `HS256` |
| | | `HS384` |
| | | `HS512` |
| | | `RS256` |
| | | `RS384` |
| | | `RS512` |
| | | `ES256` |
| | | `ES384` |
| | | `ES512` |
| `idTokenEncryptedResponseAlg` | String | `RSA1_5` |
| | | `RSA-OAEP` |
| | | `A128KW` |
| | | `A256KW` |
| `idTokenEncryptedResponseEnc` | String | `A128CBC+HS256` |
| | | `A256CBC+HS512` |
| | | `A128GCM` |
| | | `A256GCM` |
| `userInfoSignedResponseAlg` | String | `none` |
| | | `HS256` |
| | | `HS384` |
| | | `HS512` |
| | | `RS256` |
| | | `RS384` |
| | | `RS512` |
| | | `ES256` |
| | | `ES384` |
| | | `ES512` |
| `userInfoEncryptedResponseAlg` | String | `RSA1_5` |
| | | `RSA-OAEP` |
| | | `A128KW` |
| | | `A256KW` |
| `userInfoEncryptedResponseEnc` | String |`A128CBC+HS256` |
| | | `A256CBC+HS512` |
| | | `A128GCM` |
| | | `A256GCM` |
| `requestObjectSigningAlg` | String | `none` |
| | | `HS256` |
| | | `HS384` |
| | | `HS512` |
| | | `RS256` |
| | | `RS384` |
| | | `RS512` |
| | | `ES256` |
| | | `ES384` |
| | | `ES512` |
| `requestObjectEncryptionAlg` | String | `RSA1_5` |
| | | `RSA-OAEP` |
| | | `A128KW` |
| | | `A256KW` |
| `requestObjectEncryptionEnc` | String | `A128CBC+HS256` |
| | | `A256CBC+HS512` |
| | | `A128GCM` |
| | | `A256GCM` |
| `tokenEndpointAuthMethod` | String | `client_secret_basic` |
| | | `client_secret_post` |
| | | `client_secret_jwt` |
| | | `private_key_jwt` |
| | | `none` |
| `tokenEndpointAuthSigningAlg` | String | `none` |
| | | `HS256` |
| | | `HS384` |
| | | `HS512` |
| | | `RS256` |
| | | `RS384` |
| | | `RS512` |
| | | `ES256` |
| | | `ES384` |
| | | `ES512` |
| `defaultMaxAge` | Integer | | 
| `requireAuthTime` | Boolean | |  
| `postLogoutRedirectUris` | List | | 
| `claimRedirectURI` | List | |
| `logoutUri` | List | |
| `logoutSessionRequired` | Boolean | |
| `oxAuthPersistClientAuthorizations` | Boolean | | 
| `oxIncludeClaimsInIdToken` | Boolean | |
| `oxRefreshTokenLifetime` | Integer | |
| `accessTokenLifetime` | Integer | |
| `defaultAcrValues` | List | |
| `initiateLoginUri` | String | |
| `clientSecretExpiresAt` | Date | |
| `requestUris` | List | |
| `authorizedOrigins` | List | | 
| `softwareId` | String | |
| `softwareVersion` | String | | 
| `softwareStatement` | String | |
| `disabled` | Boolean | |
| `oxdId` | String | |
| `oxAuthClientSecret` | String | | 
| `attributes` | ClientAttributes | |
| `baseDn` | String | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Body | body | `OxAuthClient(OxAuthClient)` |

### createCustomScript

**URL**

```
//api/v1/configuration/scripts
```

**HTTP Method**

`POST`

**Response Type**

CustomScript

| Field | Data Type | Options|
|---    | --- | --- |
| `dn` | String | |
| `inum` | String | | 
| `name` | String | | 
| `aliases` | List | | 
| `description` | String | | 
| `script` | String | | 
| `scriptType` | String | `person_authentication`
| | | `introspection` |
| | | `resource_owner_password_credentials` |
| | | `application_session` |
| | | `cache_refresh` |
| | | `update_user` |
| | | `user_registration` |
| | | `client_registration` |
| | | `id_generator` |
| | | `uma_rpt_policy` |
| | | `uma_claims_gathering` |
| | | `consent_gathering` |
| | | `dynamic_scope` |
| | | `scim` |
| `programmingLanguage` | String | `python` |
| | | `javascript` |
| `moduleProperties` | List | | 
| `configurationProperties` | List | | 
| `level` | Integer | |
| `revision` | Long | | 
| `enabled` | Boolean | | 
| `scriptError` | ScriptError | | 
| `modified` | Boolean | | 
| `internal` | Boolean | | 
| `locationType` | String | `ldap` |
| | | `file` |
| `locationPath` | String | | 
| `baseDn` | String | | 

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Body | body | `CustomScript(CustomScript)` |

### createGroup

**URL**

```
//api/v1/groups
```

**HTTP Method**
`POST`

**Response Type**

GluuGroupApi

| Field | Data Type | Options |
|---    | --- | --- |
| `inum` | String |  |
| `iname` | String | | 
| `displayName` | String | | 
| `description`  | String | | 
| `owner` | String | | 
| `members` | List | | 
| `organization` | String | | 
| `status` | String | `active` |
| | | `inactive` |
| | | `expired` |
| | | `register` |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| Body | body | `GluuGroupApi(GluuGroupApi)` |

### createPassportProvider

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### createPerson

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### createScope

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### createSectorIdentifier

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### createUmaResource

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### createUmaScope

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### delete

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteAllProviders

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteAllUmaScopes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteAttribute

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteAttributes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteClient

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteClientScopes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteClients

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteCustomScript

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteGroup

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteGroupMembers

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteGroups

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deletePeople

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deletePerson

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteProvider

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteRadiusClient

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteScope

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteScopes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteSectorIdentifier

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteUmaResource

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### deleteUmaScope

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getAllActiveAttributes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getAllAttributes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getAllInactiveAttributes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getAllScopes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getAllSectorIdentifiers

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getAttributeByInum

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getCasConfig

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getClientByInum

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getClientScope

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getConfiguration

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getCurrentAuthentication

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getCustomScriptsByInum

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getGroupByInum

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getGroupMembers

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getOxAuthJsonSettings

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getOxtrustJsonSettings

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getOxtrustSettings

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getPassportBasicConfig

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getPersonByInum

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getProviderById

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getRadiusClient

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getScopeByInum

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getScopeClaims

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getSectorIdentifierById

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getServerConfig

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getServerStatus

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getSmtpServerConfiguration

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getUmaResourceById

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getUmaResourceClients

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getUmaResourceScopes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### getUmaScopeByInum

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listCertificates

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listClients

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listCustomScripts

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listCustomScriptsByType

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listGroups

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listPeople

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listProviders

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listRadiusClients

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listUmaResources

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### listUmaScopes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### read

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### removeClientToUmaResource

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### removeGroupMember

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### removeScopeToClient

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### removeScopeToUmaResource

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### searchAttributes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### searchGroups

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### searchGroups1

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### searchGroups2

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### searchScope

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### searchSectorIdentifier

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### searchUmaResources

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### searchUmaScopes

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### status

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### status1

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### testSmtpConfiguration

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### update

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### update1

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateAttribute

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateAuthenticationMethod

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateClient

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateCustomScript

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateGroup

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateGroup1

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateOxauthJsonSetting

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateOxtrustJsonSetting

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateOxtrustSetting

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updatePassportBasicConfig

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updatePassportProvider

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateRadiusClient

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateScope

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateSectorIdentifier

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateServerConfiguration

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateSmtpConfiguration

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateUmaResource

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |

### updateUmaScope

**URL**

**HTTP Method**

**Response Type**

| Field | Data Type |
|---    | --- |
| | |

**Parameters**

| Location | Parameter Name | Input |
| --- | --- | --- |
| | |
