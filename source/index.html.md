---
title: Yield Dance API v2
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

<h1 id="yield-dance-api">Yield Dance API v2</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Welcome to the Yield Dance API! You can use our API to access Yield Dance API endpoints.

Base URLs:

* <a href="http://localhost:4928/api/v2">http://localhost:4928/api/v2</a>

<h1 id="yield-dance-api-admin">Admin</h1>

## get__admin_balance_{asset_id}

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/admin/balance/{asset_id} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/admin/balance/{asset_id} HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/balance/{asset_id}',
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

result = RestClient.get 'http://localhost:4928/api/v2/admin/balance/{asset_id}',
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

r = requests.get('http://localhost:4928/api/v2/admin/balance/{asset_id}', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/admin/balance/{asset_id}', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/balance/{asset_id}");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/admin/balance/{asset_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /admin/balance/{asset_id}`

get asset balance by admin

<h3 id="get__admin_balance_{asset_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|asset_id|path|string|true|asset id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__admin_balance_{asset_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## get__admin_rounds

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/admin/rounds \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/admin/rounds HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds',
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

result = RestClient.get 'http://localhost:4928/api/v2/admin/rounds',
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

r = requests.get('http://localhost:4928/api/v2/admin/rounds', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/admin/rounds', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/admin/rounds", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /admin/rounds`

Get a round list by admin

<h3 id="get__admin_rounds-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|vault_type|query|integer|false|Type of vault|
|status|query|integer|false|Status of round|
|page_current|query|integer|false|current page index|
|page_size|query|integer|false|size of page|
|Authorization|header|string|true|Authorization|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "clearing_info": {
        "clearing_amount": "string",
        "clearing_asset_id": "string",
        "clearing_draft_amount": "string",
        "clearing_users": "string",
        "exercised": true,
        "underlying_asset_id": "string",
        "underlying_price": "string"
      },
      "fund_info": {
        "apy_real": "string",
        "min_unit": "string",
        "order_recv_amount": "string",
        "order_recv_users": "string",
        "outbound_asset_id": "string",
        "premium_amount": "string"
      },
      "insurances": [
        {
          "compensation_amount": "string",
          "compensation_asset_id": "string",
          "compensation_price": "string",
          "description": "string",
          "exercised": true,
          "id": 0,
          "label": "string",
          "type": "string"
        }
      ],
      "outbound_info": {
        "amount": "string",
        "fraction_amount": "string",
        "fraction_asset_id": "string",
        "fraction_users": "string",
        "premium_amount": "string",
        "premium_asset_id": "string",
        "premium_users": "string",
        "refund_amount": "string",
        "refund_asset_id": "string",
        "refund_users": "string"
      },
      "round_activities": [
        {
          "activity_type": "string",
          "amount": "string",
          "asset_id": "string",
          "created_at": "string",
          "mixin_user_id": "string",
          "mixin_user_name": "string",
          "oid": "string",
          "remark": "string",
          "status": "string",
          "trace_id": "string"
        }
      ],
      "round_info": {
        "apy_max": "string",
        "apy_min": "string",
        "clearing_asset_id": "string",
        "clearing_at": "string",
        "created_at": "string",
        "exercised": true,
        "expiry": "string",
        "funding_asset_id": "string",
        "funding_end_at": "string",
        "hide": true,
        "insurance_enable": true,
        "max_fund": "string",
        "min_fund": "string",
        "rid": "string",
        "status": "string",
        "strike": "string",
        "updated_at": "string",
        "vault_type": "string"
      }
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

<h3 id="get__admin_rounds-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of round item wrapped in common response|[ListRoundResponse](#schemalistroundresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## post__admin_rounds

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v2/admin/rounds \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST http://localhost:4928/api/v2/admin/rounds HTTP/1.1
Host: localhost:4928
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "apy_max": "string",
  "apy_min": "string",
  "clearing_asset_id": "string",
  "clearing_at": "string",
  "expiry": "string",
  "funding_asset_id": "string",
  "funding_end_at": "string",
  "funding_start_at": "string",
  "hide": true,
  "insurance_enable": true,
  "insurances": [
    {
      "description": "string",
      "id": 0,
      "label": "string"
    }
  ],
  "max_fund": "string",
  "min_fund": "string",
  "strike": "string",
  "vault_type": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds',
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

result = RestClient.post 'http://localhost:4928/api/v2/admin/rounds',
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

r = requests.post('http://localhost:4928/api/v2/admin/rounds', headers = headers)

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
    $response = $client->request('POST','http://localhost:4928/api/v2/admin/rounds', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds");
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
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v2/admin/rounds", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /admin/rounds`

Add a new round by admin

> Body parameter

```json
{
  "apy_max": "string",
  "apy_min": "string",
  "clearing_asset_id": "string",
  "clearing_at": "string",
  "expiry": "string",
  "funding_asset_id": "string",
  "funding_end_at": "string",
  "funding_start_at": "string",
  "hide": true,
  "insurance_enable": true,
  "insurances": [
    {
      "description": "string",
      "id": 0,
      "label": "string"
    }
  ],
  "max_fund": "string",
  "min_fund": "string",
  "strike": "string",
  "vault_type": "string"
}
```

<h3 id="post__admin_rounds-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|body|body|[RoundRequest](#schemaroundrequest)|true|Round info|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "clearing_info": {
      "clearing_amount": "string",
      "clearing_asset_id": "string",
      "clearing_draft_amount": "string",
      "clearing_users": "string",
      "exercised": true,
      "underlying_asset_id": "string",
      "underlying_price": "string"
    },
    "fund_info": {
      "apy_real": "string",
      "min_unit": "string",
      "order_recv_amount": "string",
      "order_recv_users": "string",
      "outbound_asset_id": "string",
      "premium_amount": "string"
    },
    "insurances": [
      {
        "compensation_amount": "string",
        "compensation_asset_id": "string",
        "compensation_price": "string",
        "description": "string",
        "exercised": true,
        "id": 0,
        "label": "string",
        "type": "string"
      }
    ],
    "outbound_info": {
      "amount": "string",
      "fraction_amount": "string",
      "fraction_asset_id": "string",
      "fraction_users": "string",
      "premium_amount": "string",
      "premium_asset_id": "string",
      "premium_users": "string",
      "refund_amount": "string",
      "refund_asset_id": "string",
      "refund_users": "string"
    },
    "round_activities": [
      {
        "activity_type": "string",
        "amount": "string",
        "asset_id": "string",
        "created_at": "string",
        "mixin_user_id": "string",
        "mixin_user_name": "string",
        "oid": "string",
        "remark": "string",
        "status": "string",
        "trace_id": "string"
      }
    ],
    "round_info": {
      "apy_max": "string",
      "apy_min": "string",
      "clearing_asset_id": "string",
      "clearing_at": "string",
      "created_at": "string",
      "exercised": true,
      "expiry": "string",
      "funding_asset_id": "string",
      "funding_end_at": "string",
      "hide": true,
      "insurance_enable": true,
      "max_fund": "string",
      "min_fund": "string",
      "rid": "string",
      "status": "string",
      "strike": "string",
      "updated_at": "string",
      "vault_type": "string"
    }
  },
  "msg": "string"
}
```

<h3 id="post__admin_rounds-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|round item wrapped in response|[CommonRoundResponse](#schemacommonroundresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## get__admin_rounds_{rid}

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/admin/rounds/{rid} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/admin/rounds/{rid} HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds/{rid}',
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

result = RestClient.get 'http://localhost:4928/api/v2/admin/rounds/{rid}',
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

r = requests.get('http://localhost:4928/api/v2/admin/rounds/{rid}', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/admin/rounds/{rid}', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds/{rid}");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/admin/rounds/{rid}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /admin/rounds/{rid}`

Get a round

