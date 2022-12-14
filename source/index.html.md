---
title: LearnByUse API v2
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

<h1 id="learnbyuse-api">LearnByUse API v2</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Welcome to the LearnByUse  API! You can use our API to access LearnByUse  API endpoints.

Base URLs:

* <a href="https://test-api.learnbyuse.app/api/v2">https://test-api.learnbyuse.app/api/v2</a>

<h1 id="learnbyuse-api-book">Book</h1>

## get__books

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/books \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET https://test-api.learnbyuse.app/api/v2/books HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/books',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/books',
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

r = requests.get('https://test-api.learnbyuse.app/api/v2/books', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/books', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/books");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/books", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /books`

????????????book??????

<h3 id="get__books-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "author": "string",
      "format": "string",
      "id": 0,
      "name": "string",
      "status": "string",
      "uri": "string"
    }
  ],
  "msg": "string"
}
```

<h3 id="get__books-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|ListBooksResp|[ListBookResp](#schemalistbookresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__books_download_{book_id}

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/books/download/{book_id} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET https://test-api.learnbyuse.app/api/v2/books/download/{book_id} HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/books/download/{book_id}',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/books/download/{book_id}',
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

r = requests.get('https://test-api.learnbyuse.app/api/v2/books/download/{book_id}', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/books/download/{book_id}', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/books/download/{book_id}");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/books/download/{book_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /books/download/{book_id}`

download book

<h3 id="get__books_download_{book_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|book_id|path|integer|true|book id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__books_download_{book_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__books_upload

> Code samples

```shell
# You can also use wget
curl -X POST https://test-api.learnbyuse.app/api/v2/books/upload \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST https://test-api.learnbyuse.app/api/v2/books/upload HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/books/upload',
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
  'Accept' => 'application/json',
  'Authorization' => 'string'
}

result = RestClient.post 'https://test-api.learnbyuse.app/api/v2/books/upload',
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

r = requests.post('https://test-api.learnbyuse.app/api/v2/books/upload', headers = headers)

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
    $response = $client->request('POST','https://test-api.learnbyuse.app/api/v2/books/upload', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/books/upload");
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
        "Authorization": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test-api.learnbyuse.app/api/v2/books/upload", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /books/upload`

??????txt pdf/mobi book

<h3 id="post__books_upload-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__books_upload-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__books_{book_id}

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/books/{book_id} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET https://test-api.learnbyuse.app/api/v2/books/{book_id} HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/books/{book_id}',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/books/{book_id}',
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

r = requests.get('https://test-api.learnbyuse.app/api/v2/books/{book_id}', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/books/{book_id}', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/books/{book_id}");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/books/{book_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /books/{book_id}`

Get book item

<h3 id="get__books_{book_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|book_id|path|integer|true|book id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "author": "string",
    "format": "string",
    "id": 0,
    "name": "string",
    "status": "string",
    "uri": "string"
  },
  "msg": "string"
}
```

<h3 id="get__books_{book_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GetBooksResp response|[GetBookResp](#schemagetbookresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__books_{book_id}_cards

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/books/{book_id}/cards \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET https://test-api.learnbyuse.app/api/v2/books/{book_id}/cards HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/books/{book_id}/cards',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/books/{book_id}/cards',
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

r = requests.get('https://test-api.learnbyuse.app/api/v2/books/{book_id}/cards', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/books/{book_id}/cards', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/books/{book_id}/cards");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/books/{book_id}/cards", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /books/{book_id}/cards`

??????Book??????????????????

