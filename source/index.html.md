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
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0
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
  "data": {
    "context_id": "string",
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0
  },
  "msg": "string"
}
```

<h3 id="get__robots-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|RobotListResponse response|[api_service.LoginResponse](#schemaapi_service.loginresponse)|
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
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0
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
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0
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
  "email": "string",
  "nick_name": "string",
  "token": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|true|none|用户email地址|
|nick_name|string|true|none|用户昵称|
|token|string|false|none|用户token|

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
    "id": 0,
    "messages": [
      {
        "content": "string",
        "created": "string",
        "role": "string"
      }
    ],
    "robot_id": 0
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
  "id": 0,
  "messages": [
    {
      "content": "string",
      "created": "string",
      "role": "string"
    }
  ],
  "robot_id": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|context_id|string|false|none|ContextID holds the value of the "context_id" field.|
|id|integer|false|none|ID of the ent.|
|messages|[[schema.Message](#schemaschema.message)]|false|none|Messages holds the value of the "messages" field.|
|robot_id|integer|false|none|RobotID holds the value of the "robot_id" field.|

<h2 id="tocS_ent.File">ent.File</h2>
<!-- backwards compatibility -->
<a id="schemaent.file"></a>
<a id="schema_ent.File"></a>
<a id="tocSent.file"></a>
<a id="tocsent.file"></a>

```json
{
  "edges": {
    "owner": {
      "description": "string",
      "edges": {
        "files": [
          {
            "edges": {},
            "id": 0,
            "name": "string",
            "status": "string"
          }
        ],
        "owner": {
          "edges": {
            "robots": [
              {}
            ]
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string"
        }
      },
      "id": 0,
      "name": "string",
      "prompt": "string",
      "share": "string"
    }
  },
  "id": 0,
  "name": "string",
  "status": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|edges|[ent.FileEdges](#schemaent.fileedges)|false|none|none|
|id|integer|false|none|ID of the ent.|
|name|string|false|none|Name holds the value of the "name" field.|
|status|string|false|none|Status holds the value of the "status" field.|

<h2 id="tocS_ent.FileEdges">ent.FileEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.fileedges"></a>
<a id="schema_ent.FileEdges"></a>
<a id="tocSent.fileedges"></a>
<a id="tocsent.fileedges"></a>

```json
{
  "owner": {
    "description": "string",
    "edges": {
      "files": [
        {
          "edges": {
            "owner": {}
          },
          "id": 0,
          "name": "string",
          "status": "string"
        }
      ],
      "owner": {
        "edges": {
          "robots": [
            {}
          ]
        },
        "email": "string",
        "id": 0,
        "nickname": "string",
        "password": "string"
      }
    },
    "id": 0,
    "name": "string",
    "prompt": "string",
    "share": "string"
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
  "description": "string",
  "edges": {
    "files": [
      {
        "edges": {
          "owner": {
            "description": "string",
            "edges": {},
            "id": 0,
            "name": "string",
            "prompt": "string",
            "share": "string"
          }
        },
        "id": 0,
        "name": "string",
        "status": "string"
      }
    ],
    "owner": {
      "edges": {
        "robots": [
          {
            "description": "string",
            "edges": {},
            "id": 0,
            "name": "string",
            "prompt": "string",
            "share": "string"
          }
        ]
      },
      "email": "string",
      "id": 0,
      "nickname": "string",
      "password": "string"
    }
  },
  "id": 0,
  "name": "string",
  "prompt": "string",
  "share": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|description|string|false|none|Description holds the value of the "description" field.|
|edges|[ent.RobotEdges](#schemaent.robotedges)|false|none|none|
|id|integer|false|none|ID of the ent.|
|name|string|false|none|Name holds the value of the "name" field.|
|prompt|string|false|none|Prompt holds the value of the "prompt" field.|
|share|string|false|none|Share holds the value of the "share" field.|

<h2 id="tocS_ent.RobotEdges">ent.RobotEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.robotedges"></a>
<a id="schema_ent.RobotEdges"></a>
<a id="tocSent.robotedges"></a>
<a id="tocsent.robotedges"></a>

```json
{
  "files": [
    {
      "edges": {
        "owner": {
          "description": "string",
          "edges": {
            "files": [],
            "owner": {
              "edges": {
                "robots": [
                  {}
                ]
              },
              "email": "string",
              "id": 0,
              "nickname": "string",
              "password": "string"
            }
          },
          "id": 0,
          "name": "string",
          "prompt": "string",
          "share": "string"
        }
      },
      "id": 0,
      "name": "string",
      "status": "string"
    }
  ],
  "owner": {
    "edges": {
      "robots": [
        {
          "description": "string",
          "edges": {
            "files": [
              {
                "edges": {
                  "owner": {}
                },
                "id": 0,
                "name": "string",
                "status": "string"
              }
            ],
            "owner": {}
          },
          "id": 0,
          "name": "string",
          "prompt": "string",
          "share": "string"
        }
      ]
    },
    "email": "string",
    "id": 0,
    "nickname": "string",
    "password": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
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
  "edges": {
    "robots": [
      {
        "description": "string",
        "edges": {
          "files": [
            {
              "edges": {
                "owner": {}
              },
              "id": 0,
              "name": "string",
              "status": "string"
            }
          ],
          "owner": {
            "edges": {},
            "email": "string",
            "id": 0,
            "nickname": "string",
            "password": "string"
          }
        },
        "id": 0,
        "name": "string",
        "prompt": "string",
        "share": "string"
      }
    ]
  },
  "email": "string",
  "id": 0,
  "nickname": "string",
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|edges|[ent.UserEdges](#schemaent.useredges)|false|none|none|
|email|string|false|none|Email holds the value of the "email" field.|
|id|integer|false|none|ID of the ent.|
|nickname|string|false|none|Nickname holds the value of the "nickname" field.|
|password|string|false|none|Password holds the value of the "password" field.|

<h2 id="tocS_ent.UserEdges">ent.UserEdges</h2>
<!-- backwards compatibility -->
<a id="schemaent.useredges"></a>
<a id="schema_ent.UserEdges"></a>
<a id="tocSent.useredges"></a>
<a id="tocsent.useredges"></a>

```json
{
  "robots": [
    {
      "description": "string",
      "edges": {
        "files": [
          {
            "edges": {
              "owner": {}
            },
            "id": 0,
            "name": "string",
            "status": "string"
          }
        ],
        "owner": {
          "edges": {
            "robots": []
          },
          "email": "string",
          "id": 0,
          "nickname": "string",
          "password": "string"
        }
      },
      "id": 0,
      "name": "string",
      "prompt": "string",
      "share": "string"
    }
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
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

