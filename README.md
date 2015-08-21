# stripe-checkout
Test implementation for strip checkout

# Stripe Checkout's ENV variables
Stripe Checkout requires the presence of the following two ENV variables
set up in the corresponding stripe initializer.


# Test
Run app with environment varialbes `PUBLISHABLE_KEY` and `SECRET_KEY`
set. Go too route `/` or `/charges/new` and fill in a test card from
Strip's [test card collection](https://stripe.com/docs/testing).

Observe in resulting `/charges/created` view the response for the charge
requested.
