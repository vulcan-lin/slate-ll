---
title: LLdriver API v1
language_tabs:
  - shell: Shell
  - http: HTTP
  - javascript: JavaScript
  - ruby: Ruby
  - python: Python
  - php: PHP
  - java: Java
  - go: Go
toc_footers: []
includes: []
search: false
code_clipboard: true
highlight_theme: darkula
headingLevel: 2
generator: widdershins v4.0.1

---

<h1 id="lldriver-api">LLdriver API v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Welcome to the Yield Dance API! You can use our API to access lldriver  API endpoints.

Base URLs:

* <a href="http://localhost:4928/api/v1">http://localhost:4928/api/v1</a>

<h1 id="lldriver-api-authorization">Authorization</h1>

## post__admin_change_password

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v1/admin/change_password \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST http://localhost:4928/api/v1/admin/change_password HTTP/1.1
Host: localhost:4928
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v1/admin/change_password',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json',
  'Authorization' => 'string'
}

result = RestClient.post 'http://localhost:4928/api/v1/admin/change_password',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json',
  'Authorization': 'string'
}

r = requests.post('http://localhost:4928/api/v1/admin/change_password', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
    'Authorization' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://localhost:4928/api/v1/admin/change_password', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:4928/api/v1/admin/change_password");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
        "Authorization": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v1/admin/change_password", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /admin/change_password`

Change password of admin user

> Body parameter

```json
{
  "password": "string"
}
```

<h3 id="post__admin_change_password-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|body|body|[AdminChangePswReq](#schemaadminchangepswreq)|true|New password|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__admin_change_password-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__admin_login

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v1/admin/login \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://localhost:4928/api/v1/admin/login HTTP/1.1
Host: localhost:4928
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "mixin_user_id": "string",
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://localhost:4928/api/v1/admin/login',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://localhost:4928/api/v1/admin/login',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://localhost:4928/api/v1/admin/login', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://localhost:4928/api/v1/admin/login', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:4928/api/v1/admin/login");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v1/admin/login", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /admin/login`

Admin user login

> Body parameter

```json
{
  "mixin_user_id": "string",
  "password": "string"
}
```

<h3 id="post__admin_login-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AdminLoginReq](#schemaadminloginreq)|true|New password|

> Example responses

> 200 Response

```json
{
  "token": "string"
}
```

<h3 id="post__admin_login-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[AdminLoginResp](#schemaadminloginresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__auth

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v1/auth \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://localhost:4928/api/v1/auth HTTP/1.1
Host: localhost:4928
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "mixin_token": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://localhost:4928/api/v1/auth',
{
  method: 'POST',
  body: inputBody,
  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/json',
  'Accept' => 'application/json'
}

result = RestClient.post 'http://localhost:4928/api/v1/auth',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Content-Type': 'application/json',
  'Accept': 'application/json'
}

r = requests.post('http://localhost:4928/api/v1/auth', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Content-Type' => 'application/json',
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('POST','http://localhost:4928/api/v1/auth', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:4928/api/v1/auth");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("POST");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Content-Type": []string{"application/json"},
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v1/auth", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /auth`

Auth with Yield Dance. You must OAuth with mixin firstly to obtain the mixin token

> Body parameter

```json
{
  "mixin_token": "string"
}
```

<h3 id="post__auth-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[AuthReq](#schemaauthreq)|true|Yield Dance Auth request|

> Example responses

> 200 Response

```json
{
  "token": "string"
}
```

<h3 id="post__auth-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Response of Yield Dance auth|[AuthResp](#schemaauthresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__oauth

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v1/oauth?code=string \
  -H 'Accept: application/json'

```

```http
GET http://localhost:4928/api/v1/oauth?code=string HTTP/1.1
Host: localhost:4928
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://localhost:4928/api/v1/oauth?code=string',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'http://localhost:4928/api/v1/oauth',
  params: {
  'code' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://localhost:4928/api/v1/oauth', params={
  'code': 'string'
}, headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://localhost:4928/api/v1/oauth', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:4928/api/v1/oauth?code=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v1/oauth", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /oauth`

OAuth with Mixin

<h3 id="get__oauth-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|code|query|string|true|OAuth code from mixin|

> Example responses

> 200 Response

```json
{
  "access_token": "string",
  "scope": "string"
}
```

<h3 id="get__oauth-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Response of OAuth|[OAuthResp](#schemaoauthresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="lldriver-api-phrase">Phrase</h1>

## get__phrases_search

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v1/phrases/search \
  -H 'Accept: application/json'

```

```http
GET http://localhost:4928/api/v1/phrases/search HTTP/1.1
Host: localhost:4928
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://localhost:4928/api/v1/phrases/search',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'http://localhost:4928/api/v1/phrases/search',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://localhost:4928/api/v1/phrases/search', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://localhost:4928/api/v1/phrases/search', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:4928/api/v1/phrases/search");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v1/phrases/search", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /phrases/search`

return a video clips

<h3 id="get__phrases_search-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|phrase|query|string|false|Phrase|
|page_current|query|integer|false|current page index|
|page_size|query|integer|false|size of page|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "count": 0,
    "phrases": [
      {
        "id": "string",
        "movie": "string",
        "start": 0,
        "text": "string",
        "video-info": {
          "imdb": "string",
          "string": "string"
        },
        "video-url": "string"
      }
    ]
  },
  "msg": "string",
  "pagination": {
    "current": 0,
    "size": 0,
    "total": 0
  }
}
```

<h3 id="get__phrases_search-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Clips item|[SearchPhraseUrlResp](#schemasearchphraseurlresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__search_{phrase}

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v1/search/{phrase} \
  -H 'Accept: application/json'

```

