---
title: CyberMem API v1
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
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="cybermem-api">CyberMem API v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Welcome to the CyberMem  API! You can use our API to access CyberMem  API endpoints.

Base URLs:

* <a href="https://api.dev.cybermem.com/api/v1">https://api.dev.cybermem.com/api/v1</a>

<h1 id="cybermem-api-chat">Chat</h1>

## post__chats

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/chats \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST https://api.dev.cybermem.com/api/v1/chats HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "robot_id": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://api.dev.cybermem.com/api/v1/chats',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/chats',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/chats', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/chats', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/chats");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/chats", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /chats`

new chat

> Body parameter

```json
{
  "robot_id": 0
}
```

<h3 id="post__chats-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|body|body|[ChatNewReq](#schemachatnewreq)|true|chat new request|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__chats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|chat context id|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__chats_qa

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/chats/qa \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST https://api.dev.cybermem.com/api/v1/chats/qa HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "context_id": "string",
  "message": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://api.dev.cybermem.com/api/v1/chats/qa',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/chats/qa',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/chats/qa', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/chats/qa', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/chats/qa");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/chats/qa", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /chats/qa`

chat

> Body parameter

```json
{
  "context_id": "string",
  "message": "string"
}
```

<h3 id="post__chats_qa-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|body|body|[ChatReq](#schemachatreq)|true|chat request|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__chats_qa-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__chats_stream-qa

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/chats/stream-qa \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST https://api.dev.cybermem.com/api/v1/chats/stream-qa HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "context_id": "string",
  "message": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://api.dev.cybermem.com/api/v1/chats/stream-qa',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/chats/stream-qa',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/chats/stream-qa', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/chats/stream-qa', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/chats/stream-qa");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/chats/stream-qa", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /chats/stream-qa`

stream chat

> Body parameter

```json
{
  "context_id": "string",
  "message": "string"
}
```

