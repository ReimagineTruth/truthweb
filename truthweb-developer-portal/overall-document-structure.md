---
icon: sd-cards
---

# Overall Document Structure

```html
HTML Document
├── <head>
│   ├── Meta tags and CDNs
│   ├── Styles (CSS)
│   └── Authentication Script (Pi SDK Initialization)
├── <body>
│   ├── UI Elements
│   │   ├── Progress Bar
│   │   ├── Header (with navigation)
│   │   ├── Main Content (sections)
│   │   ├── Footer
│   │   └── Mobile Footer Menu
│   └── Main Script (UI interactions + Authentication handlers)
```

Authentication Code Structure\
Here's how the authentication-related code is organized:

1. Head Section (Initialization)

```html
<script src="https://sdk.minepi.com/pi-sdk.js">
<script src="https://code.jquery.com/jquery-3.6.0.min.js">
<script>
  // Pi SDK Initialization
  Pi.init({ version: "2.0", sandbox: true })
  
  // Scope Definition
  const scopes = ['username', 'payments', 'wallet_address']
  
  // Core Authentication Functions
  ├── onIncompletePaymentFound()
  ├── authenticateUser()
  ├── updateUIAfterAuth()
  ├── sendAuthToServer()
  └── createPiPayment()
</script>
```

2. Body Section (Main Script)

```html
<script>
  // Existing UI code...
  
  // Authentication Integration
  document.addEventListener('DOMContentLoaded', () => {
    ├── Check existing auth
    ├── Auth button handler
    └── Subscribe function for payment plans
  })
</script>
```

Detailed Authentication Structure

```
Authentication System
├── Initialization
│   ├── Pi.init() - SDK setup with version and sandbox mode
│   └── scopes - Array of requested permissions
│
├── Core Functions
│   ├── onIncompletePaymentFound(payment)
│   │   ├── Handles pending payments
│   │   └── Makes POST request to server
│   │
│   ├── authenticateUser()
│   │   ├── async Pi.authenticate()
│   │   ├── Stores user data
│   │   ├── Updates UI
│   │   ├── Sends to server
│   │   └── Error handling
│   │
│   ├── updateUIAfterAuth(userData)
│   │   ├── Updates profile icon
│   │   └── Marks wallet as authenticated
│   │
│   ├── sendAuthToServer(userData)
│   │   ├── AJAX POST to server
│   │   └── Error handling
│   │
│   └── createPiPayment(amount, memo)
│       ├── Payment creation
│       ├── Event handlers
│       │   ├── onReadyForServerApproval
│       │   ├── onReadyForServerCompletion
│       │   ├── onCancel
│       │   └── onError
│       └── Error handling
│
└── Event Listeners
    ├── DOMContentLoaded
    │   ├── Check stored auth
    │   ├── Auth button click
    │   └── Subscribe function
    └── UI Interactions
```

Integration with HTML Structure

```*
<body>
  ├── <header> 
  │   └── Authentication UI updates (profile/wallet icons)
  │
  ├── <main>
  │   ├── Hero Section
  │   │   └── "Authenticate with Pi" button
  │   ├── Payment Plans Section
  │   │   └── Subscribe buttons
  │   └── Other sections
  │
  └── <script>
      └── Authentication event handlers
```

Data Flow

```*
1. User clicks "Authenticate with Pi"
   ├── Pi SDK popup appears
   └── User approves scopes

2. authenticateUser()
   ├── Gets authResult
   ├── Stores in localStorage
   ├── Updates UI
   └── Sends to server

3. User clicks "Subscribe"
   ├── Checks auth status
   ├── Initiates createPiPayment()
   └── Handles payment flow
```

File Dependencies

```html
├── Pi SDK (https://sdk.minepi.com/pi-sdk.js)
├── jQuery (https://code.jquery.com/jquery-3.6.0.min.js)
└── Server Endpoints
    ├── /api/auth/pi (POST)
    └── /payment/complete (POST)
```

CSS Structure (Authentication-related)

```html
<style>
  ├── .icon.authenticated
  │   └── Visual feedback for auth state
  └── .btn.authenticating
      └── Loading state styling
</style>
```

Key Features

1. Modular Functions:
   * Separate concerns (auth, UI, payments)
   * Reusable components
2. State Management:
   * localStorage for session persistence
   * UI updates reflect auth status
3. Error Handling:
   * Try/catch blocks
   * User-friendly alerts
4. Event-driven:
   * DOMContentLoaded initialization
   * Click handlers for auth and payments

This structure provides:

* Clear separation of concerns
* Easy maintenance and updates
* Scalable authentication system
* Responsive UI integration
* Robust error handling
