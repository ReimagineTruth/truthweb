---
icon: webhook
---

# API Playground

#### **Overview**

The **API Playground** is an interactive testing environment designed to help developers explore and test TruthWeb's API endpoints. It provides a user-friendly interface to send requests, view responses, and debug issues without needing to set up a development environment.

* **Key Benefits:**
  * Real-time testing of API endpoints.
  * Simplified debugging and experimentation.
  * Pre-filled examples for quick testing.
  * Error handling and response visualization.

***

#### **Features**

**1. Interactive Console**

* **Description** : A web-based interface where developers can input API requests and view responses.
* **Capabilities** :
  * Send `GET`, `POST`, `PUT`, and `DELETE` requests.
  * View formatted JSON responses.
  * Test authentication using API keys.

**2. Pre-Filled Examples**

* **Description** : Ready-to-use examples for common API operations.
* **Examples** :
  * Retrieve a user profile (`GET /profiles/{username}`).
  * Check wallet balance (`GET /wallet/{username}/balance`).
  * Initiate a Pi transfer (`POST /wallet/transfer`).

**3. Request Builder**

* **Description** : A tool to construct API requests step-by-step.
* **Components** :
  * Endpoint selection dropdown.
  * Input fields for query parameters, headers, and body data.
  * Authentication toggle for including API keys.

**4. Response Viewer**

* **Description** : Displays API responses in a readable format.
* **Features** :
  * Syntax highlighting for JSON responses.
  * Expandable/collapsible sections for nested data.
  * Error messages with detailed explanations.

**5. Debugging Tools**

* **Description** : Tools to identify and resolve issues during testing.
* **Features** :
  * Log request/response headers and payloads.
  * Highlight errors (e.g., invalid parameters, missing authentication).
  * Suggest fixes for common issues.

***

#### **How to Use the API Playground**

1. **Access the API Playground** :
   * Navigate to the **Developers** section via the main menu or footer menu.
   * Click on **API Playground** from the navigation links.
2. **Select an Endpoint** :
   * Choose an endpoint from the dropdown menu (e.g., `GET /profiles/{username}`).
   * Review the description and required parameters.
3. **Build Your Request** :
   * Fill in the required fields (e.g., username, API key).
   * Add optional query parameters or body data if needed.
4. **Send the Request** :
   * Click the **Send** button to execute the request.
   * View the response in the **Response Viewer** .
5. **Debug and Iterate** :
   * Analyze the response for correctness.
   * Use the debugging tools to identify and fix issues.
   * Repeat the process with different parameters or endpoints.

***

#### **Example Workflow**

**Retrieve User Profile**

1. **Endpoint** : `GET /profiles/{username}`
2. **Parameters** :
   * `username`: `pioneer123`
   * `Authorization`: `Bearer YOUR_API_KEY`
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

**Initiate Pi Transfer**

1. **Endpoint** : `POST /wallet/transfer`
2. **Headers** :
   * `Authorization`: `Bearer YOUR_API_KEY`
   * `Content-Type`: `application/json`
3. **Body** :

```json
{
  "from_username": "pioneer123",
  "to_username": "pioneer456",
  "amount_pi": 10.50,
  "description": "Payment for eBook"
}
```

**Response**&#x20;

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

#### **Getting Started**

To start using the API Playground:

1. **Sign Up** :
   * Create a developer account at the [TruthWeb Developer Portal ](https://developer.truthweb.com/).
   * Obtain your API key.
2. **Explore Endpoints** :
   * Navigate to the **API Playground** section.
   * Select an endpoint and review its documentation.
3. **Test Requests** :
   * Use the pre-filled examples or build custom requests.
   * Send requests and analyze responses.
4. **Integrate into Your Application** :
   * Once testing is complete, integrate the API into your application.
   * Monitor usage through the Developer Dashboard.

***

#### **Resources**

* **API Documentation** : [API Docs](https://chat.qwen.ai/c/api-docs.html)
* **Developer Dashboard** : [Monitor Usage](https://chat.qwen.ai/c/dashboardmonitoring.html#api)
* **SDKs** : [SDK Docs](https://chat.qwen.ai/c/sdk-docs.html)
* **FAQs** : [Frequently Asked Questions](https://chat.qwen.ai/c/faq.html)

***

#### **Support**

For assistance:

* Report issues on [GitHub Issues ](https://github.com/truthweb/issues).
* Email support at [support@truthweb.com ](mailto:support@truthweb.com).

***

This documentation provides a framework for the **API Playground** , enabling developers to test and debug API integrations effectively. If additional features or details are needed, feel free to ask!
