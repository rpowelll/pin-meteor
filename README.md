# Pin Meteor Integration Example

This code illustrates how to integrate [Pin][pin-site] payment processing to a
Meteor app. Pin's a great service and the core of this app took around half an
hour to get working.

The eventual goal of this project is to build an [atmosphere][atmosphere]
package that makes adding Pin to an app as easy as possible.

[pin-site]: http://pin.net.au/
[atmosphere]: https://atmosphere.meteor.com

## Roadmap

This example code is pretty new so it still has a few rough edges, here's what
I'll be working on over the next few days to make this a more well-rounded
example:

- Integration with the accounts system
- Proper redirection support
- Animation
- Support for showing the payment form as a bootstrap modal
- Support for recurring payments

Once all of those are out of the way, we'll look at turning this into a package.

## Usage

Right now this is all pretty rough, you'll need to first go into 
`/client/main.js` and change the following line to use your publishable API 
key:

    Pin.setPublishableKey('YOUR_PUBLISHABLE_KEY');

This key can be found on your [account page][account].

Next up you'll need to set the `PIN_API_SECRET` environment variable to your
private key, which should be on the same page as the publishable key.

After that just use the meteorite `mrt server` command and everything should
work without a hitch.

[account]: https://dashboard.pin.net.au/account
