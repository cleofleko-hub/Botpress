# Paystack Integration Notes

Paystack supports a hosted redirect checkout in which the server initializes a transaction, receives an `authorization_url`, and redirects the customer to Paystack. The initialization request must remain server-side because it uses the secret key. The amount must be sent in the currency subunit, the reference must be unique, and the callback URL must be fully qualified.

The payment return URL is not proof of payment. BOTPRESS must call Paystack's server-side verify endpoint and compare the returned transaction status, reference, amount, currency, and metadata against the local payment record before fulfilling a number or proxy purchase. Fulfillment must be idempotent so a callback and webhook cannot create duplicate services.

Paystack sends successful transaction events as `charge.success` webhooks. The webhook handler must verify the `x-paystack-signature` header using HMAC SHA-512 with the Paystack secret key before processing the event. It should acknowledge valid events with HTTP 200 and keep fulfillment short and deterministic.

| Checkout approach | Tradeoffs | Cost | Setup complexity |
|---|---|---|---|
| Hosted Paystack redirect | Best match for the user's explicit redirect request; strong mobile compatibility; customer briefly leaves BOTPRESS and returns to the callback URL | Standard Paystack transaction fees | Moderate: server initialization, callback verification, signed webhook, and payment-state UI |
| Paystack Popup | Customer remains visually inside BOTPRESS; may be affected by popup handling and requires additional frontend library code | Standard Paystack transaction fees | Moderate-high: server initialization plus Popup V2, callback handling, verification, and signed webhook |

The requested experience selects the hosted redirect option. BOTPRESS will show an internal confirmation prompt first, initialize the transaction on the server, then redirect to Paystack's hosted checkout.

## Official references

1. [Accept Payments](https://paystack.com/docs/payments/accept-payments/)
2. [Transaction API](https://paystack.com/docs/api/transaction/)
3. [Verify Payments](https://paystack.com/docs/payments/verify-payments/)
4. [Webhooks](https://paystack.com/docs/payments/webhooks/)