<h3 id="get__admin_rounds_{rid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|rid|path|string|true|round id|
|Authorization|header|string|true|Authorization|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "clearing_info": {
      "clearing_amount": "string",
      "clearing_asset_id": "string",
      "clearing_draft_amount": "string",
      "clearing_users": "string",
      "exercised": true,
      "underlying_asset_id": "string",
      "underlying_price": "string"
    },
    "fund_info": {
      "apy_real": "string",
      "min_unit": "string",
      "order_recv_amount": "string",
      "order_recv_users": "string",
      "outbound_asset_id": "string",
      "premium_amount": "string"
    },
    "insurances": [
      {
        "compensation_amount": "string",
        "compensation_asset_id": "string",
        "compensation_price": "string",
        "description": "string",
        "exercised": true,
        "id": 0,
        "label": "string",
        "type": "string"
      }
    ],
    "outbound_info": {
      "amount": "string",
      "fraction_amount": "string",
      "fraction_asset_id": "string",
      "fraction_users": "string",
      "premium_amount": "string",
      "premium_asset_id": "string",
      "premium_users": "string",
      "refund_amount": "string",
      "refund_asset_id": "string",
      "refund_users": "string"
    },
    "round_activities": [
      {
        "activity_type": "string",
        "amount": "string",
        "asset_id": "string",
        "created_at": "string",
        "mixin_user_id": "string",
        "mixin_user_name": "string",
        "oid": "string",
        "remark": "string",
        "status": "string",
        "trace_id": "string"
      }
    ],
    "round_info": {
      "apy_max": "string",
      "apy_min": "string",
      "clearing_asset_id": "string",
      "clearing_at": "string",
      "created_at": "string",
      "exercised": true,
      "expiry": "string",
      "funding_asset_id": "string",
      "funding_end_at": "string",
      "hide": true,
      "insurance_enable": true,
      "max_fund": "string",
      "min_fund": "string",
      "rid": "string",
      "status": "string",
      "strike": "string",
      "updated_at": "string",
      "vault_type": "string"
    }
  },
  "msg": "string"
}
```

<h3 id="get__admin_rounds_{rid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of round item wrapped in common response|[CommonRoundResponse](#schemacommonroundresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## put__admin_rounds_{rid}

> Code samples

```shell
# You can also use wget
curl -X PUT http://localhost:4928/api/v2/admin/rounds/{rid} \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
PUT http://localhost:4928/api/v2/admin/rounds/{rid} HTTP/1.1
Host: localhost:4928
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "apy_max": "string",
  "apy_min": "string",
  "clearing_asset_id": "string",
  "clearing_at": "string",
  "expiry": "string",
  "funding_asset_id": "string",
  "funding_end_at": "string",
  "funding_start_at": "string",
  "hide": true,
  "insurance_enable": true,
  "insurances": [
    {
      "description": "string",
      "id": 0,
      "label": "string"
    }
  ],
  "max_fund": "string",
  "min_fund": "string",
  "strike": "string",
  "vault_type": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds/{rid}',
{
  method: 'PUT',
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

result = RestClient.put 'http://localhost:4928/api/v2/admin/rounds/{rid}',
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

r = requests.put('http://localhost:4928/api/v2/admin/rounds/{rid}', headers = headers)

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
    $response = $client->request('PUT','http://localhost:4928/api/v2/admin/rounds/{rid}', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds/{rid}");
HttpURLConnection con = (HttpURLConnection) obj.openConnection();
con.setRequestMethod("PUT");
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
    req, err := http.NewRequest("PUT", "http://localhost:4928/api/v2/admin/rounds/{rid}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`PUT /admin/rounds/{rid}`

Update the round

> Body parameter

```json
{
  "apy_max": "string",
  "apy_min": "string",
  "clearing_asset_id": "string",
  "clearing_at": "string",
  "expiry": "string",
  "funding_asset_id": "string",
  "funding_end_at": "string",
  "funding_start_at": "string",
  "hide": true,
  "insurance_enable": true,
  "insurances": [
    {
      "description": "string",
      "id": 0,
      "label": "string"
    }
  ],
  "max_fund": "string",
  "min_fund": "string",
  "strike": "string",
  "vault_type": "string"
}
```

<h3 id="put__admin_rounds_{rid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|rid|path|string|true|round id|
|Authorization|header|string|true|Authorization|
|body|body|[RoundRequest](#schemaroundrequest)|true|Round update info|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "clearing_info": {
      "clearing_amount": "string",
      "clearing_asset_id": "string",
      "clearing_draft_amount": "string",
      "clearing_users": "string",
      "exercised": true,
      "underlying_asset_id": "string",
      "underlying_price": "string"
    },
    "fund_info": {
      "apy_real": "string",
      "min_unit": "string",
      "order_recv_amount": "string",
      "order_recv_users": "string",
      "outbound_asset_id": "string",
      "premium_amount": "string"
    },
    "insurances": [
      {
        "compensation_amount": "string",
        "compensation_asset_id": "string",
        "compensation_price": "string",
        "description": "string",
        "exercised": true,
        "id": 0,
        "label": "string",
        "type": "string"
      }
    ],
    "outbound_info": {
      "amount": "string",
      "fraction_amount": "string",
      "fraction_asset_id": "string",
      "fraction_users": "string",
      "premium_amount": "string",
      "premium_asset_id": "string",
      "premium_users": "string",
      "refund_amount": "string",
      "refund_asset_id": "string",
      "refund_users": "string"
    },
    "round_activities": [
      {
        "activity_type": "string",
        "amount": "string",
        "asset_id": "string",
        "created_at": "string",
        "mixin_user_id": "string",
        "mixin_user_name": "string",
        "oid": "string",
        "remark": "string",
        "status": "string",
        "trace_id": "string"
      }
    ],
    "round_info": {
      "apy_max": "string",
      "apy_min": "string",
      "clearing_asset_id": "string",
      "clearing_at": "string",
      "created_at": "string",
      "exercised": true,
      "expiry": "string",
      "funding_asset_id": "string",
      "funding_end_at": "string",
      "hide": true,
      "insurance_enable": true,
      "max_fund": "string",
      "min_fund": "string",
      "rid": "string",
      "status": "string",
      "strike": "string",
      "updated_at": "string",
      "vault_type": "string"
    }
  },
  "msg": "string"
}
```

<h3 id="put__admin_rounds_{rid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[CommonRoundResponse](#schemacommonroundresponse)|

<aside class="success">
 
</aside>

## delete__admin_rounds_{rid}

> Code samples

```shell
# You can also use wget
curl -X DELETE http://localhost:4928/api/v2/admin/rounds/{rid} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
DELETE http://localhost:4928/api/v2/admin/rounds/{rid} HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds/{rid}',
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

result = RestClient.delete 'http://localhost:4928/api/v2/admin/rounds/{rid}',
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

r = requests.delete('http://localhost:4928/api/v2/admin/rounds/{rid}', headers = headers)

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
    $response = $client->request('DELETE','http://localhost:4928/api/v2/admin/rounds/{rid}', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds/{rid}");
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
    req, err := http.NewRequest("DELETE", "http://localhost:4928/api/v2/admin/rounds/{rid}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`DELETE /admin/rounds/{rid}`

Del a round by admin

<h3 id="delete__admin_rounds_{rid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|rid|path|string|true|Round id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="delete__admin_rounds_{rid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## get__admin_rounds_{rid}_activities

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/admin/rounds/{rid}/activities \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/admin/rounds/{rid}/activities HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds/{rid}/activities',
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

result = RestClient.get 'http://localhost:4928/api/v2/admin/rounds/{rid}/activities',
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

r = requests.get('http://localhost:4928/api/v2/admin/rounds/{rid}/activities', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/admin/rounds/{rid}/activities', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds/{rid}/activities");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/admin/rounds/{rid}/activities", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /admin/rounds/{rid}/activities`

get a round's activities by admin

<h3 id="get__admin_rounds_{rid}_activities-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|rid|path|string|true|round id|
|activity_type|query|string|false|the type of activity|
|page_current|query|integer|false|current page index|
|page_size|query|integer|false|size of page|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "activity_type": "string",
      "amount": "string",
      "asset_id": "string",
      "created_at": "string",
      "mixin_user_id": "string",
      "mixin_user_name": "string",
      "oid": "string",
      "remark": "string",
      "status": "string",
      "trace_id": "string"
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

<h3 id="get__admin_rounds_{rid}_activities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|list of activity response|[ListActivityResponse](#schemalistactivityresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## post__admin_rounds_{rid}_insurance

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v2/admin/rounds/{rid}/insurance \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST http://localhost:4928/api/v2/admin/rounds/{rid}/insurance HTTP/1.1
Host: localhost:4928
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "compensation_amount": "string",
  "compensation_asset_id": "string",
  "compensation_price": "string",
  "exercised": true,
  "id": 0,
  "operation": "string",
  "type": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds/{rid}/insurance',
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

result = RestClient.post 'http://localhost:4928/api/v2/admin/rounds/{rid}/insurance',
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

r = requests.post('http://localhost:4928/api/v2/admin/rounds/{rid}/insurance', headers = headers)

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
    $response = $client->request('POST','http://localhost:4928/api/v2/admin/rounds/{rid}/insurance', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds/{rid}/insurance");
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
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v2/admin/rounds/{rid}/insurance", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /admin/rounds/{rid}/insurance`

Admin execute insurance

> Body parameter

```json
{
  "compensation_amount": "string",
  "compensation_asset_id": "string",
  "compensation_price": "string",
  "exercised": true,
  "id": 0,
  "operation": "string",
  "type": "string"
}
```

<h3 id="post__admin_rounds_{rid}_insurance-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|rid|path|string|true|round  id|
|Authorization|header|string|true|Authorization|
|body|body|[RoundInsuranceReq](#schemaroundinsurancereq)|true|insurance operation request|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "amount": "string"
  },
  "msg": "string"
}
```

<h3 id="post__admin_rounds_{rid}_insurance-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|insurance operation response|[CommonInsuranceResponse](#schemacommoninsuranceresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[CommonInsuranceResponse](#schemacommoninsuranceresponse)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Common response|[CommonInsuranceResponse](#schemacommoninsuranceresponse)|

<aside class="success">
 
</aside>

## post__admin_rounds_{rid}_notice

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v2/admin/rounds/{rid}/notice \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST http://localhost:4928/api/v2/admin/rounds/{rid}/notice HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds/{rid}/notice',
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

result = RestClient.post 'http://localhost:4928/api/v2/admin/rounds/{rid}/notice',
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

r = requests.post('http://localhost:4928/api/v2/admin/rounds/{rid}/notice', headers = headers)

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
    $response = $client->request('POST','http://localhost:4928/api/v2/admin/rounds/{rid}/notice', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds/{rid}/notice");
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
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v2/admin/rounds/{rid}/notice", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /admin/rounds/{rid}/notice`

notice users that a new round has been created

<h3 id="post__admin_rounds_{rid}_notice-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|rid|path|string|true|Round id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="post__admin_rounds_{rid}_notice-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## post__admin_rounds_{rid}_operation

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v2/admin/rounds/{rid}/operation \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST http://localhost:4928/api/v2/admin/rounds/{rid}/operation HTTP/1.1
Host: localhost:4928
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "amount": "string",
  "asset_id": "string",
  "exercised": true,
  "insurance": {
    "compensation_amount": "string",
    "compensation_asset_id": "string",
    "compensation_price": "string",
    "description": "string",
    "exercised": true,
    "id": 0,
    "label": "string",
    "type": "string"
  },
  "min_unit": "string",
  "operation": "string",
  "underlying_price": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds/{rid}/operation',
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

result = RestClient.post 'http://localhost:4928/api/v2/admin/rounds/{rid}/operation',
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

r = requests.post('http://localhost:4928/api/v2/admin/rounds/{rid}/operation', headers = headers)

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
    $response = $client->request('POST','http://localhost:4928/api/v2/admin/rounds/{rid}/operation', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds/{rid}/operation");
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
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v2/admin/rounds/{rid}/operation", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /admin/rounds/{rid}/operation`

Admin execute operation

> Body parameter

```json
{
  "amount": "string",
  "asset_id": "string",
  "exercised": true,
  "insurance": {
    "compensation_amount": "string",
    "compensation_asset_id": "string",
    "compensation_price": "string",
    "description": "string",
    "exercised": true,
    "id": 0,
    "label": "string",
    "type": "string"
  },
  "min_unit": "string",
  "operation": "string",
  "underlying_price": "string"
}
```

<h3 id="post__admin_rounds_{rid}_operation-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|rid|path|string|true|round id|
|Authorization|header|string|true|Authorization|
|body|body|[RoundOperationReq](#schemaroundoperationreq)|true|round operation request|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "clearing_info": {
      "clearing_amount": "string",
      "clearing_asset_id": "string",
      "clearing_draft_amount": "string",
      "clearing_users": "string",
      "exercised": true,
      "underlying_asset_id": "string",
      "underlying_price": "string"
    },
    "fund_info": {
      "apy_real": "string",
      "min_unit": "string",
      "order_recv_amount": "string",
      "order_recv_users": "string",
      "outbound_asset_id": "string",
      "premium_amount": "string"
    },
    "insurances": [
      {
        "compensation_amount": "string",
        "compensation_asset_id": "string",
        "compensation_price": "string",
        "description": "string",
        "exercised": true,
        "id": 0,
        "label": "string",
        "type": "string"
      }
    ],
    "outbound_info": {
      "amount": "string",
      "fraction_amount": "string",
      "fraction_asset_id": "string",
      "fraction_users": "string",
      "premium_amount": "string",
      "premium_asset_id": "string",
      "premium_users": "string",
      "refund_amount": "string",
      "refund_asset_id": "string",
      "refund_users": "string"
    },
    "round_activities": [
      {
        "activity_type": "string",
        "amount": "string",
        "asset_id": "string",
        "created_at": "string",
        "mixin_user_id": "string",
        "mixin_user_name": "string",
        "oid": "string",
        "remark": "string",
        "status": "string",
        "trace_id": "string"
      }
    ],
    "round_info": {
      "apy_max": "string",
      "apy_min": "string",
      "clearing_asset_id": "string",
      "clearing_at": "string",
      "created_at": "string",
      "exercised": true,
      "expiry": "string",
      "funding_asset_id": "string",
      "funding_end_at": "string",
      "hide": true,
      "insurance_enable": true,
      "max_fund": "string",
      "min_fund": "string",
      "rid": "string",
      "status": "string",
      "strike": "string",
      "updated_at": "string",
      "vault_type": "string"
    }
  },
  "msg": "string"
}
```

<h3 id="post__admin_rounds_{rid}_operation-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|round operation response|[CommonRoundResponse](#schemacommonroundresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|
|500|[Internal Server Error](https://tools.ietf.org/html/rfc7231#section-6.6.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## get__admin_rounds_{rid}_orders

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/admin/rounds/{rid}/orders \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/admin/rounds/{rid}/orders HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/admin/rounds/{rid}/orders',
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

result = RestClient.get 'http://localhost:4928/api/v2/admin/rounds/{rid}/orders',
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

r = requests.get('http://localhost:4928/api/v2/admin/rounds/{rid}/orders', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/admin/rounds/{rid}/orders', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/rounds/{rid}/orders");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/admin/rounds/{rid}/orders", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /admin/rounds/{rid}/orders`

Get order list

<h3 id="get__admin_rounds_{rid}_orders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|rid|path|string|true|round id|
|page_current|query|integer|false|current page index|
|page_size|query|integer|false|size of page|
|Authorization|header|string|true|Authorization|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "amount": "string",
      "apy_real": "string",
      "clearing_amount": "string",
      "clearing_asset_id": "string",
      "created_at": "string",
      "fraction_amount": "string",
      "fraction_asset_id": "string",
      "insurances": [
        {
          "compensation_amount": "string",
          "compensation_asset_id": "string",
          "compensation_price": "string",
          "description": "string",
          "exercised": true,
          "id": 0,
          "label": "string",
          "type": "string"
        }
      ],
      "mixin_user_id": "string",
      "mixin_user_name": "string",
      "oid": "string",
      "premium_amount": "string",
      "premium_asset_id": "string",
      "refund_amount": "string",
      "rid": "string",
      "round": {
        "apy_max": "string",
        "apy_min": "string",
        "clearing_asset_id": "string",
        "clearing_at": "string",
        "created_at": "string",
        "exercised": true,
        "expiry": "string",
        "funding_asset_id": "string",
        "funding_end_at": "string",
        "hide": true,
        "insurance_enable": true,
        "max_fund": "string",
        "min_fund": "string",
        "rid": "string",
        "status": "string",
        "strike": "string",
        "updated_at": "string",
        "vault_type": "string"
      },
      "underlying_asset_id": "string",
      "underlying_price": "string",
      "updated_at": "string"
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

<h3 id="get__admin_rounds_{rid}_orders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of round item wrapped in common response|[ListOrderResponse](#schemalistorderresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

<h1 id="yield-dance-api-authorization">Authorization</h1>

## post__admin_change_password

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v2/admin/change_password \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST http://localhost:4928/api/v2/admin/change_password HTTP/1.1
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

fetch('http://localhost:4928/api/v2/admin/change_password',
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

result = RestClient.post 'http://localhost:4928/api/v2/admin/change_password',
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

r = requests.post('http://localhost:4928/api/v2/admin/change_password', headers = headers)

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
    $response = $client->request('POST','http://localhost:4928/api/v2/admin/change_password', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/change_password");
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
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v2/admin/change_password", data)
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
 
</aside>

## post__admin_login

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v2/admin/login \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://localhost:4928/api/v2/admin/login HTTP/1.1
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

fetch('http://localhost:4928/api/v2/admin/login',
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

result = RestClient.post 'http://localhost:4928/api/v2/admin/login',
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

r = requests.post('http://localhost:4928/api/v2/admin/login', headers = headers)

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
    $response = $client->request('POST','http://localhost:4928/api/v2/admin/login', array(
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
URL obj = new URL("http://localhost:4928/api/v2/admin/login");
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
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v2/admin/login", data)
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
 
</aside>

## post__auth

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v2/auth \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json'

```

```http
POST http://localhost:4928/api/v2/auth HTTP/1.1
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

fetch('http://localhost:4928/api/v2/auth',
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

result = RestClient.post 'http://localhost:4928/api/v2/auth',
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

r = requests.post('http://localhost:4928/api/v2/auth', headers = headers)

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
    $response = $client->request('POST','http://localhost:4928/api/v2/auth', array(
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
URL obj = new URL("http://localhost:4928/api/v2/auth");
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
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v2/auth", data)
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
 
</aside>

## get__oauth

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/oauth?code=string \
  -H 'Accept: application/json'

```

```http
GET http://localhost:4928/api/v2/oauth?code=string HTTP/1.1
Host: localhost:4928
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://localhost:4928/api/v2/oauth?code=string',
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

result = RestClient.get 'http://localhost:4928/api/v2/oauth',
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

r = requests.get('http://localhost:4928/api/v2/oauth', params={
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
    $response = $client->request('GET','http://localhost:4928/api/v2/oauth', array(
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
URL obj = new URL("http://localhost:4928/api/v2/oauth?code=string");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/oauth", data)
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
 
</aside>

<h1 id="yield-dance-api-market">Market</h1>

## get__market_assets_{asset_type}

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/market/assets/{asset_type} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/market/assets/{asset_type} HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/market/assets/{asset_type}',
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

result = RestClient.get 'http://localhost:4928/api/v2/market/assets/{asset_type}',
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

r = requests.get('http://localhost:4928/api/v2/market/assets/{asset_type}', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/market/assets/{asset_type}', array(
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
URL obj = new URL("http://localhost:4928/api/v2/market/assets/{asset_type}");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/market/assets/{asset_type}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /market/assets/{asset_type}`

return asset price

<h3 id="get__market_assets_{asset_type}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|asset_type|path|string|true|asset type:[eth,btc]|

> Example responses

> 400 Response

```json
{
  "code": 0,
  "data": null,
  "msg": "string"
}
```

<h3 id="get__market_assets_{asset_type}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

<h1 id="yield-dance-api-order">Order</h1>

## get__orders

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/orders \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/orders HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/orders',
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

result = RestClient.get 'http://localhost:4928/api/v2/orders',
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

r = requests.get('http://localhost:4928/api/v2/orders', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/orders', array(
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
URL obj = new URL("http://localhost:4928/api/v2/orders");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/orders", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /orders`

return a order list

<h3 id="get__orders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|round_status|query|string|false|status of round|
|page_current|query|integer|false|current page index|
|page_size|query|integer|false|size of page|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "amount": "string",
      "apy_real": "string",
      "clearing_amount": "string",
      "clearing_asset_id": "string",
      "created_at": "string",
      "fraction_amount": "string",
      "fraction_asset_id": "string",
      "insurances": [
        {
          "compensation_amount": "string",
          "compensation_asset_id": "string",
          "compensation_price": "string",
          "description": "string",
          "exercised": true,
          "id": 0,
          "label": "string",
          "type": "string"
        }
      ],
      "mixin_user_id": "string",
      "mixin_user_name": "string",
      "oid": "string",
      "premium_amount": "string",
      "premium_asset_id": "string",
      "refund_amount": "string",
      "rid": "string",
      "round": {
        "apy_max": "string",
        "apy_min": "string",
        "clearing_asset_id": "string",
        "clearing_at": "string",
        "created_at": "string",
        "exercised": true,
        "expiry": "string",
        "funding_asset_id": "string",
        "funding_end_at": "string",
        "hide": true,
        "insurance_enable": true,
        "max_fund": "string",
        "min_fund": "string",
        "rid": "string",
        "status": "string",
        "strike": "string",
        "updated_at": "string",
        "vault_type": "string"
      },
      "underlying_asset_id": "string",
      "underlying_price": "string",
      "updated_at": "string"
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

<h3 id="get__orders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Order item info|[ListOrderResponse](#schemalistorderresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## post__orders

> Code samples

```shell
# You can also use wget
curl -X POST http://localhost:4928/api/v2/orders \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
POST http://localhost:4928/api/v2/orders HTTP/1.1
Host: localhost:4928
Content-Type: application/json
Accept: application/json
Authorization: string

```

```javascript
const inputBody = '{
  "order_amount": "string",
  "rid": "string"
}';
const headers = {
  'Content-Type':'application/json',
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/orders',
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

result = RestClient.post 'http://localhost:4928/api/v2/orders',
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

r = requests.post('http://localhost:4928/api/v2/orders', headers = headers)

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
    $response = $client->request('POST','http://localhost:4928/api/v2/orders', array(
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
URL obj = new URL("http://localhost:4928/api/v2/orders");
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
    req, err := http.NewRequest("POST", "http://localhost:4928/api/v2/orders", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`POST /orders`

submit a order to round

> Body parameter

```json
{
  "order_amount": "string",
  "rid": "string"
}
```

<h3 id="post__orders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|body|body|[OrderReq](#schemaorderreq)|true|Order info|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "mixin_pay_url": "string",
    "mixin_transfer_trace_id": "string",
    "oid": "string",
    "order_amount": "string",
    "rid": "string",
    "status": "string"
  },
  "msg": "string"
}
```

<h3 id="post__orders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Order created info|[CreateOrderResponse](#schemacreateorderresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## get__orders_{oid}

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/orders/{oid} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/orders/{oid} HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/orders/{oid}',
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

result = RestClient.get 'http://localhost:4928/api/v2/orders/{oid}',
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

r = requests.get('http://localhost:4928/api/v2/orders/{oid}', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/orders/{oid}', array(
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
URL obj = new URL("http://localhost:4928/api/v2/orders/{oid}");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/orders/{oid}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /orders/{oid}`

return a order

<h3 id="get__orders_{oid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|oid|path|string|true|Order id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "amount": "string",
    "apy_real": "string",
    "clearing_amount": "string",
    "clearing_asset_id": "string",
    "created_at": "string",
    "fraction_amount": "string",
    "fraction_asset_id": "string",
    "insurances": [
      {
        "compensation_amount": "string",
        "compensation_asset_id": "string",
        "compensation_price": "string",
        "description": "string",
        "exercised": true,
        "id": 0,
        "label": "string",
        "type": "string"
      }
    ],
    "mixin_user_id": "string",
    "mixin_user_name": "string",
    "oid": "string",
    "premium_amount": "string",
    "premium_asset_id": "string",
    "refund_amount": "string",
    "rid": "string",
    "round": {
      "apy_max": "string",
      "apy_min": "string",
      "clearing_asset_id": "string",
      "clearing_at": "string",
      "created_at": "string",
      "exercised": true,
      "expiry": "string",
      "funding_asset_id": "string",
      "funding_end_at": "string",
      "hide": true,
      "insurance_enable": true,
      "max_fund": "string",
      "min_fund": "string",
      "rid": "string",
      "status": "string",
      "strike": "string",
      "updated_at": "string",
      "vault_type": "string"
    },
    "underlying_asset_id": "string",
    "underlying_price": "string",
    "updated_at": "string"
  },
  "msg": "string"
}
```

<h3 id="get__orders_{oid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Order item|[GetOrderResponse](#schemagetorderresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

<h1 id="yield-dance-api-round">Round</h1>

## get__rounds

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/rounds \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/rounds HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/rounds',
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

result = RestClient.get 'http://localhost:4928/api/v2/rounds',
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

r = requests.get('http://localhost:4928/api/v2/rounds', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/rounds', array(
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
URL obj = new URL("http://localhost:4928/api/v2/rounds");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/rounds", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /rounds`

Get a round list

<h3 id="get__rounds-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|vault_type|query|string|false|Type of vault|
|hide|query|boolean|false|hide state of round [true, false]|
|status|query|string|false|Status of round|
|Authorization|header|string|true|Authorization|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": [
    {
      "insurances": [
        {
          "compensation_amount": "string",
          "compensation_asset_id": "string",
          "compensation_price": "string",
          "description": "string",
          "exercised": true,
          "id": 0,
          "label": "string",
          "type": "string"
        }
      ],
      "round_info": {
        "apy_max": "string",
        "apy_min": "string",
        "clearing_asset_id": "string",
        "clearing_at": "string",
        "created_at": "string",
        "exercised": true,
        "expiry": "string",
        "funding_asset_id": "string",
        "funding_end_at": "string",
        "hide": true,
        "insurance_enable": true,
        "max_fund": "string",
        "min_fund": "string",
        "rid": "string",
        "status": "string",
        "strike": "string",
        "updated_at": "string",
        "vault_type": "string"
      }
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

<h3 id="get__rounds-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|List of round item wrapped in common response|[ListRoundSimpleResponse](#schemalistroundsimpleresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

## get__rounds_{rid}

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/rounds/{rid} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/rounds/{rid} HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/rounds/{rid}',
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

result = RestClient.get 'http://localhost:4928/api/v2/rounds/{rid}',
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

r = requests.get('http://localhost:4928/api/v2/rounds/{rid}', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/rounds/{rid}', array(
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
URL obj = new URL("http://localhost:4928/api/v2/rounds/{rid}");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/rounds/{rid}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /rounds/{rid}`

Get a round item

<h3 id="get__rounds_{rid}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|rid|path|string|true|round id|
|Authorization|header|string|true|Authorization|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "clearing_info": {
      "clearing_amount": "string",
      "clearing_asset_id": "string",
      "clearing_draft_amount": "string",
      "clearing_users": "string",
      "exercised": true,
      "underlying_asset_id": "string",
      "underlying_price": "string"
    },
    "fund_info": {
      "apy_real": "string",
      "min_unit": "string",
      "order_recv_amount": "string",
      "order_recv_users": "string",
      "outbound_asset_id": "string",
      "premium_amount": "string"
    },
    "insurances": [
      {
        "compensation_amount": "string",
        "compensation_asset_id": "string",
        "compensation_price": "string",
        "description": "string",
        "exercised": true,
        "id": 0,
        "label": "string",
        "type": "string"
      }
    ],
    "outbound_info": {
      "amount": "string",
      "fraction_amount": "string",
      "fraction_asset_id": "string",
      "fraction_users": "string",
      "premium_amount": "string",
      "premium_asset_id": "string",
      "premium_users": "string",
      "refund_amount": "string",
      "refund_asset_id": "string",
      "refund_users": "string"
    },
    "round_activities": [
      {
        "activity_type": "string",
        "amount": "string",
        "asset_id": "string",
        "created_at": "string",
        "mixin_user_id": "string",
        "mixin_user_name": "string",
        "oid": "string",
        "remark": "string",
        "status": "string",
        "trace_id": "string"
      }
    ],
    "round_info": {
      "apy_max": "string",
      "apy_min": "string",
      "clearing_asset_id": "string",
      "clearing_at": "string",
      "created_at": "string",
      "exercised": true,
      "expiry": "string",
      "funding_asset_id": "string",
      "funding_end_at": "string",
      "hide": true,
      "insurance_enable": true,
      "max_fund": "string",
      "min_fund": "string",
      "rid": "string",
      "status": "string",
      "strike": "string",
      "updated_at": "string",
      "vault_type": "string"
    }
  },
  "msg": "string"
}
```

<h3 id="get__rounds_{rid}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Round item wrapped in common response|[CommonRoundResponse](#schemacommonroundresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

<h1 id="yield-dance-api-transfer">Transfer</h1>

## get__transfer_{trace_id}

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/transfer/{trace_id} \
  -H 'Accept: application/json' \
  -H 'Authorization: string'

```

```http
GET http://localhost:4928/api/v2/transfer/{trace_id} HTTP/1.1
Host: localhost:4928
Accept: application/json
Authorization: string

```

```javascript

const headers = {
  'Accept':'application/json',
  'Authorization':'string'
};

fetch('http://localhost:4928/api/v2/transfer/{trace_id}',
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

result = RestClient.get 'http://localhost:4928/api/v2/transfer/{trace_id}',
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

r = requests.get('http://localhost:4928/api/v2/transfer/{trace_id}', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/transfer/{trace_id}', array(
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
URL obj = new URL("http://localhost:4928/api/v2/transfer/{trace_id}");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/transfer/{trace_id}", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /transfer/{trace_id}`

return a transfer

<h3 id="get__transfer_{trace_id}-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|Authorization|header|string|true|Authorization|
|trace_id|query|string|false|transfer trace id|

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "activity_type": "string",
    "amount": "string",
    "asset_id": "string",
    "created_at": "string",
    "mixin_user_id": "string",
    "mixin_user_name": "string",
    "oid": "string",
    "remark": "string",
    "status": "string",
    "trace_id": "string"
  },
  "msg": "string"
}
```

<h3 id="get__transfer_{trace_id}-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|transfer info|[GetTransferResponse](#schemagettransferresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

<h1 id="yield-dance-api-user">User</h1>

## get__user_me

> Code samples

```shell
# You can also use wget
curl -X GET http://localhost:4928/api/v2/user/me \
  -H 'Accept: application/json'

```

```http
GET http://localhost:4928/api/v2/user/me HTTP/1.1
Host: localhost:4928
Accept: application/json

```

```javascript

const headers = {
  'Accept':'application/json'
};

fetch('http://localhost:4928/api/v2/user/me',
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

result = RestClient.get 'http://localhost:4928/api/v2/user/me',
  params: {
  }, headers: headers

p JSON.parse(result)

```

```python
import requests
headers = {
  'Accept': 'application/json'
}

r = requests.get('http://localhost:4928/api/v2/user/me', headers = headers)

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
    $response = $client->request('GET','http://localhost:4928/api/v2/user/me', array(
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
URL obj = new URL("http://localhost:4928/api/v2/user/me");
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
    req, err := http.NewRequest("GET", "http://localhost:4928/api/v2/user/me", data)
    req.Header = headers

    client := &http.Client{}
    resp, err := client.Do(req)
    // ...
}

```

`GET /user/me`

get user info

> Example responses

> 200 Response

```json
{
  "code": 0,
  "data": {
    "mixin_user_id": "string",
    "mixin_user_number": "string",
    "nickname": "string"
  },
  "msg": "string"
}
```

<h3 id="get__user_me-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|return user info|[UserResponse](#schemauserresponse)|
|400|[Bad Request](https://tools.ietf.org/html/rfc7231#section-6.5.1)|Common response|[commonResponse](#schemacommonresponse)|

<aside class="success">
 
</aside>

# Schemas

<h2 id="tocS_Activity">Activity</h2>

<a id="schemaactivity"></a>
<a id="schema_Activity"></a>
<a id="tocSactivity"></a>
<a id="tocsactivity"></a>

```json
{
  "activity_type": "string",
  "amount": "string",
  "asset_id": "string",
  "created_at": "string",
  "mixin_user_id": "string",
  "mixin_user_name": "string",
  "oid": "string",
  "remark": "string",
  "status": "string",
  "trace_id": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|activity_type|string|false|none|类型|
|amount|string|false|none|金额|
|asset_id|string|false|none|资产类型|
|created_at|string|false|none|时间|
|mixin_user_id|string|false|none|mixin id|
|mixin_user_name|string|false|none|昵称|
|oid|string|false|none|关联的订单id|
|remark|string|false|none|出错信息|
|status|string|false|none|转账状态|
|trace_id|string|false|none|uuid|

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

<h2 id="tocS_CommonInsuranceResponse">CommonInsuranceResponse</h2>

<a id="schemacommoninsuranceresponse"></a>
<a id="schema_CommonInsuranceResponse"></a>
<a id="tocScommoninsuranceresponse"></a>
<a id="tocscommoninsuranceresponse"></a>

```json
{
  "code": 0,
  "data": {
    "amount": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[RoundInsuranceResp](#schemaroundinsuranceresp)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_CommonRoundResponse">CommonRoundResponse</h2>

<a id="schemacommonroundresponse"></a>
<a id="schema_CommonRoundResponse"></a>
<a id="tocScommonroundresponse"></a>
<a id="tocscommonroundresponse"></a>

```json
{
  "code": 0,
  "data": {
    "clearing_info": {
      "clearing_amount": "string",
      "clearing_asset_id": "string",
      "clearing_draft_amount": "string",
      "clearing_users": "string",
      "exercised": true,
      "underlying_asset_id": "string",
      "underlying_price": "string"
    },
    "fund_info": {
      "apy_real": "string",
      "min_unit": "string",
      "order_recv_amount": "string",
      "order_recv_users": "string",
      "outbound_asset_id": "string",
      "premium_amount": "string"
    },
    "insurances": [
      {
        "compensation_amount": "string",
        "compensation_asset_id": "string",
        "compensation_price": "string",
        "description": "string",
        "exercised": true,
        "id": 0,
        "label": "string",
        "type": "string"
      }
    ],
    "outbound_info": {
      "amount": "string",
      "fraction_amount": "string",
      "fraction_asset_id": "string",
      "fraction_users": "string",
      "premium_amount": "string",
      "premium_asset_id": "string",
      "premium_users": "string",
      "refund_amount": "string",
      "refund_asset_id": "string",
      "refund_users": "string"
    },
    "round_activities": [
      {
        "activity_type": "string",
        "amount": "string",
        "asset_id": "string",
        "created_at": "string",
        "mixin_user_id": "string",
        "mixin_user_name": "string",
        "oid": "string",
        "remark": "string",
        "status": "string",
        "trace_id": "string"
      }
    ],
    "round_info": {
      "apy_max": "string",
      "apy_min": "string",
      "clearing_asset_id": "string",
      "clearing_at": "string",
      "created_at": "string",
      "exercised": true,
      "expiry": "string",
      "funding_asset_id": "string",
      "funding_end_at": "string",
      "hide": true,
      "insurance_enable": true,
      "max_fund": "string",
      "min_fund": "string",
      "rid": "string",
      "status": "string",
      "strike": "string",
      "updated_at": "string",
      "vault_type": "string"
    }
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[RoundItem](#schemarounditem)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_CreateOrderResponse">CreateOrderResponse</h2>

<a id="schemacreateorderresponse"></a>
<a id="schema_CreateOrderResponse"></a>
<a id="tocScreateorderresponse"></a>
<a id="tocscreateorderresponse"></a>

```json
{
  "code": 0,
  "data": {
    "mixin_pay_url": "string",
    "mixin_transfer_trace_id": "string",
    "oid": "string",
    "order_amount": "string",
    "rid": "string",
    "status": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[OrderResp](#schemaorderresp)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_GetOrderResponse">GetOrderResponse</h2>

<a id="schemagetorderresponse"></a>
<a id="schema_GetOrderResponse"></a>
<a id="tocSgetorderresponse"></a>
<a id="tocsgetorderresponse"></a>

```json
{
  "code": 0,
  "data": {
    "amount": "string",
    "apy_real": "string",
    "clearing_amount": "string",
    "clearing_asset_id": "string",
    "created_at": "string",
    "fraction_amount": "string",
    "fraction_asset_id": "string",
    "insurances": [
      {
        "compensation_amount": "string",
        "compensation_asset_id": "string",
        "compensation_price": "string",
        "description": "string",
        "exercised": true,
        "id": 0,
        "label": "string",
        "type": "string"
      }
    ],
    "mixin_user_id": "string",
    "mixin_user_name": "string",
    "oid": "string",
    "premium_amount": "string",
    "premium_asset_id": "string",
    "refund_amount": "string",
    "rid": "string",
    "round": {
      "apy_max": "string",
      "apy_min": "string",
      "clearing_asset_id": "string",
      "clearing_at": "string",
      "created_at": "string",
      "exercised": true,
      "expiry": "string",
      "funding_asset_id": "string",
      "funding_end_at": "string",
      "hide": true,
      "insurance_enable": true,
      "max_fund": "string",
      "min_fund": "string",
      "rid": "string",
      "status": "string",
      "strike": "string",
      "updated_at": "string",
      "vault_type": "string"
    },
    "underlying_asset_id": "string",
    "underlying_price": "string",
    "updated_at": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[OrderItem](#schemaorderitem)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_GetTransferResponse">GetTransferResponse</h2>

<a id="schemagettransferresponse"></a>
<a id="schema_GetTransferResponse"></a>
<a id="tocSgettransferresponse"></a>
<a id="tocsgettransferresponse"></a>

```json
{
  "code": 0,
  "data": {
    "activity_type": "string",
    "amount": "string",
    "asset_id": "string",
    "created_at": "string",
    "mixin_user_id": "string",
    "mixin_user_name": "string",
    "oid": "string",
    "remark": "string",
    "status": "string",
    "trace_id": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[Activity](#schemaactivity)|false|none|none|
|msg|string|false|none|none|

<h2 id="tocS_Insurance">Insurance</h2>

<a id="schemainsurance"></a>
<a id="schema_Insurance"></a>
<a id="tocSinsurance"></a>
<a id="tocsinsurance"></a>

```json
{
  "compensation_amount": "string",
  "compensation_asset_id": "string",
  "compensation_price": "string",
  "description": "string",
  "exercised": true,
  "id": 0,
  "label": "string",
  "type": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|compensation_amount|string|false|none|赔付金额|
|compensation_asset_id|string|false|none|赔付资产|
|compensation_price|string|false|none|赔付格价|
|description|string|false|none|赔付描述|
|exercised|boolean|false|none|赔付状态|
|id|integer|false|none|insurance id|
|label|string|false|none|赔付标签|
|type|string|false|none|赔付类型|

<h2 id="tocS_ListActivityResponse">ListActivityResponse</h2>

<a id="schemalistactivityresponse"></a>
<a id="schema_ListActivityResponse"></a>
<a id="tocSlistactivityresponse"></a>
<a id="tocslistactivityresponse"></a>

```json
{
  "code": 0,
  "data": [
    {
      "activity_type": "string",
      "amount": "string",
      "asset_id": "string",
      "created_at": "string",
      "mixin_user_id": "string",
      "mixin_user_name": "string",
      "oid": "string",
      "remark": "string",
      "status": "string",
      "trace_id": "string"
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
|data|[[Activity](#schemaactivity)]|false|none|none|
|msg|string|false|none|none|
|pagination|[Pagination](#schemapagination)|false|none|none|

<h2 id="tocS_ListOrderResponse">ListOrderResponse</h2>

<a id="schemalistorderresponse"></a>
<a id="schema_ListOrderResponse"></a>
<a id="tocSlistorderresponse"></a>
<a id="tocslistorderresponse"></a>

```json
{
  "code": 0,
  "data": [
    {
      "amount": "string",
      "apy_real": "string",
      "clearing_amount": "string",
      "clearing_asset_id": "string",
      "created_at": "string",
      "fraction_amount": "string",
      "fraction_asset_id": "string",
      "insurances": [
        {
          "compensation_amount": "string",
          "compensation_asset_id": "string",
          "compensation_price": "string",
          "description": "string",
          "exercised": true,
          "id": 0,
          "label": "string",
          "type": "string"
        }
      ],
      "mixin_user_id": "string",
      "mixin_user_name": "string",
      "oid": "string",
      "premium_amount": "string",
      "premium_asset_id": "string",
      "refund_amount": "string",
      "rid": "string",
      "round": {
        "apy_max": "string",
        "apy_min": "string",
        "clearing_asset_id": "string",
        "clearing_at": "string",
        "created_at": "string",
        "exercised": true,
        "expiry": "string",
        "funding_asset_id": "string",
        "funding_end_at": "string",
        "hide": true,
        "insurance_enable": true,
        "max_fund": "string",
        "min_fund": "string",
        "rid": "string",
        "status": "string",
        "strike": "string",
        "updated_at": "string",
        "vault_type": "string"
      },
      "underlying_asset_id": "string",
      "underlying_price": "string",
      "updated_at": "string"
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
|data|[[OrderItem](#schemaorderitem)]|false|none|none|
|msg|string|false|none|none|
|pagination|[Pagination](#schemapagination)|false|none|none|

<h2 id="tocS_ListRoundResponse">ListRoundResponse</h2>

<a id="schemalistroundresponse"></a>
<a id="schema_ListRoundResponse"></a>
<a id="tocSlistroundresponse"></a>
<a id="tocslistroundresponse"></a>

```json
{
  "code": 0,
  "data": [
    {
      "clearing_info": {
        "clearing_amount": "string",
        "clearing_asset_id": "string",
        "clearing_draft_amount": "string",
        "clearing_users": "string",
        "exercised": true,
        "underlying_asset_id": "string",
        "underlying_price": "string"
      },
      "fund_info": {
        "apy_real": "string",
        "min_unit": "string",
        "order_recv_amount": "string",
        "order_recv_users": "string",
        "outbound_asset_id": "string",
        "premium_amount": "string"
      },
      "insurances": [
        {
          "compensation_amount": "string",
          "compensation_asset_id": "string",
          "compensation_price": "string",
          "description": "string",
          "exercised": true,
          "id": 0,
          "label": "string",
          "type": "string"
        }
      ],
      "outbound_info": {
        "amount": "string",
        "fraction_amount": "string",
        "fraction_asset_id": "string",
        "fraction_users": "string",
        "premium_amount": "string",
        "premium_asset_id": "string",
        "premium_users": "string",
        "refund_amount": "string",
        "refund_asset_id": "string",
        "refund_users": "string"
      },
      "round_activities": [
        {
          "activity_type": "string",
          "amount": "string",
          "asset_id": "string",
          "created_at": "string",
          "mixin_user_id": "string",
          "mixin_user_name": "string",
          "oid": "string",
          "remark": "string",
          "status": "string",
          "trace_id": "string"
        }
      ],
      "round_info": {
        "apy_max": "string",
        "apy_min": "string",
        "clearing_asset_id": "string",
        "clearing_at": "string",
        "created_at": "string",
        "exercised": true,
        "expiry": "string",
        "funding_asset_id": "string",
        "funding_end_at": "string",
        "hide": true,
        "insurance_enable": true,
        "max_fund": "string",
        "min_fund": "string",
        "rid": "string",
        "status": "string",
        "strike": "string",
        "updated_at": "string",
        "vault_type": "string"
      }
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
|data|[[RoundItem](#schemarounditem)]|false|none|none|
|msg|string|false|none|none|
|pagination|[Pagination](#schemapagination)|false|none|none|

<h2 id="tocS_ListRoundSimpleResponse">ListRoundSimpleResponse</h2>

<a id="schemalistroundsimpleresponse"></a>
<a id="schema_ListRoundSimpleResponse"></a>
<a id="tocSlistroundsimpleresponse"></a>
<a id="tocslistroundsimpleresponse"></a>

```json
{
  "code": 0,
  "data": [
    {
      "insurances": [
        {
          "compensation_amount": "string",
          "compensation_asset_id": "string",
          "compensation_price": "string",
          "description": "string",
          "exercised": true,
          "id": 0,
          "label": "string",
          "type": "string"
        }
      ],
      "round_info": {
        "apy_max": "string",
        "apy_min": "string",
        "clearing_asset_id": "string",
        "clearing_at": "string",
        "created_at": "string",
        "exercised": true,
        "expiry": "string",
        "funding_asset_id": "string",
        "funding_end_at": "string",
        "hide": true,
        "insurance_enable": true,
        "max_fund": "string",
        "min_fund": "string",
        "rid": "string",
        "status": "string",
        "strike": "string",
        "updated_at": "string",
        "vault_type": "string"
      }
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
|data|[[service.RoundInfoWithInsurance](#schemaservice.roundinfowithinsurance)]|false|none|none|
|msg|string|false|none|none|
|pagination|[Pagination](#schemapagination)|false|none|none|

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

<h2 id="tocS_OrderItem">OrderItem</h2>

<a id="schemaorderitem"></a>
<a id="schema_OrderItem"></a>
<a id="tocSorderitem"></a>
<a id="tocsorderitem"></a>

```json
{
  "amount": "string",
  "apy_real": "string",
  "clearing_amount": "string",
  "clearing_asset_id": "string",
  "created_at": "string",
  "fraction_amount": "string",
  "fraction_asset_id": "string",
  "insurances": [
    {
      "compensation_amount": "string",
      "compensation_asset_id": "string",
      "compensation_price": "string",
      "description": "string",
      "exercised": true,
      "id": 0,
      "label": "string",
      "type": "string"
    }
  ],
  "mixin_user_id": "string",
  "mixin_user_name": "string",
  "oid": "string",
  "premium_amount": "string",
  "premium_asset_id": "string",
  "refund_amount": "string",
  "rid": "string",
  "round": {
    "apy_max": "string",
    "apy_min": "string",
    "clearing_asset_id": "string",
    "clearing_at": "string",
    "created_at": "string",
    "exercised": true,
    "expiry": "string",
    "funding_asset_id": "string",
    "funding_end_at": "string",
    "hide": true,
    "insurance_enable": true,
    "max_fund": "string",
    "min_fund": "string",
    "rid": "string",
    "status": "string",
    "strike": "string",
    "updated_at": "string",
    "vault_type": "string"
  },
  "underlying_asset_id": "string",
  "underlying_price": "string",
  "updated_at": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|string|false|none|购币金(用户实际转账购币金)|
|apy_real|string|false|none|权利金年化收益率|
|clearing_amount|string|false|none|结算数量(如:C端BTC数量)|
|clearing_asset_id|string|false|none|结算类型|
|created_at|string|false|none|none|
|fraction_amount|string|false|none|资金修剪|
|fraction_asset_id|string|false|none|货币：USDT or BTC or ETH|
|insurances|[[Insurance](#schemainsurance)]|false|none|赔付信息|
|mixin_user_id|string|false|none|none|
|mixin_user_name|string|false|none|昵称|
|oid|string|false|none|none|
|premium_amount|string|false|none|权利金收益|
|premium_asset_id|string|false|none|标的资产: USDT or BTC or ETH|
|refund_amount|string|false|none|退回购币金|
|rid|string|false|none|none|
|round|[RoundInfo](#schemaroundinfo)|false|none|Round信息|
|underlying_asset_id|string|false|none|标的资产：USDT or BTC or ETH|
|underlying_price|string|false|none|标的价格(报价)|
|updated_at|string|false|none|none|

<h2 id="tocS_OrderReq">OrderReq</h2>

<a id="schemaorderreq"></a>
<a id="schema_OrderReq"></a>
<a id="tocSorderreq"></a>
<a id="tocsorderreq"></a>

```json
{
  "order_amount": "string",
  "rid": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|order_amount|string|true|none|购买额|
|rid|string|true|none|Round ID|

<h2 id="tocS_OrderResp">OrderResp</h2>

<a id="schemaorderresp"></a>
<a id="schema_OrderResp"></a>
<a id="tocSorderresp"></a>
<a id="tocsorderresp"></a>

```json
{
  "mixin_pay_url": "string",
  "mixin_transfer_trace_id": "string",
  "oid": "string",
  "order_amount": "string",
  "rid": "string",
  "status": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|mixin_pay_url|string|false|none|转账状态|
|mixin_transfer_trace_id|string|false|none|本次订单trace_id|
|oid|string|true|none|none|
|order_amount|string|true|none|购买额|
|rid|string|true|none|Round ID|
|status|string|false|none|转账状态|

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

<h2 id="tocS_RoundClearingInfo">RoundClearingInfo</h2>

<a id="schemaroundclearinginfo"></a>
<a id="schema_RoundClearingInfo"></a>
<a id="tocSroundclearinginfo"></a>
<a id="tocsroundclearinginfo"></a>

```json
{
  "clearing_amount": "string",
  "clearing_asset_id": "string",
  "clearing_draft_amount": "string",
  "clearing_users": "string",
  "exercised": true,
  "underlying_asset_id": "string",
  "underlying_price": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|clearing_amount|string|false|none|结算执行结果|
|clearing_asset_id|string|false|none|标的结算：USDT or BTC or ETH|
|clearing_draft_amount|string|false|none|拟定发放金额(发放金额)|
|clearing_users|string|false|none|发放成功人数|
|exercised|boolean|false|none|结算信息|
|underlying_asset_id|string|false|none|标的资产：USDT or BTC or ETH|
|underlying_price|string|false|none|标的价格(报价)|

<h2 id="tocS_RoundFundInfo">RoundFundInfo</h2>

<a id="schemaroundfundinfo"></a>
<a id="schema_RoundFundInfo"></a>
<a id="tocSroundfundinfo"></a>
<a id="tocsroundfundinfo"></a>

```json
{
  "apy_real": "string",
  "min_unit": "string",
  "order_recv_amount": "string",
  "order_recv_users": "string",
  "outbound_asset_id": "string",
  "premium_amount": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|apy_real|string|false|none|年化收益率|
|min_unit|string|false|none|发车最小单位|
|order_recv_amount|string|false|none|已募资金额|
|order_recv_users|string|false|none|参与人数|
|outbound_asset_id|string|false|none|发车发放资产：无 or USDT or BTC or ETH|
|premium_amount|string|false|none|发放金额|

<h2 id="tocS_RoundInfo">RoundInfo</h2>

<a id="schemaroundinfo"></a>
<a id="schema_RoundInfo"></a>
<a id="tocSroundinfo"></a>
<a id="tocsroundinfo"></a>

```json
{
  "apy_max": "string",
  "apy_min": "string",
  "clearing_asset_id": "string",
  "clearing_at": "string",
  "created_at": "string",
  "exercised": true,
  "expiry": "string",
  "funding_asset_id": "string",
  "funding_end_at": "string",
  "hide": true,
  "insurance_enable": true,
  "max_fund": "string",
  "min_fund": "string",
  "rid": "string",
  "status": "string",
  "strike": "string",
  "updated_at": "string",
  "vault_type": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|apy_max|string|false|none|最大年化收益率|
|apy_min|string|false|none|最小年化收益率|
|clearing_asset_id|string|false|none|结算货币：USDT or BTC or ETH|
|clearing_at|string|false|none|结算时间|
|created_at|string|false|none|募资开始时间|
|exercised|boolean|false|none|行权状态|
|expiry|string|false|none|(C端显示)到期时间|
|funding_asset_id|string|false|none|募资货币：USDT or BTC or ETH|
|funding_end_at|string|false|none|FundingStartAt  string `json:"funding_start_at"`  //使用created_at作为募资开始时间|
|hide|boolean|false|none|可见状态(是否隐藏该round)|
|insurance_enable|boolean|false|none|是否开启保险赔付|
|max_fund|string|false|none|最高募资金额|
|min_fund|string|false|none|最低募资金额|
|rid|string|false|none|round id|
|status|string|false|none|项目状态|
|strike|string|false|none|(C端显示)执行价格|
|updated_at|string|false|none|none|
|vault_type|string|false|none|Round类型|

<h2 id="tocS_RoundInsuranceReq">RoundInsuranceReq</h2>

<a id="schemaroundinsurancereq"></a>
<a id="schema_RoundInsuranceReq"></a>
<a id="tocSroundinsurancereq"></a>
<a id="tocsroundinsurancereq"></a>

```json
{
  "compensation_amount": "string",
  "compensation_asset_id": "string",
  "compensation_price": "string",
  "exercised": true,
  "id": 0,
  "operation": "string",
  "type": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|compensation_amount|string|false|none|赔付金额|
|compensation_asset_id|string|false|none|赔付资产|
|compensation_price|string|false|none|赔付格价|
|exercised|boolean|false|none|赔付状态|
|id|integer|false|none|insurance id|
|operation|string|false|none|操作类型|
|type|string|false|none|赔付类型|

<h2 id="tocS_RoundInsuranceResp">RoundInsuranceResp</h2>

<a id="schemaroundinsuranceresp"></a>
<a id="schema_RoundInsuranceResp"></a>
<a id="tocSroundinsuranceresp"></a>
<a id="tocsroundinsuranceresp"></a>

```json
{
  "amount": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|string|false|none|计算的赔付金额|

<h2 id="tocS_RoundItem">RoundItem</h2>

<a id="schemarounditem"></a>
<a id="schema_RoundItem"></a>
<a id="tocSrounditem"></a>
<a id="tocsrounditem"></a>

```json
{
  "clearing_info": {
    "clearing_amount": "string",
    "clearing_asset_id": "string",
    "clearing_draft_amount": "string",
    "clearing_users": "string",
    "exercised": true,
    "underlying_asset_id": "string",
    "underlying_price": "string"
  },
  "fund_info": {
    "apy_real": "string",
    "min_unit": "string",
    "order_recv_amount": "string",
    "order_recv_users": "string",
    "outbound_asset_id": "string",
    "premium_amount": "string"
  },
  "insurances": [
    {
      "compensation_amount": "string",
      "compensation_asset_id": "string",
      "compensation_price": "string",
      "description": "string",
      "exercised": true,
      "id": 0,
      "label": "string",
      "type": "string"
    }
  ],
  "outbound_info": {
    "amount": "string",
    "fraction_amount": "string",
    "fraction_asset_id": "string",
    "fraction_users": "string",
    "premium_amount": "string",
    "premium_asset_id": "string",
    "premium_users": "string",
    "refund_amount": "string",
    "refund_asset_id": "string",
    "refund_users": "string"
  },
  "round_activities": [
    {
      "activity_type": "string",
      "amount": "string",
      "asset_id": "string",
      "created_at": "string",
      "mixin_user_id": "string",
      "mixin_user_name": "string",
      "oid": "string",
      "remark": "string",
      "status": "string",
      "trace_id": "string"
    }
  ],
  "round_info": {
    "apy_max": "string",
    "apy_min": "string",
    "clearing_asset_id": "string",
    "clearing_at": "string",
    "created_at": "string",
    "exercised": true,
    "expiry": "string",
    "funding_asset_id": "string",
    "funding_end_at": "string",
    "hide": true,
    "insurance_enable": true,
    "max_fund": "string",
    "min_fund": "string",
    "rid": "string",
    "status": "string",
    "strike": "string",
    "updated_at": "string",
    "vault_type": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|clearing_info|[RoundClearingInfo](#schemaroundclearinginfo)|false|none|结算信息|
|fund_info|[RoundFundInfo](#schemaroundfundinfo)|false|none|发车信息(募资信息)|
|insurances|[[Insurance](#schemainsurance)]|false|none|保险信息|
|outbound_info|[RoundOutBoundInfo](#schemaroundoutboundinfo)|false|none|发车执行结果|
|round_activities|[[Activity](#schemaactivity)]|false|none|项目日志|
|round_info|[RoundInfo](#schemaroundinfo)|false|none|项目信息|

<h2 id="tocS_RoundOperationReq">RoundOperationReq</h2>

<a id="schemaroundoperationreq"></a>
<a id="schema_RoundOperationReq"></a>
<a id="tocSroundoperationreq"></a>
<a id="tocsroundoperationreq"></a>

```json
{
  "amount": "string",
  "asset_id": "string",
  "exercised": true,
  "insurance": {
    "compensation_amount": "string",
    "compensation_asset_id": "string",
    "compensation_price": "string",
    "description": "string",
    "exercised": true,
    "id": 0,
    "label": "string",
    "type": "string"
  },
  "min_unit": "string",
  "operation": "string",
  "underlying_price": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|string|false|none|1. 发车发放利息 2. 结算金额|
|asset_id|string|false|none|相应操作的币种|
|exercised|boolean|false|none|是否行权|
|insurance|[Insurance](#schemainsurance)|false|none|none|
|min_unit|string|false|none|发车与做市商结算最小单位|
|operation|string|false|none|操作类型|
|underlying_price|string|false|none|结算时管理员所填的报价|

<h2 id="tocS_RoundOutBoundInfo">RoundOutBoundInfo</h2>

<a id="schemaroundoutboundinfo"></a>
<a id="schema_RoundOutBoundInfo"></a>
<a id="tocSroundoutboundinfo"></a>
<a id="tocsroundoutboundinfo"></a>

```json
{
  "amount": "string",
  "fraction_amount": "string",
  "fraction_asset_id": "string",
  "fraction_users": "string",
  "premium_amount": "string",
  "premium_asset_id": "string",
  "premium_users": "string",
  "refund_amount": "string",
  "refund_asset_id": "string",
  "refund_users": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|amount|string|false|none|发车金额|
|fraction_amount|string|false|none|资金修剪金额|
|fraction_asset_id|string|false|none|货币：USDT or BTC or ETH|
|fraction_users|string|false|none|资金修剪人数|
|premium_amount|string|false|none|发放成功金额|
|premium_asset_id|string|false|none|货币：USDT or BTC or ETH|
|premium_users|string|false|none|发放成功人数|
|refund_amount|string|false|none|退款成功金额|
|refund_asset_id|string|false|none|货币：USDT or BTC or ETH|
|refund_users|string|false|none|退款成功人数|

<h2 id="tocS_RoundRequest">RoundRequest</h2>

<a id="schemaroundrequest"></a>
<a id="schema_RoundRequest"></a>
<a id="tocSroundrequest"></a>
<a id="tocsroundrequest"></a>

```json
{
  "apy_max": "string",
  "apy_min": "string",
  "clearing_asset_id": "string",
  "clearing_at": "string",
  "expiry": "string",
  "funding_asset_id": "string",
  "funding_end_at": "string",
  "funding_start_at": "string",
  "hide": true,
  "insurance_enable": true,
  "insurances": [
    {
      "description": "string",
      "id": 0,
      "label": "string"
    }
  ],
  "max_fund": "string",
  "min_fund": "string",
  "strike": "string",
  "vault_type": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|apy_max|string|true|none|最大年化收益率|
|apy_min|string|true|none|最小年化收益率|
|clearing_asset_id|string|true|none|结算货币：USDT or BTC or ETH|
|clearing_at|string|true|none|结算时间|
|expiry|string|true|none|(C端显示)到期时间|
|funding_asset_id|string|true|none|募资货币：USDT or BTC or ETH|
|funding_end_at|string|true|none|发车时间|
|funding_start_at|string|false|none|募资开始时间|
|hide|boolean|true|none|可见状态(是否隐藏该round)|
|insurance_enable|boolean|true|none|是否开启保险赔付|
|insurances|[[insurance](#schemainsurance)]|false|none|保险赔付组合|
|max_fund|string|true|none|最高募资金额|
|min_fund|string|true|none|最低募资金额|
|strike|string|true|none|(C端显示)执行价格|
|vault_type|string|true|none|Round类型|

<h2 id="tocS_User">User</h2>

<a id="schemauser"></a>
<a id="schema_User"></a>
<a id="tocSuser"></a>
<a id="tocsuser"></a>

```json
{
  "mixin_user_id": "string",
  "mixin_user_number": "string",
  "nickname": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|mixin_user_id|string|false|none|none|
|mixin_user_number|string|false|none|none|
|nickname|string|false|none|none|

<h2 id="tocS_UserResponse">UserResponse</h2>

<a id="schemauserresponse"></a>
<a id="schema_UserResponse"></a>
<a id="tocSuserresponse"></a>
<a id="tocsuserresponse"></a>

```json
{
  "code": 0,
  "data": {
    "mixin_user_id": "string",
    "mixin_user_number": "string",
    "nickname": "string"
  },
  "msg": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|integer|false|none|none|
|data|[User](#schemauser)|false|none|none|
|msg|string|false|none|none|

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

<h2 id="tocS_insurance">insurance</h2>

<a id="schemainsurance"></a>
<a id="schema_insurance"></a>
<a id="tocSinsurance"></a>
<a id="tocsinsurance"></a>

```json
{
  "description": "string",
  "id": 0,
  "label": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|description|string|false|none|赔付描述|
|id|integer|false|none|insurance id|
|label|string|false|none|赔付标签|

<h2 id="tocS_service.RoundInfoWithInsurance">service.RoundInfoWithInsurance</h2>

<a id="schemaservice.roundinfowithinsurance"></a>
<a id="schema_service.RoundInfoWithInsurance"></a>
<a id="tocSservice.roundinfowithinsurance"></a>
<a id="tocsservice.roundinfowithinsurance"></a>

```json
{
  "insurances": [
    {
      "compensation_amount": "string",
      "compensation_asset_id": "string",
      "compensation_price": "string",
      "description": "string",
      "exercised": true,
      "id": 0,
      "label": "string",
      "type": "string"
    }
  ],
  "round_info": {
    "apy_max": "string",
    "apy_min": "string",
    "clearing_asset_id": "string",
    "clearing_at": "string",
    "created_at": "string",
    "exercised": true,
    "expiry": "string",
    "funding_asset_id": "string",
    "funding_end_at": "string",
    "hide": true,
    "insurance_enable": true,
    "max_fund": "string",
    "min_fund": "string",
    "rid": "string",
    "status": "string",
    "strike": "string",
    "updated_at": "string",
    "vault_type": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|insurances|[[Insurance](#schemainsurance)]|false|none|none|
|round_info|[RoundInfo](#schemaroundinfo)|false|none|none|

