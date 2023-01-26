---
title: "Center div"
date: 2023-01-25T23:15:00+07:00
slug: center-div
category: snippets
summary:
description:
cover:
  image: "covers/accept-a-payment-with-Stripe.jpg"
  alt: "center div"
  caption:
  relative: true
showtoc: true
draft: false
---

Centering a div can sometimes be a frustrating task for developers. It can be especially difficult when trying to center a div both vertically and horizontally. It's a common problem that many developers face and it's something that can slow down your workflow.

```css
.container {
  display: flex; /* establish flex container */
  flex-direction: column; /* make main axis vertical */
  justify-content: center; /* center items vertically, in this case */
  align-items: center; /* center items horizontally */
  height: 100vh;
}
```
