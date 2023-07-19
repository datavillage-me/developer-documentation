---
layout: default
title: Using the platform
---
# Using the platform

The Datavillage platform is accessible through several channels : 
 - the web UI
 - the Command Line Interface  
 - the Typescript client 
 - the HTTP API

## Web UI

### Obtaining an API token

## Command Line Interface

### Installation

The Datavillage Platform CLI can be installed from the public NPM registry, resulting in a global `datavillage` executable :
```bash
$> npm i @datavillage-me/platform-cli -g

$> datavillage --help
```
It can also be directly executed with `npx`:
```bash
$> npx @datavillage-me/platform-cli
```

### Authentication

The login command will open a browser window and redirect to the platform login page.
On success, the resulting token and the server URL will be stored in `$HOME/.datavillage/config.json`

```bash
# The default login flow uses the Dev login page (github)
$> datavillage auth login

# Force login as a user (using a pod provider)
$> datavillage auth login --user

# Force login to a specific server instance
$> datavillage auth login --url=https://api-dev.datavillage.me

# Display the current credentials
$> datavillage auth whoami
```

## Typescript API client  

The DataVillage Platform API provides an abstract access to all the functionalities exposed by the DataVillage platform.  
The Typescript API Client is an HTTP client that leverages the HTTP API (below).
It can be used in a Node environment or a browser.

### Instantiating the API client
The main method to obtain a client is
[`getRemoteClient`](./modules.html#getremoteclient) :
```typescript
import { getRemoteClient } from '@datavillage-me/api';

const client = getRemoteClient('https://api-dev.datavillage.me');
```
The client can then be used to get proxies to the different subcomponents of the platform :
```typescript
const consentManager = client.getConsentManager();
client.getConsentReceipts().then((receipts) => {...});
```

### Authentication

#### Providing the auth token (Node)
The remote client requires some valid authentication token to perform requests.   
In a Node environment, such an authentication token can be passed explicitly in the constructor method :
```typescript
const authToken = ...; // auth token obtained previously
const client = getRemoteClient('https://api-dev.datavillage.me', authToken);
```

#### Triggering the login flow in a browser
In a the browser environment, assuming the user has authenticated to the backend
previously, the authentication token present in the browser cookies will automatically be appended to outgoing requests.
In that case, the call to `getRemoteClient` can omit the auth token.

To obtain an authentication token as a browser cookie, the login flow has to be performed. This can be done by
redirecting the user to the URL provided by [`Client.getPassport().getAuthenticationUrl()`](./interfaces/passport.html#getauthenticationurl).  
Building that URL requires the pod type ('solid' or 'google'), the redirectUrl (where to go after the login succeeds),
and optionally the identity issuer (for Solid, this can be f.i. 'http://inrupt.net', 'https://solidcommunity.net').
```typescript
const client = getRemoteClient('https://api-dev.datavillage.me');
// let's return to this same page after login
const redirectUrl = window.location.href; 
// if issuer is not provided for Solid, a default one will be used
const authUrl = await client.getPassport().getAuthenticationUrl(POD_IDENTITY_PROVIDER.Solid, redirectUrl);

window.location.href = authUrl;
```

## HTTP API
All of the three previous methods actually rely on an HTTP API. That API can also be used directly.

### Authentication