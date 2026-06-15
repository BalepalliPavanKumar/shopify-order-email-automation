
# Shopify Order Conditional Email Campaign

## Overview

This Pipedream workflow receives a Shopify order webhook and validates:

1. Order contains tag "MakeOrder"
2. Customer contains tag "ColdCustomer"
3. Order amount is greater than ₹2500

If all conditions are satisfied:

- Send an immediate onboarding email
- Wait 5 minutes
- Send a discount email

Otherwise, the workflow exits.

## Workflow

Webhook Trigger
↓
Condition Validation
↓
Immediate Email
↓
5 Minute Delay
↓
Discount Email



## Technologies

- Pipedream
- Gmail Integration
- Shopify Webhooks

Execution Result

The workflow was successfully tested using the sample payload.

Results:

Webhook received successfully
Conditions validated successfully
Immediate onboarding email sent
5-minute delay executed successfully
Discount email sent successfully
  

## Test Payload

```json
{
  "tags": "MakeOrder",
  "total_price": "3000",
  "email": "customer@example.com",
  "customer": {
    "first_name": "Customer",
    "email": "customer@example.com",
    "tags": "ColdCustomer"
  }
}
