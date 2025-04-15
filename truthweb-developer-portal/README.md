---
icon: laptop-binary
---

# TruthWeb Developer Portal

#### **Overview**

The **TruthWeb Developer Portal** is a comprehensive resource for developers looking to integrate TruthWeb's decentralized ecosystem into their applications. It provides access to APIs, SDKs, documentation, and tools to streamline development and enhance user experiences.

* **Key Benefits:**
  * Access to powerful APIs for wallet management, marketplace operations, and transaction tracking.
  * Pre-built SDKs for multiple programming languages.
  * Detailed documentation and code examples.
  * Community-driven support and collaboration.

***

#### **Features**

**1. API Documentation**

* **Description** : Comprehensive guides and reference materials for integrating with TruthWeb's API.
* **Endpoints** :
  * Retrieve user profiles `(GET /profiles/{username}).`
  * Check wallet balances (`GET /wallet/{username}/balance`).
  * Initiate Pi transfers (`POST /wallet/transfer`).
  * List marketplace items (`GET /marketplace/listings`).
* **Authentication** : API key required for all requests.
* **Rate Limits** : 100 requests per minute per API key.

**2. SDKs**

* **JavaScript SDK** :
  * Install via npm: `npm install truthweb-sdk`.
  * Simplifies integration with web and Node.js applications.
* **Python SDK** :
  * Install via pip: `pip install truthweb-sdk`.
  * Ideal for backend systems and data analysis workflows.
* **Mobile SDKs** :
  * Android (Kotlin/Java) and iOS (Swift) libraries for mobile app development.

**3. API Playground**

* **Description** : A real-time testing environment for experimenting with API endpoints.
* **Features** :
  * Interactive console for sending requests and viewing responses.
  * Pre-filled examples for quick testing.
  * Error handling and debugging tools.

**4. Webhooks**

* **Description** : Real-time event notifications for specific actions (e.g., transactions, listings).
* **Supported Events** :
  * `transaction.created`: Triggered when a new transaction is initiated.
  * `listing.created`: Triggered when a new item is listed on the marketplace.
  * `user.verified`: Triggered when a user completes KYC verification.
* **Security** : Signature verification ensures payload authenticity.

**5. Developer Dashboard**

* **Description** : A centralized dashboard for managing API keys, monitoring usage, and tracking performance metrics.
* **Features** :
  * Generate and revoke API keys.
  * View API usage statistics (requests per minute, errors, etc.).
  * Monitor webhook activity and delivery status.

**6. Open-Source Contributions**

* **GitHub Repository** : [Contribute to TruthWeb ](https://github.com/truthweb).
* **Features** :
  * Submit pull requests for bug fixes or feature enhancements.
  * Report issues and collaborate with the developer community.
  * Access source code for transparency and customization.

***

#### **Getting Started**

1. **Sign Up** :
   * Create a developer account at the [TruthWeb Developer Portal ](https://developer.truthweb.com/).
   * Complete KYC verification for enhanced security.
2. **Generate API Key** :
   * Navigate to the **Developer Dashboard** .
   * Generate an API key to authenticate your requests.
3. **Explore Documentation** :
   * Review the API documentation for detailed endpoint descriptions and usage examples.
   * Test endpoints in the **API Playground** .
4. **Install SDKs** :
   * Choose the SDK for your preferred programming language.
   * Follow the installation and usage instructions.
5. **Deploy Your Application** :
   * Once testing is complete, deploy your application to production.
   * Monitor API usage and performance through the Developer Dashboard.

***

#### **Resources**

* **API Documentation** : [API Docs](../basics/integrations/)
* **SDK Documentation** :[ SDK Docs](../truthweb-sdks.md)
* **API Playground** : Test Endpoints
* **GitHub Repository** : [Contribute](https://github.com/truthweb)
* **FAQs** : [Frequently Asked Questions](https://chat.qwen.ai/c/faq.html)

***

#### **Support**

For assistance:

* Report issues on [GitHub Issues ](https://github.com/truthweb/issues).
* Email support at [support@truthweb.com ](mailto:support@truthweb.com).

***

#### **Last Updated**

March 13, 2025

***

This documentation provides a framework for the **TruthWeb Developer Portal** , enabling developers to seamlessly integrate with the Pi Network ecosystem. If additional features or details are needed, feel free to ask!