```http
GET http://localhost:4928/api/v1/search/{phrase} HTTP/1.1
Host: localhost:4928
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://localhost:4928/api/v1/search/{phrase}',
{
  method: 'GET',

  headers: headers
})
.then(function(res) {
    return res.json();
}).then(function(body) {
    console.log(body);
});

```

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get 'http://localhost:4928/api/v1/search/{phrase}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://localhost:4928/api/v1/search/{phrase}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','http://localhost:4928/api/v1/search/{phrase}', array(
        'headers' => $headers,
        'json' => $request_body,
       )
    );
    print_r($response->getBody()->getContents());
 }
 catch (\GuzzleHttp\Exception\BadResponseException $e) {
    // handle exception or api errors.
    print_r($e->getMessage());
 }

 // ...

```

```java
URL obj = new URL("http://localhost:4928/api/v1/search/{phrase}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("GET");
int responseCode = con.getResponseCode();
BufferedReader in = new BufferedReader(
    new InputStreamReader(con.getInputStream()));
String inputLine;
StringBuffer response = new StringBuffer();
while ((inputLine = in.readLine()) != null) {
    response.append(inputLine);
}
in.close();
System.out.println(response.toString());

```

```go
package main

import (
       "bytes"
       "net/http"
)

func main() {

    headers := map[string][]string{
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v1/search/{phrase}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /search/{phrase}`

return a video clips

<h3 id="get__search_{phrase}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|phrase|path|string|true|Phrase|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    "string"
  ],
  "msg": "string"
}
```

<h3 id="get__search_{phrase}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Clips item|[SearchPhraseResp](#schemasearchphraseresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_AdminChangePswReq">AdminChangePswReq</h2>

<a id="schemaadminchangepswreq"></a>
<a id="schema_AdminChangePswReq"></a>
<a id="tocSadminchangepswreq"></a>
<a id="tocsadminchangepswreq"></a>

```json
{
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|password|string|true|none|none|

<h2 id="tocS_AdminLoginReq">AdminLoginReq</h2>

<a id="schemaadminloginreq"></a>
<a id="schema_AdminLoginReq"></a>
<a id="tocSadminloginreq"></a>
<a id="tocsadminloginreq"></a>

```json
{
  "mixin_user_id": "string",
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|mixin_user_id|string|true|none|none|
|password|string|true|none|none|

<h2 id="tocS_AdminLoginResp">AdminLoginResp</h2>

<a id="schemaadminloginresp"></a>
<a id="schema_AdminLoginResp"></a>
<a id="tocSadminloginresp"></a>
<a id="tocsadminloginresp"></a>

```json
{
  "token": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|token|string|false|none|none|

<h2 id="tocS_AuthReq">AuthReq</h2>

<a id="schemaauthreq"></a>
<a id="schema_AuthReq"></a>
<a id="tocSauthreq"></a>
<a id="tocsauthreq"></a>

```json
{
  "mixin_token": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|mixin_token|string|true|none|none|

<h2 id="tocS_AuthResp">AuthResp</h2>

<a id="schemaauthresp"></a>
<a id="schema_AuthResp"></a>
<a id="tocSauthresp"></a>
<a id="tocsauthresp"></a>

```json
{
  "token": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|token|string|false|none|none|

<h2 id="tocS_OAuthResp">OAuthResp</h2>

<a id="schemaoauthresp"></a>
<a id="schema_OAuthResp"></a>
<a id="tocSoauthresp"></a>
<a id="tocsoauthresp"></a>

```json
{
  "access_token": "string",
  "scope": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|access_token|string|false|none|none|
|scope|string|false|none|none|

<h2 id="tocS_Pagination">Pagination</h2>

<a id="schemapagination"></a>
<a id="schema_Pagination"></a>
<a id="tocSpagination"></a>
<a id="tocspagination"></a>

```json
{
  "current": 0,
  "size": 0,
  "total": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|current|integer|false|none|none|
|size|integer|false|none|none|
|total|integer|false|none|none|

<h2 id="tocS_Phrase">Phrase</h2>

<a id="schemaphrase"></a>
<a id="schema_Phrase"></a>
<a id="tocSphrase"></a>
<a id="tocsphrase"></a>

```json
{
  "id": "string",
  "movie": "string",
  "start": 0,
  "text": "string",
  "video-info": {
    "imdb": "string",
    "string": "string"
  },
  "video-url": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|string|false|none|none|
|movie|string|false|none|none|
|start|number|false|none|none|
|text|string|false|none|none|
|video-info|[VideoInfo](#schemavideoinfo)|false|none|none|
|video-url|string|false|none|none|

<h2 id="tocS_Phrases">Phrases</h2>

<a id="schemaphrases"></a>
<a id="schema_Phrases"></a>
<a id="tocSphrases"></a>
<a id="tocsphrases"></a>

```json
{
  "count": 0,
  "phrases": [
    {
      "id": "string",
      "movie": "string",
      "start": 0,
      "text": "string",
      "video-info": {
        "imdb": "string",
        "string": "string"
      },
      "video-url": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|count|integer|false|none|none|
|phrases|[[Phrase](#schemaphrase)]|false|none|none|

<h2 id="tocS_SearchPhraseResp">SearchPhraseResp</h2>

<a id="schemasearchphraseresp"></a>
<a id="schema_SearchPhraseResp"></a>
<a id="tocSsearchphraseresp"></a>
<a id="tocssearchphraseresp"></a>

```json
{
  "code": 0,
  "data": [
    "string"
  ],
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[string]|false|none|视频组ids|
|msg|string|false|none|none|

<h2 id="tocS_SearchPhraseUrlResp">SearchPhraseUrlResp</h2>

<a id="schemasearchphraseurlresp"></a>
<a id="schema_SearchPhraseUrlResp"></a>
<a id="tocSsearchphraseurlresp"></a>
<a id="tocssearchphraseurlresp"></a>

```json
{
  "code": 0,
  "data": {
    "count": 0,
    "phrases": [
      {
        "id": "string",
        "movie": "string",
        "start": 0,
        "text": "string",
        "video-info": {
          "imdb": "string",
          "string": "string"
        },
        "video-url": "string"
      }
    ]
  },
  "msg": "string",
  "pagination": {
    "current": 0,
    "size": 0,
    "total": 0
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[Phrases](#schemaphrases)|false|none|视频对象组|
|msg|string|false|none|none|
|pagination|[Pagination](#schemapagination)|false|none|none|

<h2 id="tocS_VideoInfo">VideoInfo</h2>

<a id="schemavideoinfo"></a>
<a id="schema_VideoInfo"></a>
<a id="tocSvideoinfo"></a>
<a id="tocsvideoinfo"></a>

```json
{
  "imdb": "string",
  "string": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|imdb|string|false|none|none|
|string|string|false|none|none|

<h2 id="tocS_commonResponse">commonResponse</h2>

<a id="schemacommonresponse"></a>
<a id="schema_commonResponse"></a>
<a id="tocScommonresponse"></a>
<a id="tocscommonresponse"></a>

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|any|false|none|none|
|msg|string|false|none|none|