<h3 id="get__books_{book_id}_cards-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|book_id|path|integer|true|book id|
|page_current|query|integer|false|current page index, ???1??????|
|page_size|query|integer|false|size of page, ?????????: 15|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "answer": "string",
      "card_id": 0,
      "frq": 0,
      "learn_times": 0,
      "proficiency": 0,
      "question": "string",
      "tips": "string"
    }
  ],
  "msg": "string",
  "pagination": {
    "current": 0,
    "size": 0,
    "total": 0
  }
}
```

<h3 id="get__books_{book_id}_cards-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[CardListResp](#schemacardlistresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__books_{book_id}_exercise

> Code samples

```shell
# You can also use wget
curl -X POST https://test-api.learnbyuse.app/api/v2/books/{book_id}/exercise \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST https://test-api.learnbyuse.app/api/v2/books/{book_id}/exercise HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/books/{book_id}/exercise',
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
  'Accept' => 'application/json',
  'Authorization' => 'string'
}

result = RestClient.post 'https://test-api.learnbyuse.app/api/v2/books/{book_id}/exercise',
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

r = requests.post('https://test-api.learnbyuse.app/api/v2/books/{book_id}/exercise', headers = headers)

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
    $response = $client->request('POST','https://test-api.learnbyuse.app/api/v2/books/{book_id}/exercise', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/books/{book_id}/exercise");
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
        "Authorization": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test-api.learnbyuse.app/api/v2/books/{book_id}/exercise", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /books/{book_id}/exercise`

??????Book??????

<h3 id="post__books_{book_id}_exercise-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|book_id|path|integer|true|book id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "author": "string",
    "format": "string",
    "id": 0,
    "name": "string",
    "status": "string",
    "uri": "string"
  },
  "msg": "string"
}
```

<h3 id="post__books_{book_id}_exercise-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GetBookInfoResp response|[GetBookInfoResp](#schemagetbookinforesp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__books_{book_id}_info

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/books/{book_id}/info \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET https://test-api.learnbyuse.app/api/v2/books/{book_id}/info HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/books/{book_id}/info',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/books/{book_id}/info',
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

r = requests.get('https://test-api.learnbyuse.app/api/v2/books/{book_id}/info', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/books/{book_id}/info', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/books/{book_id}/info");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/books/{book_id}/info", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /books/{book_id}/info`

??????Book?????????

<h3 id="get__books_{book_id}_info-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|book_id|path|integer|true|book id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "author": "string",
    "format": "string",
    "id": 0,
    "name": "string",
    "status": "string",
    "uri": "string"
  },
  "msg": "string"
}
```

<h3 id="get__books_{book_id}_info-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GetBookInfoResp response|[GetBookInfoResp](#schemagetbookinforesp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__books_{book_id}_learn

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/books/{book_id}/learn \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET https://test-api.learnbyuse.app/api/v2/books/{book_id}/learn HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/books/{book_id}/learn',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/books/{book_id}/learn',
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

r = requests.get('https://test-api.learnbyuse.app/api/v2/books/{book_id}/learn', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/books/{book_id}/learn', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/books/{book_id}/learn");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/books/{book_id}/learn", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /books/{book_id}/learn`

????????????Book??????????????????

<h3 id="get__books_{book_id}_learn-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|book_id|path|integer|true|book id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "answer": "string",
      "card_id": 0,
      "frq": 0,
      "learn_times": 0,
      "proficiency": 0,
      "question": "string",
      "tips": "string"
    }
  ],
  "msg": "string",
  "pagination": {
    "current": 0,
    "size": 0,
    "total": 0
  }
}
```

<h3 id="get__books_{book_id}_learn-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[CardListResp](#schemacardlistresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__cards_{card_id}_learn

> Code samples

```shell
# You can also use wget
curl -X POST https://test-api.learnbyuse.app/api/v2/cards/{card_id}/learn \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test-api.learnbyuse.app/api/v2/cards/{card_id}/learn HTTP/1.1
Host: test-api.learnbyuse.app
Content-Type: application/json
Accept: application/json

```

```javascript
const inputBody = '{
  "proficiency": 0
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json'
};

