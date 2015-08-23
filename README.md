# stripe-checkout
This is a minimal example implementation of Stripe Checkout for Rails using the `stripe` gem.

Stripe Checkout (Checkout) is a payment-integration solution of payment service provider Stripe for the web. The main advantage of Checkout is its effortless integration. As opposed to most standard solutions, Checkout does *not* rely on asynchronous backend-to-backend communication by callback. Instead it uses a simple synchronous solution that works in three steps as follows.

1. Using your public Stripe secret, the client (i.e. browser) posts the banking deatils to Stripe and receives a *Stripe token*.
2. Next, based on a callback, the users posts the *Strip token* to your controller. 
3. The controller action makes a post request to Stripe's API including the ammount to be debited as well as the *Stripe token*. This call is synchronous and you immediately receive notice if the card was debited or some error occured. No further reuqests are required. The response contains all information required for managing the purchase.

Possible disadvantages include the followign three items. 
1. Only credit cards are supported
2. Risk management might not be as good as for other solutions
3. I'm not sure if self-managed recurring payment is possible (although you can use some sort of recurring payment by Stripe).

# Test
Run app with environment varialbes `PUBLISHABLE_KEY` and `SECRET_KEY`
set. Go to route `/` or `/charges/new` and fill in a test card from
Strip's [test card collection](https://stripe.com/docs/testing).

Observe in resulting `/charges/created` view the response for the charge
requested.

# References
Official documentation of [Rail integration](https://stripe.com/docs/checkout/guides/rails).
