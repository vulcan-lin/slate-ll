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

* <a href="http://https://test-api.learnbyuse.app/api/v1">http://https://test-api.learnbyuse.app/api/v1</a>

<h1 id="learnbyuse-api-group">Group</h1>

## get__groups

> Code samples

```shell
# You can also use wget
curl -X GET http://https:/test-api.learnbyuse.app/api/v1/groups \
  -H 'Accept: application/json'

```

```http
GET http://https:/test-api.learnbyuse.app/api/v1/groups HTTP/1.1
Host: https
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/groups',
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

result = RestClient.get 'http://https:/test-api.learnbyuse.app/api/v1/groups',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://https:/test-api.learnbyuse.app/api/v1/groups', headers = headers)

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
    $response = $client->request('GET','http://https:/test-api.learnbyuse.app/api/v1/groups', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/groups");
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
    req, err := http.NewRequest("GET", "http://https:/test-api.learnbyuse.app/api/v1/groups", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /groups`

查询分组列表

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__groups-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## post__groups

> Code samples

```shell
# You can also use wget
curl -X POST http://https:/test-api.learnbyuse.app/api/v1/groups \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://https:/test-api.learnbyuse.app/api/v1/groups HTTP/1.1
Host: https
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "name": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/groups',
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

result = RestClient.post 'http://https:/test-api.learnbyuse.app/api/v1/groups',
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

r = requests.post('http://https:/test-api.learnbyuse.app/api/v1/groups', headers = headers)

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
    $response = $client->request('POST','http://https:/test-api.learnbyuse.app/api/v1/groups', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/groups");
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
    req, err := http.NewRequest("POST", "http://https:/test-api.learnbyuse.app/api/v1/groups", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /groups`

创建分组

> Body parameter

```json
{
  "name": "string"
}
```

<h3 id="post__groups-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[GroupCreateReq](#schemagroupcreatereq)|true|group create|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__groups-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## get__groups_{group_id}

> Code samples

```shell
# You can also use wget
curl -X GET http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id} \
  -H 'Accept: application/json'

```

```http
GET http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id} HTTP/1.1
Host: https
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}',
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

result = RestClient.get 'http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}', headers = headers)

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
    $response = $client->request('GET','http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}");
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
    req, err := http.NewRequest("GET", "http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /groups/{group_id}`

查询分组信息

<h3 id="get__groups_{group_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|group_id|path|integer|true|group id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "count": 0,
    "group_id": 0,
    "group_name": "string"
  },
  "msg": "string"
}
```

<h3 id="get__groups_{group_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[GetGroupResp](#schemagetgroupresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## delete__groups_{group_id}

> Code samples

```shell
# You can also use wget
curl -X DELETE http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id} \
  -H 'Accept: application/json'

```

```http
DELETE http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id} HTTP/1.1
Host: https
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}',
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
  'Accept' => 'application/json'
}

result = RestClient.delete 'http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}', headers = headers)

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
    $response = $client->request('DELETE','http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}");
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
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /groups/{group_id}`

删除分组

<h3 id="delete__groups_{group_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|group_id|path|integer|true|group id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="delete__groups_{group_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## get__groups_{group_id}_cards

> Code samples

```shell
# You can also use wget
curl -X GET http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards \
  -H 'Accept: application/json'

```

```http
GET http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards HTTP/1.1
Host: https
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards',
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

result = RestClient.get 'http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards', headers = headers)

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
    $response = $client->request('GET','http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards");
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
    req, err := http.NewRequest("GET", "http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /groups/{group_id}/cards`

查询分组下的卡片列表

<h3 id="get__groups_{group_id}_cards-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|group_id|path|integer|true|group id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "answer": "string",
      "card_id": 0,
      "phrase_id": "string",
      "phrase_text": "string",
      "video-url": "string"
    }
  ],
  "msg": "string"
}
```

<h3 id="get__groups_{group_id}_cards-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[CardListResp](#schemacardlistresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## post__groups_{group_id}_cards

> Code samples

```shell
# You can also use wget
curl -X POST http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards HTTP/1.1
Host: https
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "answer": "string",
  "phrase_id": "string",
  "phrase_text": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards',
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

result = RestClient.post 'http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards',
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

