---
icon: sd-cards
---

# TruthWeb SDKs

#### **Overview**

The **TruthWeb SDKs** enable developers to integrate TruthWeb's decentralized ecosystem into their applications seamlessly. These SDKs provide pre-built libraries and tools for interacting with the TruthWeb API, simplifying tasks such as wallet management, marketplace operations, and transaction tracking.

* **Key Benefits:**
  * Simplified integration with TruthWeb's API.
  * Pre-built functions for common tasks.
  * Support for multiple programming languages.
  * Enhanced developer experience with detailed documentation.

***

#### **Supported SDKs**

**1. JavaScript SDK**

* **Description** : A lightweight library for integrating TruthWeb into web and Node.js applications.
* **Installation**&#x20;

```bash
npm install truthweb-sdk
```

**Usage Example**&#x20;

```javascript
const TruthWeb = require('truthweb-sdk');

const client = new TruthWeb({
  apiKey: 'YOUR_API_KEY',
  baseUrl: 'https://api.truthweb.com/v1/'
});

// Fetch user profile
client.getProfile('pioneer123')
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

* **Features** :
  * Wallet management (balance checks, transfers).
  * Marketplace operations (listings, orders).
  * Transaction tracking.

***

**2. Python SDK**

* **Description** : A Python library for integrating TruthWeb into backend systems or data analysis workflows.
* **Installation** :

```bash
pip install truthweb-sdk
```

**Usage Example**&#x20;

```python
from truthweb import TruthWeb

client = TruthWeb(api_key='YOUR_API_KEY', base_url='https://api.truthweb.com/v1/')

# Fetch marketplace listings
listings = client.get_marketplace_listings(category='digital', limit=10)
print(listings)
```

* **Features** :
  * AI-powered insights.
  * Escrow system integration.
  * Vendor dashboard analytics.

***

**3. Mobile SDKs**

* **Android SDK** :
  * Integration with Android apps using Kotlin or Java.
  * Pre-built UI components for wallet and marketplace features.
* **iOS SDK** :
  * Integration with iOS apps using Swift.
  * Support for push notifications and offline mode.

***

#### **Getting Started**

To start using the TruthWeb SDKs:

1. **Sign Up** :
   * Create a developer account at the [TruthWeb Developer Portal ](https://developer.truthweb.com/).
   * Obtain your API key.
2. **Install the SDK** :
   * Choose the SDK for your preferred programming language.
   * Install it using the package manager (e.g., `npm`, `pip`).
3. **Initialize the SDK** :
   * Use your API key to initialize the SDK client.
   * Configure the base URL if necessary.
4. **Explore Features** :
   * Refer to the SDK documentation for detailed usage examples.
   * Test the SDK in a sandbox environment before deploying to production.

***

#### **Resources**

* **SDK Documentation** : [TruthWeb SDK Docs](https://chat.qwen.ai/c/sdk-docs.html)
* **API Reference** : [API Docs](https://chat.qwen.ai/c/api-docs.html)
* **GitHub Repository** : [Contribute](https://github.com/truthweb)
* **FAQs** : [Frequently Asked Questions](https://chat.qwen.ai/c/faq.html)

***

#### **Support**

For assistance:

* Report issues on [GitHub Issues ](https://github.com/truthweb/issues).
* Email support at [support@truthweb.com ](mailto:support@truthweb.com).

***

#### **Last Updated**

March 05, 2025

***

This documentation provides a conceptual framework for integrating **TruthWeb SDKs** into your projects. If SDKs are not currently supported, this guide can serve as a blueprint for future implementation. For more details, refer to the linked resources or explore the platform directly.
