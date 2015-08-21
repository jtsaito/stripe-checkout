# stripe-checkout
Minimal implementation of Stripe Checkout for Rails using the `stripe` gem.

# Test
Run app with environment varialbes `PUBLISHABLE_KEY` and `SECRET_KEY`
set. Go too route `/` or `/charges/new` and fill in a test card from
Strip's [test card collection](https://stripe.com/docs/testing).

Observe in resulting `/charges/created` view the response for the charge
requested.

# Reference
Official documentation of [Rail integration](https://stripe.com/docs/checkout/guides/rails).
