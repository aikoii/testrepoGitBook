# Annotations deletes

<table><thead><tr><th>Field Name</th><th width="134.33333333333331">Mandatory?</th><th>Description</th></tr></thead><tbody><tr><td>paymentMethod adding text</td><td>Yes[<a data-footnote-ref href="#user-content-fn-1">1</a>]</td><td>Payment method to be used with Nomupay (eg nomupay.ecpay, nomupay.linepay, etc).</td></tr><tr><td>checkoutRedirectURL</td><td>Yes[2]</td><td>URL on Merchant’s server to return to when the Nomupay APM Checkout is closed.</td></tr><tr><td>checkoutOptions</td><td>No[<a data-footnote-ref href="#user-content-fn-2">3</a>],[4]</td><td>Record containing options are used to customise <a href="page-3.md#checkout-options-hosted-and-direct-integration">Nomupay APM Checkout.</a></td></tr><tr><td>nomupayCheckoutOptions</td><td>No[<a data-footnote-ref href="#user-content-fn-3">5</a>],[4]</td><td>Record containing options used to customise the <a href="page-3.md#checkout-options-hosted-and-direct-integration">Nomupay APM Checkout.</a></td></tr></tbody></table>

_\[1] Optional in Hosted Integration._

_\[3] Direct Integration only._

_\[4] Whilst the Gateway does not see this field as mandatory, Nomupay may have payment methods that require additional configuration using checkout options._

_\[2] Not required for Hosted Integration._

_\[5] Hosted Integration Only._

1. _Not required for Hosted Integration._
2. _Whilst the Gateway does not see this field as mandatory, Nomupay may have payment methods that require additional configuration using checkout options._

[^1]: Optional in Hosted Integration.

[^2]: Direct Integration only.

[^3]: Hosted Integration Only.