r = requests.post('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards', headers = headers)

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
    $response = $client->request('POST','http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards");
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
    req, err := http.NewRequest("POST", "http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /groups/{group_id}/cards`

创建分组所属卡片

> Body parameter

```json
{
  "answer": "string",
  "phrase_id": "string",
  "phrase_text": "string"
}
```

<h3 id="post__groups_{group_id}_cards-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|group_id|path|integer|true|group id|
|body|body|[api_service.UserRegisterReq](#schemaapi_service.userregisterreq)|true|card create|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "answer": "string",
    "card_id": 0,
    "phrase_id": "string",
    "phrase_text": "string",
    "video-url": "string"
  },
  "msg": "string"
}
```

<h3 id="post__groups_{group_id}_cards-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[CardCreateResp](#schemacardcreateresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## delete__groups_{group_id}_cards_{card_id}

> Code samples

```shell
# You can also use wget
curl -X DELETE http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards/{card_id} \
  -H 'Accept: application/json'

```

```http
DELETE http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards/{card_id} HTTP/1.1
Host: https
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards/{card_id}',
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
  'Accept' => 'application/json'
}

result = RestClient.delete 'http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards/{card_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.delete('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards/{card_id}', headers = headers)

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
    $response = $client->request('DELETE','http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards/{card_id}', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards/{card_id}");
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
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("DELETE", "http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/cards/{card_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /groups/{group_id}/cards/{card_id}`

删除分组下的卡片

<h3 id="delete__groups_{group_id}_cards_{card_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|group_id|path|integer|true|group id|
|card_id|path|integer|true|card id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="delete__groups_{group_id}_cards_{card_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

<h1 id="learnbyuse-api-learn">Learn</h1>

## get__groups_{group_id}_learn

> Code samples

```shell
# You can also use wget
curl -X GET http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn \
  -H 'Accept: application/json'

```

```http
GET http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn HTTP/1.1
Host: https
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn',
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

result = RestClient.get 'http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn', headers = headers)

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
    $response = $client->request('GET','http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn");
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
    req, err := http.NewRequest("GET", "http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /groups/{group_id}/learn`

[闪记卡片]获取本次推荐学习卡片列表

<h3 id="get__groups_{group_id}_learn-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|group_id|path|integer|true|group id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "answer": "string",
      "card_id": 0,
      "phrase_id": "string",
      "phrase_text": "string",
      "video-url": "string"
    }
  ],
  "msg": "string"
}
```

<h3 id="get__groups_{group_id}_learn-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|LearnGroupCardsResp|[LearnGroupCardsResp](#schemalearngroupcardsresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## post__groups_{group_id}_learn

> Code samples

```shell
# You can also use wget
curl -X POST http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn?card_id=0&review_score=string \
  -H 'Accept: application/json'

```

```http
POST http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn?card_id=0&review_score=string HTTP/1.1
Host: https
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn?card_id=0&review_score=string',
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

