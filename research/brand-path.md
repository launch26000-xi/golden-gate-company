# 100% Golden Gates branding: platform decision (2026-11-23)

Jason's rule: no third-party names visible to families anywhere (site, checkout, emails, receipts, phone, listing).

## Path A: Shopify, every branding setting removed
What a family sees:
- Site: Golden Gates design on goldengatescompany.com. "Powered by Shopify" footer can be removed in the theme.
- Checkout: on our domain, our logo/colors. BUT on non-Plus plans (Plus starts ~$2,300/mo) checkout layout is locked
  and only lightly brandable; Shop Pay button/"Shop" sign-in prompts appear unless Shop Pay is turned off.
- Order status / thank-you page: Shopify's standard blocks (map, icons) can't be removed on non-Plus plans.
- Emails: say "via shopifyemail.com" until our sending domain is authenticated (DNS + DMARC); fixable, sometimes fussy.
- Customer account login: may run on a shopify.com address unless a custom account subdomain is set up.
- Card statement: our descriptor; Shop Pay purchases can show Shop Pay naming.
Verdict: about 95% ours. Small Shopify traces survive at checkout and order pages that we cannot fully control.
Cost: Basic ~$29/mo annual or $39/mo monthly, plus payment fees.

## Path B: Golden Gates site on its own domain, Stripe handling payments quietly (RECOMMENDED)
What a family sees:
- Site: 100% Golden Gates, built by Claude Code, hosted on goldengatescompany.com. Host name never shown.
- Payment: card fields sit INSIDE our own page (Stripe "Payment Element", embedded). No Stripe-hosted page, no
  stripe.com address bar. Turn Link (Stripe's one-click wallet) OFF so no "Link" button shows.
  Keep Apple Pay / Google Pay OFF for 100% (they show their own names).
- Receipts/emails: turn Stripe receipts OFF and send our own from @goldengatescompany.com (Google Workspace),
  or set Stripe's custom email domain so they come from our domain with our logo.
- Card statement: our descriptor (e.g. GOLDEN GATES CO).
Verdict: about 100% ours. The only outside things a family could ever see are their OWN bank's security popup
(3-D Secure) and, if they open browser developer tools, the secure card frame address. Neither is our vendor's brand.
Cost: no platform subscription; hosting free-to-low; Stripe per-transaction fee only.

## Same rules for everything else
- Phone line: ElevenLabs voice says only "Golden Gates." Register outbound caller ID name (CNAM) as GOLDEN GATES.
- Email: Google Workspace on our domain; recipients see @goldengatescompany.com only.
- Google Business Profile: the listing lives on Google Maps (that's the point), but every word, photo and link is ours.
- Domain: registrar never visible to families; privacy protection hides owner details.

## Domain decision under Path B
Outside registrar beats a Shopify-bought domain: portable, not tied to any platform subscription, full DNS control
for Workspace email, Stripe email domain, and the .company redirect.
ONE pick stays: Hover. .com $18.99/yr, .company ~$44.99–46.99/yr, renewal = first-year price. ~$64–66/yr total,
well under the ~$200 ceiling.

## Sources
- https://help.shopify.com/en/manual/checkout-settings/checkout-extensibility
- https://help.shopify.com/en/manual/orders/status-tracking/customize-order-status
- https://community.shopify.com/t/allow-removal-of-native-blocks-map-icons-on-thank-you-page-for-non-plus-plans/643783
- https://help.shopify.com/en/manual/intro-to-shopify/initial-setup/setup-your-email
- https://community.shopify.com/t/how-to-remove-via-shopify-com-in-the-email-sent-to-the-customers/15028
- https://www.nerdwallet.com/article/small-business/shopify-pricing
- https://docs.stripe.com/payments/payment-element
- https://docs.stripe.com/get-started/account/branding
- https://docs.stripe.com/payments/link/payment-element-link
- https://docs.stripe.com/payments/checkout/custom-domains
- https://docs.stripe.com/get-started/account/email-domain
- https://www.whtop.com/plans/hover.com/82297
- https://domainoffer.net/tld/company/hover