fetch('https://test-api.learnbyuse.app/api/v2/cards/{card_id}/learn',
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

result = RestClient.post 'https://test-api.learnbyuse.app/api/v2/cards/{card_id}/learn',
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

r = requests.post('https://test-api.learnbyuse.app/api/v2/cards/{card_id}/learn', headers = headers)

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
    $response = $client->request('POST','https://test-api.learnbyuse.app/api/v2/cards/{card_id}/learn', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/cards/{card_id}/learn");
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
    req, err := http.NewRequest("POST", "https://test-api.learnbyuse.app/api/v2/cards/{card_id}/learn", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /cards/{card_id}/learn`

[????????????]????????????

> Body parameter

```json
{
  "proficiency": 0
}
```

<h3 id="post__cards_{card_id}_learn-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|card_id|path|integer|true|card id|
|body|body|[RatingCardsRequest](#schemaratingcardsrequest)|true|Rating card request|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "answer": "string",
    "card_id": 0,
    "frq": 0,
    "learn_times": 0,
    "proficiency": 0,
    "question": "string",
    "tips": "string"
  },
  "msg": "string"
}
```

<h3 id="post__cards_{card_id}_learn-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[RatingCardsResp](#schemaratingcardsresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="learnbyuse-api-share">Share</h1>

## get__s_{book_uuid}

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid} \
  -H 'Accept: application/json'

```

```http
GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid} HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/s/{book_uuid}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/s/{book_uuid}', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/s/{book_uuid}");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/s/{book_uuid}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /s/{book_uuid}`

?????????????????????

<h3 id="get__s_{book_uuid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|book_uuid|path|integer|true|book uuid|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__s_{book_uuid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__s_{book_uuid}_cards

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/cards \
  -H 'Accept: application/json'

```

```http
GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/cards HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/cards',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/cards',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/cards', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/cards', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/cards");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/cards", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /s/{book_uuid}/cards`

??????Book??????????????????

<h3 id="get__s_{book_uuid}_cards-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|book_uuid|path|integer|true|book uuid|
|page_current|query|integer|false|current page index, ???1??????|
|page_size|query|integer|false|size of page, ?????????: 15|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "answer": "string",
      "card_id": 0,
      "frq": 0,
      "learn_times": 0,
      "proficiency": 0,
      "question": "string",
      "tips": "string"
    }
  ],
  "msg": "string",
  "pagination": {
    "current": 0,
    "size": 0,
    "total": 0
  }
}
```

<h3 id="get__s_{book_uuid}_cards-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[CardListResp](#schemacardlistresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__s_{book_uuid}_download

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/download \
  -H 'Accept: application/json'

```

```http
GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/download HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/download',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/download',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/download', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/download', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/download");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/download", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /s/{book_uuid}/download`

????????????????????????

<h3 id="get__s_{book_uuid}_download-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|book_uuid|path|integer|true|book uuid|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__s_{book_uuid}_download-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__s_{book_uuid}_exercise

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/exercise \
  -H 'Accept: application/json'

```

```http
GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/exercise HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/exercise',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/exercise',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/exercise', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/exercise', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/exercise");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/exercise", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /s/{book_uuid}/exercise`

????????????????????????????????????

<h3 id="get__s_{book_uuid}_exercise-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|book_uuid|path|integer|true|book uuid|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "answer": "string",
      "card_id": 0,
      "frq": 0,
      "learn_times": 0,
      "proficiency": 0,
      "question": "string",
      "tips": "string"
    }
  ],
  "msg": "string",
  "pagination": {
    "current": 0,
    "size": 0,
    "total": 0
  }
}
```

<h3 id="get__s_{book_uuid}_exercise-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|CardListResp response|[CardListResp](#schemacardlistresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## get__s_{book_uuid}_info

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/info \
  -H 'Accept: application/json'

```

```http
GET https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/info HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/info',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/info',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/info', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/info', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/info");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/s/{book_uuid}/info", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /s/{book_uuid}/info`

????????????Book?????????