result = RestClient.post 'http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn',
  params: {
  'card_id' => 'integer',
'review_score' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.post('http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn', params={
  'card_id': '0',  'review_score': 'string'
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
    $response = $client->request('POST','http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn?card_id=0&review_score=string");
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
    req, err := http.NewRequest("POST", "http://https:/test-api.learnbyuse.app/api/v1/groups/{group_id}/learn", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /groups/{group_id}/learn`

[闪记卡片]卡片打分

<h3 id="post__groups_{group_id}_learn-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|card_id|query|integer|true|card id|
|review_score|query|string|true|review score 枚举:[again, hard, good, easy]|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "answer": "string",
    "card_id": 0,
    "phrase_id": "string",
    "phrase_text": "string",
    "video-url": "string"
  },
  "msg": "string"
}
```

<h3 id="post__groups_{group_id}_learn-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[RatingCardsResp](#schemaratingcardsresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

<h1 id="learnbyuse-api-phrase">Phrase</h1>

## get__phrases_search

> Code samples

```shell
# You can also use wget
curl -X GET http://https:/test-api.learnbyuse.app/api/v1/phrases/search?phrase=string \
  -H 'Accept: application/json'

```

```http
GET http://https:/test-api.learnbyuse.app/api/v1/phrases/search?phrase=string HTTP/1.1
Host: https
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/phrases/search?phrase=string',
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

result = RestClient.get 'http://https:/test-api.learnbyuse.app/api/v1/phrases/search',
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

r = requests.get('http://https:/test-api.learnbyuse.app/api/v1/phrases/search', params={
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
    $response = $client->request('GET','http://https:/test-api.learnbyuse.app/api/v1/phrases/search', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/phrases/search?phrase=string");
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
    req, err := http.NewRequest("GET", "http://https:/test-api.learnbyuse.app/api/v1/phrases/search", data)
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
 
</aside>

<h1 id="learnbyuse-api-user">User</h1>

## post__user_login

> Code samples

```shell
# You can also use wget
curl -X POST http://https:/test-api.learnbyuse.app/api/v1/user/login \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://https:/test-api.learnbyuse.app/api/v1/user/login HTTP/1.1
Host: https
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

fetch('http://https:/test-api.learnbyuse.app/api/v1/user/login',
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

result = RestClient.post 'http://https:/test-api.learnbyuse.app/api/v1/user/login',
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

r = requests.post('http://https:/test-api.learnbyuse.app/api/v1/user/login', headers = headers)

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
    $response = $client->request('POST','http://https:/test-api.learnbyuse.app/api/v1/user/login', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/user/login");
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
    req, err := http.NewRequest("POST", "http://https:/test-api.learnbyuse.app/api/v1/user/login", data)
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
    "token": "string"
  },
  "msg": "string"
}
```

<h3 id="post__user_login-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Login response|[LoginResponse](#schemaloginresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## post__user_register

> Code samples

```shell
# You can also use wget
curl -X POST http://https:/test-api.learnbyuse.app/api/v1/user/register \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://https:/test-api.learnbyuse.app/api/v1/user/register HTTP/1.1
Host: https
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "answer": "string",
  "phrase_id": "string",
  "phrase_text": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/user/register',
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

result = RestClient.post 'http://https:/test-api.learnbyuse.app/api/v1/user/register',
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

r = requests.post('http://https:/test-api.learnbyuse.app/api/v1/user/register', headers = headers)

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
    $response = $client->request('POST','http://https:/test-api.learnbyuse.app/api/v1/user/register', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/user/register");
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
    req, err := http.NewRequest("POST", "http://https:/test-api.learnbyuse.app/api/v1/user/register", data)
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
  "answer": "string",
  "phrase_id": "string",
  "phrase_text": "string"
}
```

<h3 id="post__user_register-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|[api_service.UserRegisterReq](#schemaapi_service.userregisterreq)|true|user register|

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
 
</aside>

<h1 id="learnbyuse-api-videos">Videos</h1>

## get__videos_{fid}

> Code samples

```shell
# You can also use wget
curl -X GET http://https:/test-api.learnbyuse.app/api/v1/videos/{fid} \
  -H 'Accept: application/json'

```

```http
GET http://https:/test-api.learnbyuse.app/api/v1/videos/{fid} HTTP/1.1
Host: https
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://https:/test-api.learnbyuse.app/api/v1/videos/{fid}',
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

result = RestClient.get 'http://https:/test-api.learnbyuse.app/api/v1/videos/{fid}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://https:/test-api.learnbyuse.app/api/v1/videos/{fid}', headers = headers)

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
    $response = $client->request('GET','http://https:/test-api.learnbyuse.app/api/v1/videos/{fid}', array(
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
URL obj = new URL("http://https:/test-api.learnbyuse.app/api/v1/videos/{fid}");
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
    req, err := http.NewRequest("GET", "http://https:/test-api.learnbyuse.app/api/v1/videos/{fid}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /videos/{fid}`

download a video

<h3 id="get__videos_{fid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|fid|path|string|true|file id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__videos_{fid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

# Schemas

<h2 id="tocS_CardCreateResp">CardCreateResp</h2>

<a id="schemacardcreateresp"></a>
<a id="schema_CardCreateResp"></a>
<a id="tocScardcreateresp"></a>
<a id="tocscardcreateresp"></a>

```json
{
  "code": 0,
  "data": {
    "answer": "string",
    "card_id": 0,
    "phrase_id": "string",
    "phrase_text": "string",
    "video-url": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[CardItem](#schemacarditem)|false|none|卡片|
|msg|string|false|none|none|

<h2 id="tocS_CardItem">CardItem</h2>

<a id="schemacarditem"></a>
<a id="schema_CardItem"></a>
<a id="tocScarditem"></a>
<a id="tocscarditem"></a>

```json
{
  "answer": "string",
  "card_id": 0,
  "phrase_id": "string",
  "phrase_text": "string",
  "video-url": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|answer|string|false|none|短语答案|
|card_id|integer|false|none|卡片ID|
|phrase_id|string|false|none|短语ID, 从search phrase继承而来|
|phrase_text|string|false|none|短语文本|
|video-url|string|false|none|视频片段下载地址|

<h2 id="tocS_CardListResp">CardListResp</h2>

<a id="schemacardlistresp"></a>
<a id="schema_CardListResp"></a>
<a id="tocScardlistresp"></a>
<a id="tocscardlistresp"></a>

```json
{
  "code": 0,
  "data": [
    {
      "answer": "string",
      "card_id": 0,
      "phrase_id": "string",
      "phrase_text": "string",
      "video-url": "string"
    }
  ],
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[[CardItem](#schemacarditem)]|false|none|分组所属卡片列表|
|msg|string|false|none|none|

<h2 id="tocS_GetGroupResp">GetGroupResp</h2>

<a id="schemagetgroupresp"></a>
<a id="schema_GetGroupResp"></a>
<a id="tocSgetgroupresp"></a>
<a id="tocsgetgroupresp"></a>

```json
{
  "code": 0,
  "data": {
    "count": 0,
    "group_id": 0,
    "group_name": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[GroupItem](#schemagroupitem)|false|none|分组|
|msg|string|false|none|none|

<h2 id="tocS_GroupCreateReq">GroupCreateReq</h2>

<a id="schemagroupcreatereq"></a>
<a id="schema_GroupCreateReq"></a>
<a id="tocSgroupcreatereq"></a>
<a id="tocsgroupcreatereq"></a>

```json
{
  "name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|true|none|分组名称|

<h2 id="tocS_GroupItem">GroupItem</h2>

<a id="schemagroupitem"></a>
<a id="schema_GroupItem"></a>
<a id="tocSgroupitem"></a>
<a id="tocsgroupitem"></a>

```json
{
  "count": 0,
  "group_id": 0,
  "group_name": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|count|integer|false|none|数量|
|group_id|integer|true|none|分组ID|
|group_name|string|true|none|分组名称|

<h2 id="tocS_LearnGroupCardsResp">LearnGroupCardsResp</h2>

<a id="schemalearngroupcardsresp"></a>
<a id="schema_LearnGroupCardsResp"></a>
<a id="tocSlearngroupcardsresp"></a>
<a id="tocslearngroupcardsresp"></a>

```json
{
  "code": 0,
  "data": [
    {
      "answer": "string",
      "card_id": 0,
      "phrase_id": "string",
      "phrase_text": "string",
      "video-url": "string"
    }
  ],
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[[CardItem](#schemacarditem)]|false|none|本次推荐学习的卡片列表|
|msg|string|false|none|none|

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
|email|string|true|none|用户email地址|
|password|string|true|none|用户密码|

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
|token|string|false|none|用户token|

<h2 id="tocS_LoginResponse">LoginResponse</h2>

<a id="schemaloginresponse"></a>
<a id="schema_LoginResponse"></a>
<a id="tocSloginresponse"></a>
<a id="tocsloginresponse"></a>

```json
{
  "code": 0,
  "data": {
    "token": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[LoginResp](#schemaloginresp)|false|none|none|
|msg|string|false|none|none|

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

<h2 id="tocS_RatingCardsResp">RatingCardsResp</h2>

<a id="schemaratingcardsresp"></a>
<a id="schema_RatingCardsResp"></a>
<a id="tocSratingcardsresp"></a>
<a id="tocsratingcardsresp"></a>

```json
{
  "code": 0,
  "data": {
    "answer": "string",
    "card_id": 0,
    "phrase_id": "string",
    "phrase_text": "string",
    "video-url": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[CardItem](#schemacarditem)|false|none|下一张卡片|
|msg|string|false|none|none|

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

<h2 id="tocS_api_service.UserRegisterReq">api_service.UserRegisterReq</h2>

<a id="schemaapi_service.userregisterreq"></a>
<a id="schema_api_service.UserRegisterReq"></a>
<a id="tocSapi_service.userregisterreq"></a>
<a id="tocsapi_service.userregisterreq"></a>

```json
{
  "answer": "string",
  "phrase_id": "string",
  "phrase_text": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|answer|string|true|none|短语答案|
|phrase_id|string|true|none|短语ID, 从search phrase继承而来|
|phrase_text|string|true|none|短语文本|

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

