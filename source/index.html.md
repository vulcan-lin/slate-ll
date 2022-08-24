---
title: LearnByUse API v1
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

<h1 id="learnbyuse-api">LearnByUse API v1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Welcome to the LearnByUse  API! You can use our API to access LearnByUse  API endpoints.

Base URLs:

* <a href="http://68.183.232.22:4928/api/v1">http://68.183.232.22:4928/api/v1</a>

<h1 id="learnbyuse-api-phrase">Phrase</h1>

## get__phrases_search

> Code samples

```shell
# You can also use wget
curl -X GET http://68.183.232.22:4928/api/v1/phrases/search?phrase=string \
  -H 'Accept: application/json'

```

```http
GET http://68.183.232.22:4928/api/v1/phrases/search?phrase=string HTTP/1.1
Host: 68.183.232.22:4928
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://68.183.232.22:4928/api/v1/phrases/search?phrase=string',
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

result = RestClient.get 'http://68.183.232.22:4928/api/v1/phrases/search',
  params: {
  'phrase' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://68.183.232.22:4928/api/v1/phrases/search', params={
  'phrase': 'string'
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
    $response = $client->request('GET','http://68.183.232.22:4928/api/v1/phrases/search', array(
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
URL obj = new URL("http://68.183.232.22:4928/api/v1/phrases/search?phrase=string");
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
    req, err := http.NewRequest("GET", "http://68.183.232.22:4928/api/v1/phrases/search", data)
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
|phrase|query|string|true|Phrase|
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
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Clips item|[SearchPhraseResp](#schemasearchphraseresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="learnbyuse-api-authorization">Authorization</h1>

## post__user_login

> Code samples

```shell
# You can also use wget
curl -X POST http://68.183.232.22:4928/api/v1/user/login \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://68.183.232.22:4928/api/v1/user/login HTTP/1.1
Host: 68.183.232.22:4928
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

fetch('http://68.183.232.22:4928/api/v1/user/login',
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

result = RestClient.post 'http://68.183.232.22:4928/api/v1/user/login',
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

r = requests.post('http://68.183.232.22:4928/api/v1/user/login', headers = headers)

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
    $response = $client->request('POST','http://68.183.232.22:4928/api/v1/user/login', array(
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
URL obj = new URL("http://68.183.232.22:4928/api/v1/user/login");
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
    req, err := http.NewRequest("POST", "http://68.183.232.22:4928/api/v1/user/login", data)
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
  "token": "string"
}
```

<h3 id="post__user_login-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[LoginResp](#schemaloginresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__user_register

> Code samples

```shell
# You can also use wget
curl -X POST http://68.183.232.22:4928/api/v1/user/register \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://68.183.232.22:4928/api/v1/user/register HTTP/1.1
Host: 68.183.232.22:4928
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

fetch('http://68.183.232.22:4928/api/v1/user/register',
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

result = RestClient.post 'http://68.183.232.22:4928/api/v1/user/register',
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

r = requests.post('http://68.183.232.22:4928/api/v1/user/register', headers = headers)

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
    $response = $client->request('POST','http://68.183.232.22:4928/api/v1/user/register', array(
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
URL obj = new URL("http://68.183.232.22:4928/api/v1/user/register");
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
    req, err := http.NewRequest("POST", "http://68.183.232.22:4928/api/v1/user/register", data)
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
  "token": "string"
}
```

<h3 id="post__user_register-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[LoginResp](#schemaloginresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_LoginReq">LoginReq</h2>

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
|email|string|true|none|none|
|password|string|true|none|none|

<h2 id="tocS_LoginResp">LoginResp</h2>

<a id="schemaloginresp"></a>
<a id="schema_LoginResp"></a>
<a id="tocSloginresp"></a>
<a id="tocsloginresp"></a>

```json
{
  "token": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|token|string|false|none|none|

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
|id|string|false|none|视频片段id|
|movie|string|false|none|所属电影ID|
|start|number|false|none|视频片段在电影中的开始时间|
|text|string|false|none|字幕文本|
|video-info|[VideoInfo](#schemavideoinfo)|false|none|电影信息|
|video-url|string|false|none|视频片段下载地址|

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
|count|integer|false|none|短语搜索结果数量|
|phrases|[[Phrase](#schemaphrase)]|false|none|视频片段数组|

<h2 id="tocS_SearchPhraseResp">SearchPhraseResp</h2>

<a id="schemasearchphraseresp"></a>
<a id="schema_SearchPhraseResp"></a>
<a id="tocSsearchphraseresp"></a>
<a id="tocssearchphraseresp"></a>

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
|data|[Phrases](#schemaphrases)|false|none|none|
|msg|string|false|none|none|
|pagination|[Pagination](#schemapagination)|false|none|分页|

<h2 id="tocS_UserRegisterReq">UserRegisterReq</h2>

<a id="schemauserregisterreq"></a>
<a id="schema_UserRegisterReq"></a>
<a id="tocSuserregisterreq"></a>
<a id="tocsuserregisterreq"></a>

```json
{
  "email": "string",
  "password": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|true|none|none|
|password|string|true|none|none|

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
|imdb|string|false|none|imdb id|
|string|string|false|none|电影名称|

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