<h3 id="get__s_{book_uuid}_info-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|book_uuid|path|integer|true|book uuid|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "author": "string",
    "name": "string",
    "share_user": "string"
  },
  "msg": "string"
}
```

<h3 id="get__s_{book_uuid}_info-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|GetShareBookInfoResp response|[GetShareBookInfoResp](#schemagetsharebookinforesp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__share_{book_id}

> Code samples

```shell
# You can also use wget
curl -X POST https://test-api.learnbyuse.app/api/v2/share/{book_id} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST https://test-api.learnbyuse.app/api/v2/share/{book_id} HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/share/{book_id}',
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
  'Accept' => 'application/json',
  'Authorization' => 'string'
}

result = RestClient.post 'https://test-api.learnbyuse.app/api/v2/share/{book_id}',
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

r = requests.post('https://test-api.learnbyuse.app/api/v2/share/{book_id}', headers = headers)

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
    $response = $client->request('POST','https://test-api.learnbyuse.app/api/v2/share/{book_id}', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/share/{book_id}");
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
        "Authorization": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test-api.learnbyuse.app/api/v2/share/{book_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /share/{book_id}`

share book

<h3 id="post__share_{book_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|book_id|path|integer|true|book id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__share_{book_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="learnbyuse-api-user">User</h1>

## post__user_login

> Code samples

```shell
# You can also use wget
curl -X POST https://test-api.learnbyuse.app/api/v2/user/login \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test-api.learnbyuse.app/api/v2/user/login HTTP/1.1
Host: test-api.learnbyuse.app
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

fetch('https://test-api.learnbyuse.app/api/v2/user/login',
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

result = RestClient.post 'https://test-api.learnbyuse.app/api/v2/user/login',
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

r = requests.post('https://test-api.learnbyuse.app/api/v2/user/login', headers = headers)

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
    $response = $client->request('POST','https://test-api.learnbyuse.app/api/v2/user/login', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/user/login");
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
    req, err := http.NewRequest("POST", "https://test-api.learnbyuse.app/api/v2/user/login", data)
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
    "email": "string",
    "nick_name": "string",
    "token": "string",
    "vocablevel": 0
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
This operation does not require authentication
</aside>

## post__user_register

> Code samples

```shell
# You can also use wget
curl -X POST https://test-api.learnbyuse.app/api/v2/user/register \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST https://test-api.learnbyuse.app/api/v2/user/register HTTP/1.1
Host: test-api.learnbyuse.app
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

fetch('https://test-api.learnbyuse.app/api/v2/user/register',
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

result = RestClient.post 'https://test-api.learnbyuse.app/api/v2/user/register',
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

r = requests.post('https://test-api.learnbyuse.app/api/v2/user/register', headers = headers)

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
    $response = $client->request('POST','https://test-api.learnbyuse.app/api/v2/user/register', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/user/register");
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
    req, err := http.NewRequest("POST", "https://test-api.learnbyuse.app/api/v2/user/register", data)
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

<h1 id="learnbyuse-api-vocab">Vocab</h1>

## get__vocab_test

> Code samples

```shell
# You can also use wget
curl -X GET https://test-api.learnbyuse.app/api/v2/vocab/test \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET https://test-api.learnbyuse.app/api/v2/vocab/test HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/vocab/test',
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

result = RestClient.get 'https://test-api.learnbyuse.app/api/v2/vocab/test',
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

r = requests.get('https://test-api.learnbyuse.app/api/v2/vocab/test', headers = headers)

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
    $response = $client->request('GET','https://test-api.learnbyuse.app/api/v2/vocab/test', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/vocab/test");
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
    req, err := http.NewRequest("GET", "https://test-api.learnbyuse.app/api/v2/vocab/test", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /vocab/test`

[???????????????]?????????,????????????

<h3 id="get__vocab_test-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": "string",
  "msg": "string"
}
```

<h3 id="get__vocab_test-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|WordTestResp|[WordTestResp](#schemawordtestresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

## post__vocab_test_nextword

> Code samples

```shell
# You can also use wget
curl -X POST https://test-api.learnbyuse.app/api/v2/vocab/test/nextword?answer=string \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST https://test-api.learnbyuse.app/api/v2/vocab/test/nextword?answer=string HTTP/1.1
Host: test-api.learnbyuse.app
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('https://test-api.learnbyuse.app/api/v2/vocab/test/nextword?answer=string',
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
  'Accept' => 'application/json',
  'Authorization' => 'string'
}

result = RestClient.post 'https://test-api.learnbyuse.app/api/v2/vocab/test/nextword',
  params: {
  'answer' => 'string'
}, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json',
  'Authorization': 'string'
}

r = requests.post('https://test-api.learnbyuse.app/api/v2/vocab/test/nextword', params={
  'answer': 'string'
}, headers = headers)

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
    $response = $client->request('POST','https://test-api.learnbyuse.app/api/v2/vocab/test/nextword', array(
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
URL obj = new URL("https://test-api.learnbyuse.app/api/v2/vocab/test/nextword?answer=string");
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
        "Authorization": []string{"string"},
    }

    data := bytes.NewBuffer([]byte{jsonReq})
    req, err := http.NewRequest("POST", "https://test-api.learnbyuse.app/api/v2/vocab/test/nextword", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /vocab/test/nextword`

[???????????????]???????????????

<h3 id="post__vocab_test_nextword-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|answer|query|string|true|yes/no|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": "string",
  "msg": "string"
}
```

<h3 id="post__vocab_test_nextword-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|WordTestResp|[WordTestResp](#schemawordtestresp)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_BookInfo">BookInfo</h2>
<!-- backwards compatibility -->
<a id="schemabookinfo"></a>
<a id="schema_BookInfo"></a>
<a id="tocSbookinfo"></a>
<a id="tocsbookinfo"></a>

```json
{
  "author": "string",
  "format": "string",
  "id": 0,
  "name": "string",
  "status": "string",
  "uri": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|author|string|false|none|Book's Author|
|format|string|false|none|Book format type [html, txt, pdf, epub, mobi]|
|id|integer|false|none|Book ID|
|name|string|false|none|Book name|
|status|string|false|none|Book??????, BookNew, BookInBuilding, BookBuildEnd|
|uri|string|false|none|Book's HTML URI'|

<h2 id="tocS_CardItem">CardItem</h2>
<!-- backwards compatibility -->
<a id="schemacarditem"></a>
<a id="schema_CardItem"></a>
<a id="tocScarditem"></a>
<a id="tocscarditem"></a>

```json
{
  "answer": "string",
  "card_id": 0,
  "frq": 0,
  "learn_times": 0,
  "proficiency": 0,
  "question": "string",
  "tips": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|answer|string|false|none|????????????|
|card_id|integer|false|none|??????ID|
|frq|integer|false|none|??????|
|learn_times|integer|false|none|??????????????????|
|proficiency|integer|false|none|???????????????|
|question|string|false|none|????????????|
|tips|string|false|none|????????????|

<h2 id="tocS_CardListResp">CardListResp</h2>
<!-- backwards compatibility -->
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
      "frq": 0,
      "learn_times": 0,
      "proficiency": 0,
      "question": "string",
      "tips": "string"
    }
  ],
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
|data|[[CardItem](#schemacarditem)]|false|none|book????????????|
|msg|string|false|none|none|
|pagination|[Pagination](#schemapagination)|false|none|none|

<h2 id="tocS_GetBookInfoResp">GetBookInfoResp</h2>
<!-- backwards compatibility -->
<a id="schemagetbookinforesp"></a>
<a id="schema_GetBookInfoResp"></a>
<a id="tocSgetbookinforesp"></a>
<a id="tocsgetbookinforesp"></a>

```json
{
  "code": 0,
  "data": {
    "author": "string",
    "format": "string",
    "id": 0,
    "name": "string",
    "status": "string",
    "uri": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[BookInfo](#schemabookinfo)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_GetBookResp">GetBookResp</h2>
<!-- backwards compatibility -->
<a id="schemagetbookresp"></a>
<a id="schema_GetBookResp"></a>
<a id="tocSgetbookresp"></a>
<a id="tocsgetbookresp"></a>

```json
{
  "code": 0,
  "data": {
    "author": "string",
    "format": "string",
    "id": 0,
    "name": "string",
    "status": "string",
    "uri": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[BookInfo](#schemabookinfo)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_GetShareBookInfoResp">GetShareBookInfoResp</h2>
<!-- backwards compatibility -->
<a id="schemagetsharebookinforesp"></a>
<a id="schema_GetShareBookInfoResp"></a>
<a id="tocSgetsharebookinforesp"></a>
<a id="tocsgetsharebookinforesp"></a>

```json
{
  "code": 0,
  "data": {
    "author": "string",
    "name": "string",
    "share_user": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[ShareBookInfo](#schemasharebookinfo)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_ListBookResp">ListBookResp</h2>
<!-- backwards compatibility -->
<a id="schemalistbookresp"></a>
<a id="schema_ListBookResp"></a>
<a id="tocSlistbookresp"></a>
<a id="tocslistbookresp"></a>

```json
{
  "code": 0,
  "data": [
    {
      "author": "string",
      "format": "string",
      "id": 0,
      "name": "string",
      "status": "string",
      "uri": "string"
    }
  ],
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[[BookInfo](#schemabookinfo)]|false|none|Book??????|
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
|email|string|true|none|??????email??????|
|password|string|true|none|????????????|

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
  "token": "string",
  "vocablevel": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|email|string|true|none|??????email??????|
|nick_name|string|true|none|????????????|
|token|string|false|none|??????token|
|vocablevel|integer|false|none|??????????????????|

<h2 id="tocS_LoginResponse">LoginResponse</h2>
<!-- backwards compatibility -->
<a id="schemaloginresponse"></a>
<a id="schema_LoginResponse"></a>
<a id="tocSloginresponse"></a>
<a id="tocsloginresponse"></a>

```json
{
  "code": 0,
  "data": {
    "email": "string",
    "nick_name": "string",
    "token": "string",
    "vocablevel": 0
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
<!-- backwards compatibility -->
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

<h2 id="tocS_RatingCardsRequest">RatingCardsRequest</h2>
<!-- backwards compatibility -->
<a id="schemaratingcardsrequest"></a>
<a id="schema_RatingCardsRequest"></a>
<a id="tocSratingcardsrequest"></a>
<a id="tocsratingcardsrequest"></a>

```json
{
  "proficiency": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|proficiency|integer|true|none|????????????|

<h2 id="tocS_RatingCardsResp">RatingCardsResp</h2>
<!-- backwards compatibility -->
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
    "frq": 0,
    "learn_times": 0,
    "proficiency": 0,
    "question": "string",
    "tips": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[CardItem](#schemacarditem)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_ShareBookInfo">ShareBookInfo</h2>
<!-- backwards compatibility -->
<a id="schemasharebookinfo"></a>
<a id="schema_ShareBookInfo"></a>
<a id="tocSsharebookinfo"></a>
<a id="tocssharebookinfo"></a>

```json
{
  "author": "string",
  "name": "string",
  "share_user": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|author|string|false|none|Book's Author|
|name|string|false|none|Book name|
|share_user|string|false|none|????????????????????????|

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
|email|string|true|none|??????email??????|
|nick_name|string|true|none|??????nick_named|
|password|string|true|none|????????????|

<h2 id="tocS_WordTestResp">WordTestResp</h2>
<!-- backwards compatibility -->
<a id="schemawordtestresp"></a>
<a id="schema_WordTestResp"></a>
<a id="tocSwordtestresp"></a>
<a id="tocswordtestresp"></a>

```json
{
  "code": 0,
  "data": "string",
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|string|false|none|?????????????????????????????????|
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

