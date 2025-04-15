---
icon: osi
---

# TruthWeb Open-Source API

#### **Welcome**

The TruthWeb Open-Source API allows developers to leverage the decentralized ecosystem of Pi cryptocurrency, enabling seamless integration into custom applications.

#### **Base URL**

All API endpoints are relative to the following base URL:

```url
https://api.truthweb.com/v1/
```

_Note_ : This is a placeholder URL. Replace it with your deployment URL once live.

#### **Authentication**

* **API Key** : Required for all requests.
* **Header** : Include `Authorization: Bearer <API_KEY>` in all requests.
* **Registration** : Obtain your API key by registering at the [TruthWeb Developer Portal ](https://developer.truthweb.com/).

#### **Endpoints**

**1. Retrieve User Profile**

**Endpoint** : `GET /profiles/{username}`\
Retrieve a user’s public profile information.

* **Path Parameters** :
  * `username` (string, required): The username of the user.
* **Headers** :
  * `Authorization: Bearer <API_KEY>`
* **Response** :

```json
{
  "status": "success",
  "data": {
    "username": "pioneer123",
    "display_name": "Pioneer John",
    "bio": "Pi enthusiast and developer",
    "created_at": "2025-03-05T10:00:00Z"
  }
}
```

* **Status Codes** :
  * `200 OK`: Profile retrieved.
  * `404 Not Found`: Username not found.
  * `401 Unauthorized`: Invalid API key.

***

**2. Check Pi Balance**

**Endpoint** : `GET /wallet/{username}/balance`\
Check a user’s Pi balance.

* **Path Parameters** :
  * `username` (string, required): The username of the user.
* **Headers** :
  * `Authorization: Bearer <API_KEY>`
* **Response** :

```json
{
  "status": "success",
  "data": {
    "username": "pioneer123",
    "balance_pi": 150.75,
    "updated_at": "2025-03-05T12:00:00Z"
  }
}
```

* **Status Codes** :
  * `200 OK`: Balance retrieved.
  * `404 Not Found`: User not found.
  * `401 Unauthorized`: Invalid API key.

***

**3. Initiate Pi Transfer**

**Endpoint** : `POST /wallet/transfer`\
Initiate a Pi transfer between users.

* **Headers** :
  * `Authorization: Bearer <API_KEY>`
  * `Content-Type: application/json`
* **Body** :

```json
{
  "from_username": "pioneer123",
  "to_username": "pioneer456",
  "amount_pi": 10.50,
  "description": "Payment for eBook"
}
```

* **Response**&#x20;

```json
{
  "status": "success",
  "data": {
    "transaction_id": "txn_123456789",
    "from_username": "pioneer123",
    "to_username": "pioneer456",
    "amount_pi": 10.50,
    "timestamp": "2025-03-05T12:05:00Z"
  }
}
```

* **Status Codes** :
  * `201 Created`: Transfer initiated.
  * `400 Bad Request`: Invalid parameters.
  * `401 Unauthorized`: Invalid API key.

***

**4. List Marketplace Items**

**Endpoint** : `GET /marketplace/listings`\
List available marketplace items.

* **Query Parameters** :
  * `category` (string, optional): Filter by category (e.g., `"digital"`).
  * `limit` (integer, optional): Number of results (default: `10`).
  * `offset` (integer, optional): Pagination offset (default: `0`).
* **Headers** :
  * `Authorization: Bearer <API_KEY>`
* **Response** :

```json
{
  "status": "success",
  "data": [
    {
      "id": "lst_001",
      "title": "Pi Programming eBook",
      "category": "digital",
      "price_pi": 5.00,
      "seller_username": "pioneer789",
      "created_at": "2025-03-01T09:00:00Z"
    },
    {
      "id": "lst_002",
      "title": "Handmade Pi Mug",
      "category": "physical",
      "price_pi": 15.00,
      "seller_username": "pioneer456",
      "created_at": "2025-03-02T14:00:00Z"
    }
  ],
  "meta": {
    "total": 25,
    "limit": 10,
    "offset": 0
  }
}
```



* **Status Codes** :
  * `200 OK`: Listings retrieved.
  * `401 Unauthorized`: Invalid API key.

***

#### **Error Handling**

Errors follow this format:

```json
{
  "status": "error",
  "message": "Invalid API key",
  "code": 401
}
```

#### **Rate Limits**

* **Limit** : 100 requests per minute per API key.
* **Header** : Check `X-RateLimit-Remaining` for remaining requests.

***

#### **Getting Started**

1. **Register** : Obtain your API key at the [TruthWeb Developer Portal ](https://developer.truthweb.com/).
2. **Explore** : Clone the [TruthWeb GitHub Repository ](https://github.com/truthweb)to explore the open-source code.
3. **Contribute** : Submit pull requests to contribute to the project.

***

#### **Support**

For assistance:

* Report issues on [GitHub Issues ](https://github.com/truthweb/issues).
* Email support at [support@truthweb.com ](mailto:support@truthweb.com).

***

#### **Last Updated**

March 05, 2025

***

This documentation provides everything developers need to integrate the TruthWeb Open-Source API into their applications. For more details, refer to the [TruthWeb Developer Portal ](https://developer.truthweb.com/).