<h3 id="post__chats_stream-qa-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|body|body|[ChatReq](#schemachatreq)|true|chat request|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__chats_stream-qa-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__chats_{context_id}

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/chats/{context_id} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET https://api.dev.cybermem.com/api/v1/chats/{context_id} HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://api.dev.cybermem.com/api/v1/chats/{context_id}',
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
  'Accept' => 'application/json',
  'Authorization' => 'string'
}

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/chats/{context_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'string'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/chats/{context_id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/chats/{context_id}', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/chats/{context_id}");
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
        "Authorization": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/chats/{context_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /chats/{context_id}`

get chat

<h3 id="get__chats_{context_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|context_id|path|integer|true|chat context id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "context_id": "string",
    "created_at": "string",
    "edges": {
      "owner": {
        "created_at": "string",
        "edges": {
          "chats": [
            {}
          ],
          "owner": {
            "created_at": "string",
            "domain_id": "string",
            "edges": {
              "owner": {
                "created_at": "string",
                "edges": {
                  "domain": {},
                  "robots": [
                    {}
                  ]
                },
                "email": "string",
                "id": 0,
                "nickname": "string",
                "password": "string",
                "updated_at": "string"
              },
              "users": [
                {}
              ]
            },
            "id": 0,
            "name": "string",
            "updated_at": "string"
          }
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "openid": "string",
        "password": "string",
        "unionid": "string",
        "updated_at": "string",
        "user_type": "string"
      }
    },
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0,
    "updated_at": "string"
  },
  "msg": "string"
}
```

<h3 id="get__chats_{context_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|chat|[api_service.LoginResponse](#schemaapi_service.loginresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__s_chats

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/s/chats \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/s/chats HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "robot_uuid": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/s/chats',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/s/chats',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/s/chats', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/s/chats', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/s/chats");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/s/chats", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /s/chats`

无认证 匿名 new chat

> Body parameter

```json
{
  "robot_uuid": "string"
}
```

<h3 id="post__s_chats-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ChatShareNewReq](#schemachatsharenewreq)|true|chat new request|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__s_chats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|chat context id|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__s_chats_qa

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/s/chats/qa \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST https://api.dev.cybermem.com/api/v1/s/chats/qa HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "context_id": "string",
  "message": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://api.dev.cybermem.com/api/v1/s/chats/qa',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/s/chats/qa',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/s/chats/qa', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/s/chats/qa', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/s/chats/qa");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/s/chats/qa", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /s/chats/qa`

无认证 anonymous chat

> Body parameter

```json
{
  "context_id": "string",
  "message": "string"
}
```

<h3 id="post__s_chats_qa-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|body|body|[ChatReq](#schemachatreq)|true|chat request|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__s_chats_qa-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__s_chats_stream-qa

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/s/chats/stream-qa \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/s/chats/stream-qa HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "context_id": "string",
  "message": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/s/chats/stream-qa',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/s/chats/stream-qa',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/s/chats/stream-qa', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/s/chats/stream-qa', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/s/chats/stream-qa");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/s/chats/stream-qa", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /s/chats/stream-qa`

无认证匿名 stream chat

> Body parameter

```json
{
  "context_id": "string",
  "message": "string"
}
```

<h3 id="post__s_chats_stream-qa-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[ChatReq](#schemachatreq)|true|chat request|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__s_chats_stream-qa-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="cybermem-api-domain">Domain</h1>

## get__domains

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/domains \
  -H 'Accept: application/json'

```

```http
GET https://api.dev.cybermem.com/api/v1/domains HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/domains',
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

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/domains',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/domains', headers = headers)

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
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/domains', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/domains");
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
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/domains", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /domains`

list domain

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__domains-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__domains_{domain_id}

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/domains/{domain_id} \
  -H 'Accept: application/json'

```

```http
GET https://api.dev.cybermem.com/api/v1/domains/{domain_id} HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/domains/{domain_id}',
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

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/domains/{domain_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/domains/{domain_id}', headers = headers)

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
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/domains/{domain_id}', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/domains/{domain_id}");
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
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/domains/{domain_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /domains/{domain_id}`

get domain info

<h3 id="get__domains_{domain_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|domain_id|path|integer|true|domain id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__domains_{domain_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## patch__domains_{domain_id}

> Code samples

```shell
# You can also use wget
curl -X PATCH https://api.dev.cybermem.com/api/v1/domains/{domain_id}?name=string \
  -H 'Accept: application/json'

```

```http
PATCH https://api.dev.cybermem.com/api/v1/domains/{domain_id}?name=string HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/domains/{domain_id}?name=string',
{
  method: 'PATCH',

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

result = RestClient.patch 'https://api.dev.cybermem.com/api/v1/domains/{domain_id}',
  params: {
  'name' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.patch('https://api.dev.cybermem.com/api/v1/domains/{domain_id}', params={
  'name': 'string'
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
    $response = $client->request('PATCH','https://api.dev.cybermem.com/api/v1/domains/{domain_id}', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/domains/{domain_id}?name=string");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
    req, err := http.NewRequest("PATCH", "https://api.dev.cybermem.com/api/v1/domains/{domain_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /domains/{domain_id}`

update domain site name

<h3 id="patch__domains_{domain_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|domain_id|path|integer|true|domain id|
|name|query|string|true|new site name|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="patch__domains_{domain_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__domains_{domain_id}_robots

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/domains/{domain_id}/robots \
  -H 'Accept: application/json'

```

```http
GET https://api.dev.cybermem.com/api/v1/domains/{domain_id}/robots HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/domains/{domain_id}/robots',
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

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/domains/{domain_id}/robots',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/domains/{domain_id}/robots', headers = headers)

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
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/domains/{domain_id}/robots', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/domains/{domain_id}/robots");
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
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/domains/{domain_id}/robots", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /domains/{domain_id}/robots`

domain robot list

<h3 id="get__domains_{domain_id}_robots-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|domain_id|path|integer|true|domain id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "edges": {
        "config": {
          "created_at": "string",
          "edges": {
            "owner": {}
          },
          "id": 0,
          "openai_config": {
            "model": "string"
          },
          "openai_content": {
            "chat_with_db": true,
            "index_name": "string",
            "index_namespace": "string"
          },
          "updated_at": "string",
          "welcome": [
            {
              "ai": "string",
              "id": 0
            }
          ]
        },
        "files": [
          {
            "created_at": "string",
            "edges": {
              "owner": {}
            },
            "id": 0,
            "name": "string",
            "status": "string",
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "edges": {
            "domain": {
              "created_at": "string",
              "domain_id": "string",
              "edges": {
                "owner": {},
                "users": [
                  {
                    "created_at": "string",
                    "edges": {},
                    "email": "string",
                    "id": 0,
                    "nickname": "string",
                    "openid": "string",
                    "password": "string",
                    "unionid": "string",
                    "updated_at": "string",
                    "user_type": "string"
                  }
                ]
              },
              "id": 0,
              "name": "string",
              "updated_at": "string"
            },
            "robots": [
              {}
            ]
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string",
          "updated_at": "string"
        }
      },
      "id": 0,
      "name": "string",
      "prompt": "string",
      "share": "string",
      "updated_at": "string"
    }
  ],
  "msg": "string"
}
```

<h3 id="get__domains_{domain_id}_robots-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|RobotListResponse response|[RobotListResponse](#schemarobotlistresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__domains_{domain_id}_users

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users \
  -H 'Accept: application/json'

```

```http
GET https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users',
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

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users', headers = headers)

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
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users");
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
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /domains/{domain_id}/users`

domain user list

<h3 id="get__domains_{domain_id}_users-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|domain_id|path|integer|true|domain id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "created_at": "string",
      "edges": {
        "chats": [
          {
            "context_id": "string",
            "created_at": "string",
            "edges": {
              "owner": {}
            },
            "id": 0,
            "messages": [
              {
                "content": "string",
                "created": "string",
                "role": "string"
              }
            ],
            "robot_id": 0,
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "domain_id": "string",
          "edges": {
            "owner": {
              "created_at": "string",
              "edges": {
                "domain": {},
                "robots": [
                  {
                    "created_at": "string",
                    "description": "string",
                    "edges": {},
                    "id": 0,
                    "name": "string",
                    "prompt": "string",
                    "share": "string",
                    "updated_at": "string"
                  }
                ]
              },
              "email": "string",
              "id": 0,
              "nickname": "string",
              "password": "string",
              "updated_at": "string"
            },
            "users": [
              {}
            ]
          },
          "id": 0,
          "name": "string",
          "updated_at": "string"
        }
      },
      "email": "string",
      "id": 0,
      "nickname": "string",
      "openid": "string",
      "password": "string",
      "unionid": "string",
      "updated_at": "string",
      "user_type": "string"
    }
  ],
  "msg": "string"
}
```

<h3 id="get__domains_{domain_id}_users-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|domain list response|[DomainUserListResponse](#schemadomainuserlistresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__domains_{domain_id}_users

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "email": "string",
  "nick_name": "string",
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /domains/{domain_id}/users`

user register

> Body parameter

```json
{
  "email": "string",
  "nick_name": "string",
  "password": "string"
}
```

<h3 id="post__domains_{domain_id}_users-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|domain_id|path|integer|true|domain id|
|body|body|[UserRegisterReq](#schemauserregisterreq)|true|domain user register|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__domains_{domain_id}_users-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__domains_{domain_id}_users_login

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users/login \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users/login HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "email": "string",
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users/login',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users/login',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users/login', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users/login', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users/login");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/domains/{domain_id}/users/login", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /domains/{domain_id}/users/login`

domain user login

> Body parameter

```json
{
  "email": "string",
  "password": "string"
}
```

<h3 id="post__domains_{domain_id}_users_login-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|domain_id|path|integer|true|domain id|
|body|body|[LoginReq](#schemaloginreq)|true|login with email and password|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "context_id": "string",
    "created_at": "string",
    "edges": {
      "owner": {
        "created_at": "string",
        "edges": {
          "chats": [
            {}
          ],
          "owner": {
            "created_at": "string",
            "domain_id": "string",
            "edges": {
              "owner": {
                "created_at": "string",
                "edges": {
                  "domain": {},
                  "robots": [
                    {}
                  ]
                },
                "email": "string",
                "id": 0,
                "nickname": "string",
                "password": "string",
                "updated_at": "string"
              },
              "users": [
                {}
              ]
            },
            "id": 0,
            "name": "string",
            "updated_at": "string"
          }
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "openid": "string",
        "password": "string",
        "unionid": "string",
        "updated_at": "string",
        "user_type": "string"
      }
    },
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0,
    "updated_at": "string"
  },
  "msg": "string"
}
```

<h3 id="post__domains_{domain_id}_users_login-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Login response|[api_service.LoginResponse](#schemaapi_service.loginresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="cybermem-api-robot">Robot</h1>

## post__files

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/files \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/files HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/files',
{
  method: 'POST',

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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/files',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.post('https://api.dev.cybermem.com/api/v1/files', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/files', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/files");
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
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/files", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /files`

upload file

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    0
  ],
  "msg": "string"
}
```

<h3 id="post__files-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|UploadFileResp response|[UploadFileResp](#schemauploadfileresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__files_{fid}

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/files/{fid} \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/files/{fid} HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/files/{fid}',
{
  method: 'POST',

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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/files/{fid}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.post('https://api.dev.cybermem.com/api/v1/files/{fid}', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/files/{fid}', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/files/{fid}");
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
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/files/{fid}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /files/{fid}`

delete file

<h3 id="post__files_{fid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|fid|path|integer|true|file id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__files_{fid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__robots

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/robots \
  -H 'Accept: application/json'

```

```http
GET https://api.dev.cybermem.com/api/v1/robots HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/robots',
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

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/robots',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/robots', headers = headers)

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
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/robots', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/robots");
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
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/robots", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /robots`

robot list

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "edges": {
        "config": {
          "created_at": "string",
          "edges": {
            "owner": {}
          },
          "id": 0,
          "openai_config": {
            "model": "string"
          },
          "openai_content": {
            "chat_with_db": true,
            "index_name": "string",
            "index_namespace": "string"
          },
          "updated_at": "string",
          "welcome": [
            {
              "ai": "string",
              "id": 0
            }
          ]
        },
        "files": [
          {
            "created_at": "string",
            "edges": {
              "owner": {}
            },
            "id": 0,
            "name": "string",
            "status": "string",
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "edges": {
            "domain": {
              "created_at": "string",
              "domain_id": "string",
              "edges": {
                "owner": {},
                "users": [
                  {
                    "created_at": "string",
                    "edges": {},
                    "email": "string",
                    "id": 0,
                    "nickname": "string",
                    "openid": "string",
                    "password": "string",
                    "unionid": "string",
                    "updated_at": "string",
                    "user_type": "string"
                  }
                ]
              },
              "id": 0,
              "name": "string",
              "updated_at": "string"
            },
            "robots": [
              {}
            ]
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string",
          "updated_at": "string"
        }
      },
      "id": 0,
      "name": "string",
      "prompt": "string",
      "share": "string",
      "updated_at": "string"
    }
  ],
  "msg": "string"
}
```

<h3 id="get__robots-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|RobotListResponse response|[RobotListResponse](#schemarobotlistresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__robots

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/robots \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/robots HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "description": "string",
  "files": [
    0
  ],
  "name": "string",
  "prompt": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/robots',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/robots',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/robots', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/robots', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/robots");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/robots", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /robots`

create robot

> Body parameter

```json
{
  "description": "string",
  "files": [
    0
  ],
  "name": "string",
  "prompt": "string"
}
```

<h3 id="post__robots-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[RobotCreateReq](#schemarobotcreatereq)|true|user register|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__robots-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__robots_{robot_id}

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/robots/{robot_id} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET https://api.dev.cybermem.com/api/v1/robots/{robot_id} HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://api.dev.cybermem.com/api/v1/robots/{robot_id}',
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
  'Accept' => 'application/json',
  'Authorization' => 'string'
}

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/robots/{robot_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'string'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/robots/{robot_id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/robots/{robot_id}', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/robots/{robot_id}");
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
        "Authorization": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/robots/{robot_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /robots/{robot_id}`

query Robot

<h3 id="get__robots_{robot_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|robot_id|path|integer|true|robot id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__robots_{robot_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## delete__robots_{robot_id}

> Code samples

```shell
# You can also use wget
curl -X DELETE https://api.dev.cybermem.com/api/v1/robots/{robot_id} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
DELETE https://api.dev.cybermem.com/api/v1/robots/{robot_id} HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://api.dev.cybermem.com/api/v1/robots/{robot_id}',
{
  method: 'DELETE',

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
  'Accept' => 'application/json',
  'Authorization' => 'string'
}

result = RestClient.delete 'https://api.dev.cybermem.com/api/v1/robots/{robot_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'string'
}

r = requests.delete('https://api.dev.cybermem.com/api/v1/robots/{robot_id}', headers = headers)

print(r.json())

```

```php
<?php

require 'vendor/autoload.php';

$headers = array(
    'Accept' => 'application/json',
    'Authorization' => 'string',
);

$client = new \GuzzleHttp\Client();

// Define array of request body.
$request_body = array();

try {
    $response = $client->request('DELETE','https://api.dev.cybermem.com/api/v1/robots/{robot_id}', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/robots/{robot_id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("DELETE");
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
        "Authorization": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "https://api.dev.cybermem.com/api/v1/robots/{robot_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /robots/{robot_id}`

Delete Robot

<h3 id="delete__robots_{robot_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|robot_id|path|integer|true|robot id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="delete__robots_{robot_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## patch__robots_{robot_id}

> Code samples

```shell
# You can also use wget
curl -X PATCH https://api.dev.cybermem.com/api/v1/robots/{robot_id} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PATCH https://api.dev.cybermem.com/api/v1/robots/{robot_id} HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "description": "string",
  "files": [
    0
  ],
  "name": "string",
  "prompt": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/robots/{robot_id}',
{
  method: 'PATCH',
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

result = RestClient.patch 'https://api.dev.cybermem.com/api/v1/robots/{robot_id}',
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

r = requests.patch('https://api.dev.cybermem.com/api/v1/robots/{robot_id}', headers = headers)

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
    $response = $client->request('PATCH','https://api.dev.cybermem.com/api/v1/robots/{robot_id}', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/robots/{robot_id}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
    req, err := http.NewRequest("PATCH", "https://api.dev.cybermem.com/api/v1/robots/{robot_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /robots/{robot_id}`

create robot

> Body parameter

```json
{
  "description": "string",
  "files": [
    0
  ],
  "name": "string",
  "prompt": "string"
}
```

<h3 id="patch__robots_{robot_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|robot_id|path|integer|true|robot id|
|body|body|[RobotCreateReq](#schemarobotcreatereq)|true|update robot|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="patch__robots_{robot_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## patch__robots_{robot_id}_config

> Code samples

```shell
# You can also use wget
curl -X PATCH https://api.dev.cybermem.com/api/v1/robots/{robot_id}/config \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
PATCH https://api.dev.cybermem.com/api/v1/robots/{robot_id}/config HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "openai_config": {
    "model": "string"
  },
  "openai_content": {
    "chat_with_db": true,
    "index_name": "string",
    "index_namespace": "string"
  },
  "welcome_messages": [
    {
      "ai": "string",
      "id": 0
    }
  ]
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/robots/{robot_id}/config',
{
  method: 'PATCH',
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

result = RestClient.patch 'https://api.dev.cybermem.com/api/v1/robots/{robot_id}/config',
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

r = requests.patch('https://api.dev.cybermem.com/api/v1/robots/{robot_id}/config', headers = headers)

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
    $response = $client->request('PATCH','https://api.dev.cybermem.com/api/v1/robots/{robot_id}/config', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/robots/{robot_id}/config");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PATCH");
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
    req, err := http.NewRequest("PATCH", "https://api.dev.cybermem.com/api/v1/robots/{robot_id}/config", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PATCH /robots/{robot_id}/config`

update robot config

> Body parameter

```json
{
  "openai_config": {
    "model": "string"
  },
  "openai_content": {
    "chat_with_db": true,
    "index_name": "string",
    "index_namespace": "string"
  },
  "welcome_messages": [
    {
      "ai": "string",
      "id": 0
    }
  ]
}
```

<h3 id="patch__robots_{robot_id}_config-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|robot_id|path|integer|true|robot id|
|body|body|[RobotConfigReq](#schemarobotconfigreq)|true|update robot config|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="patch__robots_{robot_id}_config-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__s_robots_{robot_id}

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/s/robots/{robot_id} \
  -H 'Accept: application/json'

```

```http
GET https://api.dev.cybermem.com/api/v1/s/robots/{robot_id} HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/s/robots/{robot_id}',
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

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/s/robots/{robot_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/s/robots/{robot_id}', headers = headers)

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
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/s/robots/{robot_id}', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/s/robots/{robot_id}");
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
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/s/robots/{robot_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /s/robots/{robot_id}`

无认证查询 Robot

<h3 id="get__s_robots_{robot_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|robot_id|path|integer|true|robot id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__s_robots_{robot_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="cybermem-api-user">User</h1>

## post__user_login

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/user/login \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/user/login HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "email": "string",
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/user/login',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/user/login',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/user/login', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/user/login', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/user/login");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/user/login", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /user/login`

user login

> Body parameter

```json
{
  "email": "string",
  "password": "string"
}
```

<h3 id="post__user_login-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[LoginReq](#schemaloginreq)|true|login with email and password|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "context_id": "string",
    "created_at": "string",
    "edges": {
      "owner": {
        "created_at": "string",
        "edges": {
          "chats": [
            {}
          ],
          "owner": {
            "created_at": "string",
            "domain_id": "string",
            "edges": {
              "owner": {
                "created_at": "string",
                "edges": {
                  "domain": {},
                  "robots": [
                    {}
                  ]
                },
                "email": "string",
                "id": 0,
                "nickname": "string",
                "password": "string",
                "updated_at": "string"
              },
              "users": [
                {}
              ]
            },
            "id": 0,
            "name": "string",
            "updated_at": "string"
          }
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "openid": "string",
        "password": "string",
        "unionid": "string",
        "updated_at": "string",
        "user_type": "string"
      }
    },
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0,
    "updated_at": "string"
  },
  "msg": "string"
}
```

<h3 id="post__user_login-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Login response|[api_service.LoginResponse](#schemaapi_service.loginresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__user_register

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/user/register \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/user/register HTTP/1.1
Host: api.dev.cybermem.com
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "email": "string",
  "nick_name": "string",
  "password": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/user/register',
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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/user/register',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/user/register', headers = headers)

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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/user/register', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/user/register");
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
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/user/register", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /user/register`

user register

> Body parameter

```json
{
  "email": "string",
  "nick_name": "string",
  "password": "string"
}
```

<h3 id="post__user_register-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[UserRegisterReq](#schemauserregisterreq)|true|user register|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__user_register-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__users

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/users \
  -H 'Accept: application/json'

```

```http
GET https://api.dev.cybermem.com/api/v1/users HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/users',
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

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/users',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/users', headers = headers)

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
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/users', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/users");
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
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/users", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users`

user list

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "context_id": "string",
    "created_at": "string",
    "edges": {
      "owner": {
        "created_at": "string",
        "edges": {
          "chats": [
            {}
          ],
          "owner": {
            "created_at": "string",
            "domain_id": "string",
            "edges": {
              "owner": {
                "created_at": "string",
                "edges": {
                  "domain": {},
                  "robots": [
                    {}
                  ]
                },
                "email": "string",
                "id": 0,
                "nickname": "string",
                "password": "string",
                "updated_at": "string"
              },
              "users": [
                {}
              ]
            },
            "id": 0,
            "name": "string",
            "updated_at": "string"
          }
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "openid": "string",
        "password": "string",
        "unionid": "string",
        "updated_at": "string",
        "user_type": "string"
      }
    },
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0,
    "updated_at": "string"
  },
  "msg": "string"
}
```

<h3 id="get__users-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Login response|[api_service.LoginResponse](#schemaapi_service.loginresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__users_detail

> Code samples

```shell
# You can also use wget
curl -X GET https://api.dev.cybermem.com/api/v1/users/detail \
  -H 'Accept: application/json'

```

```http
GET https://api.dev.cybermem.com/api/v1/users/detail HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/users/detail',
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

result = RestClient.get 'https://api.dev.cybermem.com/api/v1/users/detail',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://api.dev.cybermem.com/api/v1/users/detail', headers = headers)

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
    $response = $client->request('GET','https://api.dev.cybermem.com/api/v1/users/detail', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/users/detail");
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
    req, err := http.NewRequest("GET", "https://api.dev.cybermem.com/api/v1/users/detail", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /users/detail`

get user detail

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__users_detail-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get user detail response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="cybermem-api-wechat">WeChat</h1>

## post__wx_{domain_id}_auth

> Code samples

```shell
# You can also use wget
curl -X POST https://api.dev.cybermem.com/api/v1/wx/{domain_id}/auth?code=string \
  -H 'Accept: application/json'

```

```http
POST https://api.dev.cybermem.com/api/v1/wx/{domain_id}/auth?code=string HTTP/1.1
Host: api.dev.cybermem.com
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://api.dev.cybermem.com/api/v1/wx/{domain_id}/auth?code=string',
{
  method: 'POST',

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

result = RestClient.post 'https://api.dev.cybermem.com/api/v1/wx/{domain_id}/auth',
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

r = requests.post('https://api.dev.cybermem.com/api/v1/wx/{domain_id}/auth', params={
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
    $response = $client->request('POST','https://api.dev.cybermem.com/api/v1/wx/{domain_id}/auth', array(
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
URL obj = new URL("https://api.dev.cybermem.com/api/v1/wx/{domain_id}/auth?code=string");
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
        "Accept": []string{"application/json"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://api.dev.cybermem.com/api/v1/wx/{domain_id}/auth", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /wx/{domain_id}/auth`

get openid

<h3 id="post__wx_{domain_id}_auth-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|code|query|string|true|wechat code|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__wx_{domain_id}_auth-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|ResponseCode2Session response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_ChatNewReq">ChatNewReq</h2>
<!-- backwards compatibility -->
<a id="schemachatnewreq"></a>
<a id="schema_ChatNewReq"></a>
<a id="tocSchatnewreq"></a>
<a id="tocschatnewreq"></a>

```json
{
  "robot_id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|robot_id|integer|true|none|none|

<h2 id="tocS_ChatReq">ChatReq</h2>
<!-- backwards compatibility -->
<a id="schemachatreq"></a>
<a id="schema_ChatReq"></a>
<a id="tocSchatreq"></a>
<a id="tocschatreq"></a>

```json
{
  "context_id": "string",
  "message": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|context_id|string|false|none|none|
|message|string|true|none|none|

<h2 id="tocS_ChatShareNewReq">ChatShareNewReq</h2>
<!-- backwards compatibility -->
<a id="schemachatsharenewreq"></a>
<a id="schema_ChatShareNewReq"></a>
<a id="tocSchatsharenewreq"></a>
<a id="tocschatsharenewreq"></a>

```json
{
  "robot_uuid": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|robot_uuid|string|true|none|none|

<h2 id="tocS_DomainUserListResponse">DomainUserListResponse</h2>
<!-- backwards compatibility -->
<a id="schemadomainuserlistresponse"></a>
<a id="schema_DomainUserListResponse"></a>
<a id="tocSdomainuserlistresponse"></a>
<a id="tocsdomainuserlistresponse"></a>

```json
{
  "code": 0,
  "data": [
    {
      "created_at": "string",
      "edges": {
        "chats": [
          {
            "context_id": "string",
            "created_at": "string",
            "edges": {
              "owner": {}
            },
            "id": 0,
            "messages": [
              {
                "content": "string",
                "created": "string",
                "role": "string"
              }
            ],
            "robot_id": 0,
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "domain_id": "string",
          "edges": {
            "owner": {
              "created_at": "string",
              "edges": {
                "domain": {},
                "robots": [
                  {
                    "created_at": "string",
                    "description": "string",
                    "edges": {},
                    "id": 0,
                    "name": "string",
                    "prompt": "string",
                    "share": "string",
                    "updated_at": "string"
                  }
                ]
              },
              "email": "string",
              "id": 0,
              "nickname": "string",
              "password": "string",
              "updated_at": "string"
            },
            "users": [
              {}
            ]
          },
          "id": 0,
          "name": "string",
          "updated_at": "string"
        }
      },
      "email": "string",
      "id": 0,
      "nickname": "string",
      "openid": "string",
      "password": "string",
      "unionid": "string",
      "updated_at": "string",
      "user_type": "string"
    }
  ],
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[[ent.DomainUser](#schemaent.domainuser)]|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_LoginReq">LoginReq</h2>
<!-- backwards compatibility -->
<a id="schemaloginreq"></a>
<a id="schema_LoginReq"></a>
<a id="tocSloginreq"></a>
<a id="tocsloginreq"></a>

```json
{
  "email": "string",
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|true|none|用户email地址|
|password|string|true|none|用户密码|

<h2 id="tocS_LoginResp">LoginResp</h2>
<!-- backwards compatibility -->
<a id="schemaloginresp"></a>
<a id="schema_LoginResp"></a>
<a id="tocSloginresp"></a>
<a id="tocsloginresp"></a>

```json
{
  "domain": {
    "created_at": "string",
    "domain_id": "string",
    "edges": {
      "owner": {
        "created_at": "string",
        "edges": {
          "domain": {},
          "robots": [
            {
              "created_at": "string",
              "description": "string",
              "edges": {
                "config": {
                  "created_at": "string",
                  "edges": {
                    "owner": {}
                  },
                  "id": 0,
                  "openai_config": {
                    "model": "string"
                  },
                  "openai_content": {
                    "chat_with_db": true,
                    "index_name": "string",
                    "index_namespace": "string"
                  },
                  "updated_at": "string",
                  "welcome": [
                    {}
                  ]
                },
                "files": [
                  {
                    "created_at": "string",
                    "edges": {},
                    "id": 0,
                    "name": "string",
                    "status": "string",
                    "updated_at": "string"
                  }
                ],
                "owner": {}
              },
              "id": 0,
              "name": "string",
              "prompt": "string",
              "share": "string",
              "updated_at": "string"
            }
          ]
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "password": "string",
        "updated_at": "string"
      },
      "users": [
        {
          "created_at": "string",
          "edges": {
            "chats": [
              {
                "context_id": "string",
                "created_at": "string",
                "edges": {
                  "owner": {}
                },
                "id": 0,
                "messages": [
                  {
                    "content": "string",
                    "created": "string",
                    "role": "string"
                  }
                ],
                "robot_id": 0,
                "updated_at": "string"
              }
            ],
            "owner": {}
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "openid": "string",
          "password": "string",
          "unionid": "string",
          "updated_at": "string",
          "user_type": "string"
        }
      ]
    },
    "id": 0,
    "name": "string",
    "updated_at": "string"
  },
  "email": "string",
  "nick_name": "string",
  "token": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|domain|[ent.Domain](#schemaent.domain)|false|none|none|
|email|string|false|none|用户email地址|
|nick_name|string|false|none|用户昵称|
|token|string|false|none|用户token|

<h2 id="tocS_RobotConfigReq">RobotConfigReq</h2>
<!-- backwards compatibility -->
<a id="schemarobotconfigreq"></a>
<a id="schema_RobotConfigReq"></a>
<a id="tocSrobotconfigreq"></a>
<a id="tocsrobotconfigreq"></a>

```json
{
  "openai_config": {
    "model": "string"
  },
  "openai_content": {
    "chat_with_db": true,
    "index_name": "string",
    "index_namespace": "string"
  },
  "welcome_messages": [
    {
      "ai": "string",
      "id": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|openai_config|[schema.OpenAIConfig](#schemaschema.openaiconfig)|false|none|none|
|openai_content|[schema.OpenAIContent](#schemaschema.openaicontent)|false|none|none|
|welcome_messages|[[schema.WelcomeMessage](#schemaschema.welcomemessage)]|false|none|none|

<h2 id="tocS_RobotCreateReq">RobotCreateReq</h2>
<!-- backwards compatibility -->
<a id="schemarobotcreatereq"></a>
<a id="schema_RobotCreateReq"></a>
<a id="tocSrobotcreatereq"></a>
<a id="tocsrobotcreatereq"></a>

```json
{
  "description": "string",
  "files": [
    0
  ],
  "name": "string",
  "prompt": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|description|string|true|none|description|
|files|[integer]|true|none|files|
|name|string|true|none|name|
|prompt|string|true|none|prompt|

<h2 id="tocS_RobotListResponse">RobotListResponse</h2>
<!-- backwards compatibility -->
<a id="schemarobotlistresponse"></a>
<a id="schema_RobotListResponse"></a>
<a id="tocSrobotlistresponse"></a>
<a id="tocsrobotlistresponse"></a>

```json
{
  "code": 0,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "edges": {
        "config": {
          "created_at": "string",
          "edges": {
            "owner": {}
          },
          "id": 0,
          "openai_config": {
            "model": "string"
          },
          "openai_content": {
            "chat_with_db": true,
            "index_name": "string",
            "index_namespace": "string"
          },
          "updated_at": "string",
          "welcome": [
            {
              "ai": "string",
              "id": 0
            }
          ]
        },
        "files": [
          {
            "created_at": "string",
            "edges": {
              "owner": {}
            },
            "id": 0,
            "name": "string",
            "status": "string",
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "edges": {
            "domain": {
              "created_at": "string",
              "domain_id": "string",
              "edges": {
                "owner": {},
                "users": [
                  {
                    "created_at": "string",
                    "edges": {},
                    "email": "string",
                    "id": 0,
                    "nickname": "string",
                    "openid": "string",
                    "password": "string",
                    "unionid": "string",
                    "updated_at": "string",
                    "user_type": "string"
                  }
                ]
              },
              "id": 0,
              "name": "string",
              "updated_at": "string"
            },
            "robots": [
              {}
            ]
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string",
          "updated_at": "string"
        }
      },
      "id": 0,
      "name": "string",
      "prompt": "string",
      "share": "string",
      "updated_at": "string"
    }
  ],
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[[ent.Robot](#schemaent.robot)]|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_UploadFileResp">UploadFileResp</h2>
<!-- backwards compatibility -->
<a id="schemauploadfileresp"></a>
<a id="schema_UploadFileResp"></a>
<a id="tocSuploadfileresp"></a>
<a id="tocsuploadfileresp"></a>

```json
{
  "code": 0,
  "data": [
    0
  ],
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[integer]|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_UserRegisterReq">UserRegisterReq</h2>
<!-- backwards compatibility -->
<a id="schemauserregisterreq"></a>
<a id="schema_UserRegisterReq"></a>
<a id="tocSuserregisterreq"></a>
<a id="tocsuserregisterreq"></a>

```json
{
  "email": "string",
  "nick_name": "string",
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|true|none|用户email地址|
|nick_name|string|true|none|用户nick_named|
|password|string|true|none|用户密码|

<h2 id="tocS_api_service.LoginResponse">api_service.LoginResponse</h2>
<!-- backwards compatibility -->
<a id="schemaapi_service.loginresponse"></a>
<a id="schema_api_service.LoginResponse"></a>
<a id="tocSapi_service.loginresponse"></a>
<a id="tocsapi_service.loginresponse"></a>

```json
{
  "code": 0,
  "data": {
    "context_id": "string",
    "created_at": "string",
    "edges": {
      "owner": {
        "created_at": "string",
        "edges": {
          "chats": [
            {}
          ],
          "owner": {
            "created_at": "string",
            "domain_id": "string",
            "edges": {
              "owner": {
                "created_at": "string",
                "edges": {
                  "domain": {},
                  "robots": [
                    {}
                  ]
                },
                "email": "string",
                "id": 0,
                "nickname": "string",
                "password": "string",
                "updated_at": "string"
              },
              "users": [
                {}
              ]
            },
            "id": 0,
            "name": "string",
            "updated_at": "string"
          }
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "openid": "string",
        "password": "string",
        "unionid": "string",
        "updated_at": "string",
        "user_type": "string"
      }
    },
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0,
    "updated_at": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[ent.Chat](#schemaent.chat)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_commonResponse">commonResponse</h2>
<!-- backwards compatibility -->
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

<h2 id="tocS_ent.Chat">ent.Chat</h2>
<!-- backwards compatibility -->
<a id="schemaent.chat"></a>
<a id="schema_ent.Chat"></a>
<a id="tocSent.chat"></a>
<a id="tocsent.chat"></a>

```json
{
  "context_id": "string",
  "created_at": "string",
  "edges": {
    "owner": {
      "created_at": "string",
      "edges": {
        "chats": [
          {
            "context_id": "string",
            "created_at": "string",
            "edges": {},
            "id": 0,
            "messages": [
              {
                "content": "string",
                "created": "string",
                "role": "string"
              }
            ],
            "robot_id": 0,
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "domain_id": "string",
          "edges": {
            "owner": {
              "created_at": "string",
              "edges": {
                "domain": {},
                "robots": [
                  {
                    "created_at": "string",
                    "description": "string",
                    "edges": {},
                    "id": 0,
                    "name": "string",
                    "prompt": "string",
                    "share": "string",
                    "updated_at": "string"
                  }
                ]
              },
              "email": "string",
              "id": 0,
              "nickname": "string",
              "password": "string",
              "updated_at": "string"
            },
            "users": [
              {}
            ]
          },
          "id": 0,
          "name": "string",
          "updated_at": "string"
        }
      },
      "email": "string",
      "id": 0,
      "nickname": "string",
      "openid": "string",
      "password": "string",
      "unionid": "string",
      "updated_at": "string",
      "user_type": "string"
    }
  },
  "id": 0,
  "messages": [
    {
      "content": "string",
      "created": "string",
      "role": "string"
    }
  ],
  "robot_id": 0,
  "updated_at": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|context_id|string|false|none|ContextID holds the value of the "context_id" field.|
|created_at|string|false|none|CreatedAt holds the value of the "created_at" field.|
|edges|[ent.ChatEdges](#schemaent.chatedges)|false|none|none|
|id|integer|false|none|ID of the ent.|
|messages|[[schema.Message](#schemaschema.message)]|false|none|Messages holds the value of the "messages" field.|
|robot_id|integer|false|none|RobotID holds the value of the "robot_id" field.|
|updated_at|string|false|none|UpdatedAt holds the value of the "updated_at" field.|

<h2 id="tocS_ent.ChatEdges">ent.ChatEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.chatedges"></a>
<a id="schema_ent.ChatEdges"></a>
<a id="tocSent.chatedges"></a>
<a id="tocsent.chatedges"></a>

```json
{
  "owner": {
    "created_at": "string",
    "edges": {
      "chats": [
        {
          "context_id": "string",
          "created_at": "string",
          "edges": {
            "owner": {}
          },
          "id": 0,
          "messages": [
            {
              "content": "string",
              "created": "string",
              "role": "string"
            }
          ],
          "robot_id": 0,
          "updated_at": "string"
        }
      ],
      "owner": {
        "created_at": "string",
        "domain_id": "string",
        "edges": {
          "owner": {
            "created_at": "string",
            "edges": {
              "domain": {},
              "robots": [
                {
                  "created_at": "string",
                  "description": "string",
                  "edges": {
                    "config": {},
                    "files": [],
                    "owner": {}
                  },
                  "id": 0,
                  "name": "string",
                  "prompt": "string",
                  "share": "string",
                  "updated_at": "string"
                }
              ]
            },
            "email": "string",
            "id": 0,
            "nickname": "string",
            "password": "string",
            "updated_at": "string"
          },
          "users": [
            {}
          ]
        },
        "id": 0,
        "name": "string",
        "updated_at": "string"
      }
    },
    "email": "string",
    "id": 0,
    "nickname": "string",
    "openid": "string",
    "password": "string",
    "unionid": "string",
    "updated_at": "string",
    "user_type": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|owner|[ent.DomainUser](#schemaent.domainuser)|false|none|none|

<h2 id="tocS_ent.Domain">ent.Domain</h2>
<!-- backwards compatibility -->
<a id="schemaent.domain"></a>
<a id="schema_ent.Domain"></a>
<a id="tocSent.domain"></a>
<a id="tocsent.domain"></a>

```json
{
  "created_at": "string",
  "domain_id": "string",
  "edges": {
    "owner": {
      "created_at": "string",
      "edges": {
        "domain": {
          "created_at": "string",
          "domain_id": "string",
          "edges": {},
          "id": 0,
          "name": "string",
          "updated_at": "string"
        },
        "robots": [
          {
            "created_at": "string",
            "description": "string",
            "edges": {
              "config": {
                "created_at": "string",
                "edges": {
                  "owner": {}
                },
                "id": 0,
                "openai_config": {
                  "model": "string"
                },
                "openai_content": {
                  "chat_with_db": true,
                  "index_name": "string",
                  "index_namespace": "string"
                },
                "updated_at": "string",
                "welcome": [
                  {
                    "ai": "string",
                    "id": 0
                  }
                ]
              },
              "files": [
                {
                  "created_at": "string",
                  "edges": {
                    "owner": {}
                  },
                  "id": 0,
                  "name": "string",
                  "status": "string",
                  "updated_at": "string"
                }
              ],
              "owner": {}
            },
            "id": 0,
            "name": "string",
            "prompt": "string",
            "share": "string",
            "updated_at": "string"
          }
        ]
      },
      "email": "string",
      "id": 0,
      "nickname": "string",
      "password": "string",
      "updated_at": "string"
    },
    "users": [
      {
        "created_at": "string",
        "edges": {
          "chats": [
            {
              "context_id": "string",
              "created_at": "string",
              "edges": {
                "owner": {}
              },
              "id": 0,
              "messages": [
                {
                  "content": "string",
                  "created": "string",
                  "role": "string"
                }
              ],
              "robot_id": 0,
              "updated_at": "string"
            }
          ],
          "owner": {
            "created_at": "string",
            "domain_id": "string",
            "edges": {},
            "id": 0,
            "name": "string",
            "updated_at": "string"
          }
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "openid": "string",
        "password": "string",
        "unionid": "string",
        "updated_at": "string",
        "user_type": "string"
      }
    ]
  },
  "id": 0,
  "name": "string",
  "updated_at": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_at|string|false|none|CreatedAt holds the value of the "created_at" field.|
|domain_id|string|false|none|DomainID holds the value of the "domain_id" field.|
|edges|[ent.DomainEdges](#schemaent.domainedges)|false|none|none|
|id|integer|false|none|ID of the ent.|
|name|string|false|none|Name holds the value of the "name" field.|
|updated_at|string|false|none|UpdatedAt holds the value of the "updated_at" field.|

<h2 id="tocS_ent.DomainEdges">ent.DomainEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.domainedges"></a>
<a id="schema_ent.DomainEdges"></a>
<a id="tocSent.domainedges"></a>
<a id="tocsent.domainedges"></a>

```json
{
  "owner": {
    "created_at": "string",
    "edges": {
      "domain": {
        "created_at": "string",
        "domain_id": "string",
        "edges": {
          "owner": {},
          "users": [
            {
              "created_at": "string",
              "edges": {
                "chats": [
                  {
                    "context_id": "string",
                    "created_at": "string",
                    "edges": {},
                    "id": 0,
                    "messages": [],
                    "robot_id": 0,
                    "updated_at": "string"
                  }
                ],
                "owner": {}
              },
              "email": "string",
              "id": 0,
              "nickname": "string",
              "openid": "string",
              "password": "string",
              "unionid": "string",
              "updated_at": "string",
              "user_type": "string"
            }
          ]
        },
        "id": 0,
        "name": "string",
        "updated_at": "string"
      },
      "robots": [
        {
          "created_at": "string",
          "description": "string",
          "edges": {
            "config": {
              "created_at": "string",
              "edges": {
                "owner": {}
              },
              "id": 0,
              "openai_config": {
                "model": "string"
              },
              "openai_content": {
                "chat_with_db": true,
                "index_name": "string",
                "index_namespace": "string"
              },
              "updated_at": "string",
              "welcome": [
                {
                  "ai": "string",
                  "id": 0
                }
              ]
            },
            "files": [
              {
                "created_at": "string",
                "edges": {
                  "owner": {}
                },
                "id": 0,
                "name": "string",
                "status": "string",
                "updated_at": "string"
              }
            ],
            "owner": {}
          },
          "id": 0,
          "name": "string",
          "prompt": "string",
          "share": "string",
          "updated_at": "string"
        }
      ]
    },
    "email": "string",
    "id": 0,
    "nickname": "string",
    "password": "string",
    "updated_at": "string"
  },
  "users": [
    {
      "created_at": "string",
      "edges": {
        "chats": [
          {
            "context_id": "string",
            "created_at": "string",
            "edges": {
              "owner": {}
            },
            "id": 0,
            "messages": [
              {
                "content": "string",
                "created": "string",
                "role": "string"
              }
            ],
            "robot_id": 0,
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "domain_id": "string",
          "edges": {
            "owner": {
              "created_at": "string",
              "edges": {
                "domain": {},
                "robots": [
                  {
                    "created_at": "string",
                    "description": "string",
                    "edges": {},
                    "id": 0,
                    "name": "string",
                    "prompt": "string",
                    "share": "string",
                    "updated_at": "string"
                  }
                ]
              },
              "email": "string",
              "id": 0,
              "nickname": "string",
              "password": "string",
              "updated_at": "string"
            },
            "users": []
          },
          "id": 0,
          "name": "string",
          "updated_at": "string"
        }
      },
      "email": "string",
      "id": 0,
      "nickname": "string",
      "openid": "string",
      "password": "string",
      "unionid": "string",
      "updated_at": "string",
      "user_type": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|owner|[ent.User](#schemaent.user)|false|none|none|
|users|[[ent.DomainUser](#schemaent.domainuser)]|false|none|Users holds the value of the users edge.|

<h2 id="tocS_ent.DomainUser">ent.DomainUser</h2>
<!-- backwards compatibility -->
<a id="schemaent.domainuser"></a>
<a id="schema_ent.DomainUser"></a>
<a id="tocSent.domainuser"></a>
<a id="tocsent.domainuser"></a>

```json
{
  "created_at": "string",
  "edges": {
    "chats": [
      {
        "context_id": "string",
        "created_at": "string",
        "edges": {
          "owner": {
            "created_at": "string",
            "edges": {},
            "email": "string",
            "id": 0,
            "nickname": "string",
            "openid": "string",
            "password": "string",
            "unionid": "string",
            "updated_at": "string",
            "user_type": "string"
          }
        },
        "id": 0,
        "messages": [
          {
            "content": "string",
            "created": "string",
            "role": "string"
          }
        ],
        "robot_id": 0,
        "updated_at": "string"
      }
    ],
    "owner": {
      "created_at": "string",
      "domain_id": "string",
      "edges": {
        "owner": {
          "created_at": "string",
          "edges": {
            "domain": {},
            "robots": [
              {
                "created_at": "string",
                "description": "string",
                "edges": {
                  "config": {
                    "created_at": "string",
                    "edges": {},
                    "id": 0,
                    "openai_config": {},
                    "openai_content": {},
                    "updated_at": "string",
                    "welcome": []
                  },
                  "files": [
                    {}
                  ],
                  "owner": {}
                },
                "id": 0,
                "name": "string",
                "prompt": "string",
                "share": "string",
                "updated_at": "string"
              }
            ]
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string",
          "updated_at": "string"
        },
        "users": [
          {
            "created_at": "string",
            "edges": {},
            "email": "string",
            "id": 0,
            "nickname": "string",
            "openid": "string",
            "password": "string",
            "unionid": "string",
            "updated_at": "string",
            "user_type": "string"
          }
        ]
      },
      "id": 0,
      "name": "string",
      "updated_at": "string"
    }
  },
  "email": "string",
  "id": 0,
  "nickname": "string",
  "openid": "string",
  "password": "string",
  "unionid": "string",
  "updated_at": "string",
  "user_type": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_at|string|false|none|CreatedAt holds the value of the "created_at" field.|
|edges|[ent.DomainUserEdges](#schemaent.domainuseredges)|false|none|none|
|email|string|false|none|Email holds the value of the "email" field.|
|id|integer|false|none|ID of the ent.|
|nickname|string|false|none|Nickname holds the value of the "nickname" field.|
|openid|string|false|none|Openid holds the value of the "openid" field.|
|password|string|false|none|Password holds the value of the "password" field.|
|unionid|string|false|none|Unionid holds the value of the "unionid" field.|
|updated_at|string|false|none|UpdatedAt holds the value of the "updated_at" field.|
|user_type|string|false|none|UserType holds the value of the "user_type" field.|

<h2 id="tocS_ent.DomainUserEdges">ent.DomainUserEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.domainuseredges"></a>
<a id="schema_ent.DomainUserEdges"></a>
<a id="tocSent.domainuseredges"></a>
<a id="tocsent.domainuseredges"></a>

```json
{
  "chats": [
    {
      "context_id": "string",
      "created_at": "string",
      "edges": {
        "owner": {
          "created_at": "string",
          "edges": {
            "chats": [],
            "owner": {
              "created_at": "string",
              "domain_id": "string",
              "edges": {
                "owner": {
                  "created_at": "string",
                  "edges": {
                    "domain": {},
                    "robots": []
                  },
                  "email": "string",
                  "id": 0,
                  "nickname": "string",
                  "password": "string",
                  "updated_at": "string"
                },
                "users": [
                  {}
                ]
              },
              "id": 0,
              "name": "string",
              "updated_at": "string"
            }
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "openid": "string",
          "password": "string",
          "unionid": "string",
          "updated_at": "string",
          "user_type": "string"
        }
      },
      "id": 0,
      "messages": [
        {
          "content": "string",
          "created": "string",
          "role": "string"
        }
      ],
      "robot_id": 0,
      "updated_at": "string"
    }
  ],
  "owner": {
    "created_at": "string",
    "domain_id": "string",
    "edges": {
      "owner": {
        "created_at": "string",
        "edges": {
          "domain": {},
          "robots": [
            {
              "created_at": "string",
              "description": "string",
              "edges": {
                "config": {
                  "created_at": "string",
                  "edges": {
                    "owner": {}
                  },
                  "id": 0,
                  "openai_config": {
                    "model": "string"
                  },
                  "openai_content": {
                    "chat_with_db": true,
                    "index_name": "string",
                    "index_namespace": "string"
                  },
                  "updated_at": "string",
                  "welcome": [
                    {}
                  ]
                },
                "files": [
                  {
                    "created_at": "string",
                    "edges": {},
                    "id": 0,
                    "name": "string",
                    "status": "string",
                    "updated_at": "string"
                  }
                ],
                "owner": {}
              },
              "id": 0,
              "name": "string",
              "prompt": "string",
              "share": "string",
              "updated_at": "string"
            }
          ]
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "password": "string",
        "updated_at": "string"
      },
      "users": [
        {
          "created_at": "string",
          "edges": {
            "chats": [
              {
                "context_id": "string",
                "created_at": "string",
                "edges": {
                  "owner": {}
                },
                "id": 0,
                "messages": [
                  {
                    "content": "string",
                    "created": "string",
                    "role": "string"
                  }
                ],
                "robot_id": 0,
                "updated_at": "string"
              }
            ],
            "owner": {}
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "openid": "string",
          "password": "string",
          "unionid": "string",
          "updated_at": "string",
          "user_type": "string"
        }
      ]
    },
    "id": 0,
    "name": "string",
    "updated_at": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|chats|[[ent.Chat](#schemaent.chat)]|false|none|Chats holds the value of the chats edge.|
|owner|[ent.Domain](#schemaent.domain)|false|none|none|

<h2 id="tocS_ent.File">ent.File</h2>
<!-- backwards compatibility -->
<a id="schemaent.file"></a>
<a id="schema_ent.File"></a>
<a id="tocSent.file"></a>
<a id="tocsent.file"></a>

```json
{
  "created_at": "string",
  "edges": {
    "owner": {
      "created_at": "string",
      "description": "string",
      "edges": {
        "config": {
          "created_at": "string",
          "edges": {
            "owner": {}
          },
          "id": 0,
          "openai_config": {
            "model": "string"
          },
          "openai_content": {
            "chat_with_db": true,
            "index_name": "string",
            "index_namespace": "string"
          },
          "updated_at": "string",
          "welcome": [
            {
              "ai": "string",
              "id": 0
            }
          ]
        },
        "files": [
          {
            "created_at": "string",
            "edges": {},
            "id": 0,
            "name": "string",
            "status": "string",
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "edges": {
            "domain": {
              "created_at": "string",
              "domain_id": "string",
              "edges": {
                "owner": {},
                "users": [
                  {
                    "created_at": "string",
                    "edges": {},
                    "email": "string",
                    "id": 0,
                    "nickname": "string",
                    "openid": "string",
                    "password": "string",
                    "unionid": "string",
                    "updated_at": "string",
                    "user_type": "string"
                  }
                ]
              },
              "id": 0,
              "name": "string",
              "updated_at": "string"
            },
            "robots": [
              {}
            ]
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string",
          "updated_at": "string"
        }
      },
      "id": 0,
      "name": "string",
      "prompt": "string",
      "share": "string",
      "updated_at": "string"
    }
  },
  "id": 0,
  "name": "string",
  "status": "string",
  "updated_at": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_at|string|false|none|CreatedAt holds the value of the "created_at" field.|
|edges|[ent.FileEdges](#schemaent.fileedges)|false|none|none|
|id|integer|false|none|ID of the ent.|
|name|string|false|none|Name holds the value of the "name" field.|
|status|string|false|none|Status holds the value of the "status" field.|
|updated_at|string|false|none|UpdatedAt holds the value of the "updated_at" field.|

<h2 id="tocS_ent.FileEdges">ent.FileEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.fileedges"></a>
<a id="schema_ent.FileEdges"></a>
<a id="tocSent.fileedges"></a>
<a id="tocsent.fileedges"></a>

```json
{
  "owner": {
    "created_at": "string",
    "description": "string",
    "edges": {
      "config": {
        "created_at": "string",
        "edges": {
          "owner": {}
        },
        "id": 0,
        "openai_config": {
          "model": "string"
        },
        "openai_content": {
          "chat_with_db": true,
          "index_name": "string",
          "index_namespace": "string"
        },
        "updated_at": "string",
        "welcome": [
          {
            "ai": "string",
            "id": 0
          }
        ]
      },
      "files": [
        {
          "created_at": "string",
          "edges": {
            "owner": {}
          },
          "id": 0,
          "name": "string",
          "status": "string",
          "updated_at": "string"
        }
      ],
      "owner": {
        "created_at": "string",
        "edges": {
          "domain": {
            "created_at": "string",
            "domain_id": "string",
            "edges": {
              "owner": {},
              "users": [
                {
                  "created_at": "string",
                  "edges": {
                    "chats": [],
                    "owner": {}
                  },
                  "email": "string",
                  "id": 0,
                  "nickname": "string",
                  "openid": "string",
                  "password": "string",
                  "unionid": "string",
                  "updated_at": "string",
                  "user_type": "string"
                }
              ]
            },
            "id": 0,
            "name": "string",
            "updated_at": "string"
          },
          "robots": [
            {}
          ]
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "password": "string",
        "updated_at": "string"
      }
    },
    "id": 0,
    "name": "string",
    "prompt": "string",
    "share": "string",
    "updated_at": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|owner|[ent.Robot](#schemaent.robot)|false|none|none|

<h2 id="tocS_ent.Robot">ent.Robot</h2>
<!-- backwards compatibility -->
<a id="schemaent.robot"></a>
<a id="schema_ent.Robot"></a>
<a id="tocSent.robot"></a>
<a id="tocsent.robot"></a>

```json
{
  "created_at": "string",
  "description": "string",
  "edges": {
    "config": {
      "created_at": "string",
      "edges": {
        "owner": {
          "created_at": "string",
          "description": "string",
          "edges": {},
          "id": 0,
          "name": "string",
          "prompt": "string",
          "share": "string",
          "updated_at": "string"
        }
      },
      "id": 0,
      "openai_config": {
        "model": "string"
      },
      "openai_content": {
        "chat_with_db": true,
        "index_name": "string",
        "index_namespace": "string"
      },
      "updated_at": "string",
      "welcome": [
        {
          "ai": "string",
          "id": 0
        }
      ]
    },
    "files": [
      {
        "created_at": "string",
        "edges": {
          "owner": {
            "created_at": "string",
            "description": "string",
            "edges": {},
            "id": 0,
            "name": "string",
            "prompt": "string",
            "share": "string",
            "updated_at": "string"
          }
        },
        "id": 0,
        "name": "string",
        "status": "string",
        "updated_at": "string"
      }
    ],
    "owner": {
      "created_at": "string",
      "edges": {
        "domain": {
          "created_at": "string",
          "domain_id": "string",
          "edges": {
            "owner": {},
            "users": [
              {
                "created_at": "string",
                "edges": {
                  "chats": [
                    {}
                  ],
                  "owner": {}
                },
                "email": "string",
                "id": 0,
                "nickname": "string",
                "openid": "string",
                "password": "string",
                "unionid": "string",
                "updated_at": "string",
                "user_type": "string"
              }
            ]
          },
          "id": 0,
          "name": "string",
          "updated_at": "string"
        },
        "robots": [
          {
            "created_at": "string",
            "description": "string",
            "edges": {},
            "id": 0,
            "name": "string",
            "prompt": "string",
            "share": "string",
            "updated_at": "string"
          }
        ]
      },
      "email": "string",
      "id": 0,
      "nickname": "string",
      "password": "string",
      "updated_at": "string"
    }
  },
  "id": 0,
  "name": "string",
  "prompt": "string",
  "share": "string",
  "updated_at": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_at|string|false|none|CreatedAt holds the value of the "created_at" field.|
|description|string|false|none|Description holds the value of the "description" field.|
|edges|[ent.RobotEdges](#schemaent.robotedges)|false|none|none|
|id|integer|false|none|ID of the ent.|
|name|string|false|none|Name holds the value of the "name" field.|
|prompt|string|false|none|Prompt holds the value of the "prompt" field.|
|share|string|false|none|Share holds the value of the "share" field.|
|updated_at|string|false|none|UpdatedAt holds the value of the "updated_at" field.|

<h2 id="tocS_ent.RobotConfig">ent.RobotConfig</h2>
<!-- backwards compatibility -->
<a id="schemaent.robotconfig"></a>
<a id="schema_ent.RobotConfig"></a>
<a id="tocSent.robotconfig"></a>
<a id="tocsent.robotconfig"></a>

```json
{
  "created_at": "string",
  "edges": {
    "owner": {
      "created_at": "string",
      "description": "string",
      "edges": {
        "config": {
          "created_at": "string",
          "edges": {},
          "id": 0,
          "openai_config": {
            "model": "string"
          },
          "openai_content": {
            "chat_with_db": true,
            "index_name": "string",
            "index_namespace": "string"
          },
          "updated_at": "string",
          "welcome": [
            {
              "ai": "string",
              "id": 0
            }
          ]
        },
        "files": [
          {
            "created_at": "string",
            "edges": {
              "owner": {}
            },
            "id": 0,
            "name": "string",
            "status": "string",
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "edges": {
            "domain": {
              "created_at": "string",
              "domain_id": "string",
              "edges": {
                "owner": {},
                "users": [
                  {
                    "created_at": "string",
                    "edges": {},
                    "email": "string",
                    "id": 0,
                    "nickname": "string",
                    "openid": "string",
                    "password": "string",
                    "unionid": "string",
                    "updated_at": "string",
                    "user_type": "string"
                  }
                ]
              },
              "id": 0,
              "name": "string",
              "updated_at": "string"
            },
            "robots": [
              {}
            ]
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string",
          "updated_at": "string"
        }
      },
      "id": 0,
      "name": "string",
      "prompt": "string",
      "share": "string",
      "updated_at": "string"
    }
  },
  "id": 0,
  "openai_config": {
    "model": "string"
  },
  "openai_content": {
    "chat_with_db": true,
    "index_name": "string",
    "index_namespace": "string"
  },
  "updated_at": "string",
  "welcome": [
    {
      "ai": "string",
      "id": 0
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_at|string|false|none|CreatedAt holds the value of the "created_at" field.|
|edges|[ent.RobotConfigEdges](#schemaent.robotconfigedges)|false|none|none|
|id|integer|false|none|ID of the ent.|
|openai_config|[schema.OpenAIConfig](#schemaschema.openaiconfig)|false|none|none|
|openai_content|[schema.OpenAIContent](#schemaschema.openaicontent)|false|none|none|
|updated_at|string|false|none|UpdatedAt holds the value of the "updated_at" field.|
|welcome|[[schema.WelcomeMessage](#schemaschema.welcomemessage)]|false|none|Welcome holds the value of the "welcome" field.|

<h2 id="tocS_ent.RobotConfigEdges">ent.RobotConfigEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.robotconfigedges"></a>
<a id="schema_ent.RobotConfigEdges"></a>
<a id="tocSent.robotconfigedges"></a>
<a id="tocsent.robotconfigedges"></a>

```json
{
  "owner": {
    "created_at": "string",
    "description": "string",
    "edges": {
      "config": {
        "created_at": "string",
        "edges": {
          "owner": {}
        },
        "id": 0,
        "openai_config": {
          "model": "string"
        },
        "openai_content": {
          "chat_with_db": true,
          "index_name": "string",
          "index_namespace": "string"
        },
        "updated_at": "string",
        "welcome": [
          {
            "ai": "string",
            "id": 0
          }
        ]
      },
      "files": [
        {
          "created_at": "string",
          "edges": {
            "owner": {}
          },
          "id": 0,
          "name": "string",
          "status": "string",
          "updated_at": "string"
        }
      ],
      "owner": {
        "created_at": "string",
        "edges": {
          "domain": {
            "created_at": "string",
            "domain_id": "string",
            "edges": {
              "owner": {},
              "users": [
                {
                  "created_at": "string",
                  "edges": {
                    "chats": [],
                    "owner": {}
                  },
                  "email": "string",
                  "id": 0,
                  "nickname": "string",
                  "openid": "string",
                  "password": "string",
                  "unionid": "string",
                  "updated_at": "string",
                  "user_type": "string"
                }
              ]
            },
            "id": 0,
            "name": "string",
            "updated_at": "string"
          },
          "robots": [
            {}
          ]
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "password": "string",
        "updated_at": "string"
      }
    },
    "id": 0,
    "name": "string",
    "prompt": "string",
    "share": "string",
    "updated_at": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|owner|[ent.Robot](#schemaent.robot)|false|none|none|

<h2 id="tocS_ent.RobotEdges">ent.RobotEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.robotedges"></a>
<a id="schema_ent.RobotEdges"></a>
<a id="tocSent.robotedges"></a>
<a id="tocsent.robotedges"></a>

```json
{
  "config": {
    "created_at": "string",
    "edges": {
      "owner": {
        "created_at": "string",
        "description": "string",
        "edges": {
          "config": {},
          "files": [
            {
              "created_at": "string",
              "edges": {
                "owner": {}
              },
              "id": 0,
              "name": "string",
              "status": "string",
              "updated_at": "string"
            }
          ],
          "owner": {
            "created_at": "string",
            "edges": {
              "domain": {
                "created_at": "string",
                "domain_id": "string",
                "edges": {
                  "owner": {},
                  "users": [
                    {}
                  ]
                },
                "id": 0,
                "name": "string",
                "updated_at": "string"
              },
              "robots": [
                {}
              ]
            },
            "email": "string",
            "id": 0,
            "nickname": "string",
            "password": "string",
            "updated_at": "string"
          }
        },
        "id": 0,
        "name": "string",
        "prompt": "string",
        "share": "string",
        "updated_at": "string"
      }
    },
    "id": 0,
    "openai_config": {
      "model": "string"
    },
    "openai_content": {
      "chat_with_db": true,
      "index_name": "string",
      "index_namespace": "string"
    },
    "updated_at": "string",
    "welcome": [
      {
        "ai": "string",
        "id": 0
      }
    ]
  },
  "files": [
    {
      "created_at": "string",
      "edges": {
        "owner": {
          "created_at": "string",
          "description": "string",
          "edges": {
            "config": {
              "created_at": "string",
              "edges": {
                "owner": {}
              },
              "id": 0,
              "openai_config": {
                "model": "string"
              },
              "openai_content": {
                "chat_with_db": true,
                "index_name": "string",
                "index_namespace": "string"
              },
              "updated_at": "string",
              "welcome": [
                {
                  "ai": "string",
                  "id": 0
                }
              ]
            },
            "files": [],
            "owner": {
              "created_at": "string",
              "edges": {
                "domain": {
                  "created_at": "string",
                  "domain_id": "string",
                  "edges": {
                    "owner": {},
                    "users": []
                  },
                  "id": 0,
                  "name": "string",
                  "updated_at": "string"
                },
                "robots": [
                  {}
                ]
              },
              "email": "string",
              "id": 0,
              "nickname": "string",
              "password": "string",
              "updated_at": "string"
            }
          },
          "id": 0,
          "name": "string",
          "prompt": "string",
          "share": "string",
          "updated_at": "string"
        }
      },
      "id": 0,
      "name": "string",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "owner": {
    "created_at": "string",
    "edges": {
      "domain": {
        "created_at": "string",
        "domain_id": "string",
        "edges": {
          "owner": {},
          "users": [
            {
              "created_at": "string",
              "edges": {
                "chats": [
                  {
                    "context_id": "string",
                    "created_at": "string",
                    "edges": {},
                    "id": 0,
                    "messages": [],
                    "robot_id": 0,
                    "updated_at": "string"
                  }
                ],
                "owner": {}
              },
              "email": "string",
              "id": 0,
              "nickname": "string",
              "openid": "string",
              "password": "string",
              "unionid": "string",
              "updated_at": "string",
              "user_type": "string"
            }
          ]
        },
        "id": 0,
        "name": "string",
        "updated_at": "string"
      },
      "robots": [
        {
          "created_at": "string",
          "description": "string",
          "edges": {
            "config": {
              "created_at": "string",
              "edges": {
                "owner": {}
              },
              "id": 0,
              "openai_config": {
                "model": "string"
              },
              "openai_content": {
                "chat_with_db": true,
                "index_name": "string",
                "index_namespace": "string"
              },
              "updated_at": "string",
              "welcome": [
                {
                  "ai": "string",
                  "id": 0
                }
              ]
            },
            "files": [
              {
                "created_at": "string",
                "edges": {
                  "owner": {}
                },
                "id": 0,
                "name": "string",
                "status": "string",
                "updated_at": "string"
              }
            ],
            "owner": {}
          },
          "id": 0,
          "name": "string",
          "prompt": "string",
          "share": "string",
          "updated_at": "string"
        }
      ]
    },
    "email": "string",
    "id": 0,
    "nickname": "string",
    "password": "string",
    "updated_at": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|config|[ent.RobotConfig](#schemaent.robotconfig)|false|none|none|
|files|[[ent.File](#schemaent.file)]|false|none|Files holds the value of the files edge.|
|owner|[ent.User](#schemaent.user)|false|none|none|

<h2 id="tocS_ent.User">ent.User</h2>
<!-- backwards compatibility -->
<a id="schemaent.user"></a>
<a id="schema_ent.User"></a>
<a id="tocSent.user"></a>
<a id="tocsent.user"></a>

```json
{
  "created_at": "string",
  "edges": {
    "domain": {
      "created_at": "string",
      "domain_id": "string",
      "edges": {
        "owner": {
          "created_at": "string",
          "edges": {},
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string",
          "updated_at": "string"
        },
        "users": [
          {
            "created_at": "string",
            "edges": {
              "chats": [
                {
                  "context_id": "string",
                  "created_at": "string",
                  "edges": {
                    "owner": {}
                  },
                  "id": 0,
                  "messages": [
                    {}
                  ],
                  "robot_id": 0,
                  "updated_at": "string"
                }
              ],
              "owner": {}
            },
            "email": "string",
            "id": 0,
            "nickname": "string",
            "openid": "string",
            "password": "string",
            "unionid": "string",
            "updated_at": "string",
            "user_type": "string"
          }
        ]
      },
      "id": 0,
      "name": "string",
      "updated_at": "string"
    },
    "robots": [
      {
        "created_at": "string",
        "description": "string",
        "edges": {
          "config": {
            "created_at": "string",
            "edges": {
              "owner": {}
            },
            "id": 0,
            "openai_config": {
              "model": "string"
            },
            "openai_content": {
              "chat_with_db": true,
              "index_name": "string",
              "index_namespace": "string"
            },
            "updated_at": "string",
            "welcome": [
              {
                "ai": "string",
                "id": 0
              }
            ]
          },
          "files": [
            {
              "created_at": "string",
              "edges": {
                "owner": {}
              },
              "id": 0,
              "name": "string",
              "status": "string",
              "updated_at": "string"
            }
          ],
          "owner": {
            "created_at": "string",
            "edges": {},
            "email": "string",
            "id": 0,
            "nickname": "string",
            "password": "string",
            "updated_at": "string"
          }
        },
        "id": 0,
        "name": "string",
        "prompt": "string",
        "share": "string",
        "updated_at": "string"
      }
    ]
  },
  "email": "string",
  "id": 0,
  "nickname": "string",
  "password": "string",
  "updated_at": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|created_at|string|false|none|CreatedAt holds the value of the "created_at" field.|
|edges|[ent.UserEdges](#schemaent.useredges)|false|none|none|
|email|string|false|none|Email holds the value of the "email" field.|
|id|integer|false|none|ID of the ent.|
|nickname|string|false|none|Nickname holds the value of the "nickname" field.|
|password|string|false|none|Password holds the value of the "password" field.|
|updated_at|string|false|none|UpdatedAt holds the value of the "updated_at" field.|

<h2 id="tocS_ent.UserEdges">ent.UserEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.useredges"></a>
<a id="schema_ent.UserEdges"></a>
<a id="tocSent.useredges"></a>
<a id="tocsent.useredges"></a>

```json
{
  "domain": {
    "created_at": "string",
    "domain_id": "string",
    "edges": {
      "owner": {
        "created_at": "string",
        "edges": {
          "domain": {},
          "robots": [
            {
              "created_at": "string",
              "description": "string",
              "edges": {
                "config": {
                  "created_at": "string",
                  "edges": {
                    "owner": {}
                  },
                  "id": 0,
                  "openai_config": {
                    "model": "string"
                  },
                  "openai_content": {
                    "chat_with_db": true,
                    "index_name": "string",
                    "index_namespace": "string"
                  },
                  "updated_at": "string",
                  "welcome": [
                    {}
                  ]
                },
                "files": [
                  {
                    "created_at": "string",
                    "edges": {},
                    "id": 0,
                    "name": "string",
                    "status": "string",
                    "updated_at": "string"
                  }
                ],
                "owner": {}
              },
              "id": 0,
              "name": "string",
              "prompt": "string",
              "share": "string",
              "updated_at": "string"
            }
          ]
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "password": "string",
        "updated_at": "string"
      },
      "users": [
        {
          "created_at": "string",
          "edges": {
            "chats": [
              {
                "context_id": "string",
                "created_at": "string",
                "edges": {
                  "owner": {}
                },
                "id": 0,
                "messages": [
                  {
                    "content": "string",
                    "created": "string",
                    "role": "string"
                  }
                ],
                "robot_id": 0,
                "updated_at": "string"
              }
            ],
            "owner": {}
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "openid": "string",
          "password": "string",
          "unionid": "string",
          "updated_at": "string",
          "user_type": "string"
        }
      ]
    },
    "id": 0,
    "name": "string",
    "updated_at": "string"
  },
  "robots": [
    {
      "created_at": "string",
      "description": "string",
      "edges": {
        "config": {
          "created_at": "string",
          "edges": {
            "owner": {}
          },
          "id": 0,
          "openai_config": {
            "model": "string"
          },
          "openai_content": {
            "chat_with_db": true,
            "index_name": "string",
            "index_namespace": "string"
          },
          "updated_at": "string",
          "welcome": [
            {
              "ai": "string",
              "id": 0
            }
          ]
        },
        "files": [
          {
            "created_at": "string",
            "edges": {
              "owner": {}
            },
            "id": 0,
            "name": "string",
            "status": "string",
            "updated_at": "string"
          }
        ],
        "owner": {
          "created_at": "string",
          "edges": {
            "domain": {
              "created_at": "string",
              "domain_id": "string",
              "edges": {
                "owner": {},
                "users": [
                  {
                    "created_at": "string",
                    "edges": {},
                    "email": "string",
                    "id": 0,
                    "nickname": "string",
                    "openid": "string",
                    "password": "string",
                    "unionid": "string",
                    "updated_at": "string",
                    "user_type": "string"
                  }
                ]
              },
              "id": 0,
              "name": "string",
              "updated_at": "string"
            },
            "robots": []
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string",
          "updated_at": "string"
        }
      },
      "id": 0,
      "name": "string",
      "prompt": "string",
      "share": "string",
      "updated_at": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|domain|[ent.Domain](#schemaent.domain)|false|none|none|
|robots|[[ent.Robot](#schemaent.robot)]|false|none|Robots holds the value of the robots edge.|

<h2 id="tocS_schema.Message">schema.Message</h2>
<!-- backwards compatibility -->
<a id="schemaschema.message"></a>
<a id="schema_schema.Message"></a>
<a id="tocSschema.message"></a>
<a id="tocsschema.message"></a>

```json
{
  "content": "string",
  "created": "string",
  "role": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|content|string|false|none|none|
|created|string|false|none|none|
|role|string|false|none|none|

<h2 id="tocS_schema.OpenAIConfig">schema.OpenAIConfig</h2>
<!-- backwards compatibility -->
<a id="schemaschema.openaiconfig"></a>
<a id="schema_schema.OpenAIConfig"></a>
<a id="tocSschema.openaiconfig"></a>
<a id="tocsschema.openaiconfig"></a>

```json
{
  "model": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|model|string|false|none|none|

<h2 id="tocS_schema.OpenAIContent">schema.OpenAIContent</h2>
<!-- backwards compatibility -->
<a id="schemaschema.openaicontent"></a>
<a id="schema_schema.OpenAIContent"></a>
<a id="tocSschema.openaicontent"></a>
<a id="tocsschema.openaicontent"></a>

```json
{
  "chat_with_db": true,
  "index_name": "string",
  "index_namespace": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|chat_with_db|boolean|false|none|none|
|index_name|string|false|none|none|
|index_namespace|string|false|none|none|

<h2 id="tocS_schema.WelcomeMessage">schema.WelcomeMessage</h2>
<!-- backwards compatibility -->
<a id="schemaschema.welcomemessage"></a>
<a id="schema_schema.WelcomeMessage"></a>
<a id="tocSschema.welcomemessage"></a>
<a id="tocsschema.welcomemessage"></a>

```json
{
  "ai": "string",
  "id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|ai|string|false|none|none|
|id|integer|false|none|none|

