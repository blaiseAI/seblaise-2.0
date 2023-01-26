---
title: "Stripe"
date: 2022-04-03T23:15:00+07:00
slug: accept-a-payment-with-Stripe
category: snippets
summary:
description:
cover:
  image: "covers/accept-a-payment-with-Stripe.jpg"
  alt: "Accept a payment with Stripe"
  caption:
  relative: true
showtoc: true
draft: false
---

**Accept a payment.**

```js
const stripe = require("stripe")(process.env.STRIPE_API_KEY);

export default async (req, res) => {
  const session = await stripe.checkout.sessions.create({
    payment_method_types: ["card"],
    line_items: [
      {
        name: "Serverless Functions – The Complete Guide",
        description: "100 page e-book on serverless functions.",
        images: ["https://site.com/image.png"],
        amount: "5000", // Cents
        currency: "usd",
        quantity: 1,
      },
    ],
    success_url: "https://site.com/success?session_id={CHECKOUT_SESSION_ID}",
    cancel_url: "https://site.com",
  });

  return res.status(200).json(session);
};
```

## Usage

### 1. Create Checkout Session

Using the function above, create a checkout session returning `CHECKOUT_SESSION_ID`. Upon success, it will redirect to your `success_url`.

### 2. Redirect to Checkout

Follow Stripe's documentation to complete the client-side.

### 3. Add Environment Variables

To securely access the API, we need to include the secret with each request. We also do not want to commit secrets to git. Thus, we should use an environment variable. Learn how to add environment variables in Vercel.
