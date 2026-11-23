# DNS plan (ready for after the Hover purchase) — Path B

DNS (Domain Name System) = the address book that points the domain to the website and email.

## goldengatescompany.com (main)
| Record | Host | Value | Purpose |
|---|---|---|---|
| A / CNAME | @ and www | from the web host at setup | website |
| MX | @ | smtp.google.com (priority 1) | Google Workspace email |
| TXT | @ | v=spf1 include:_spf.google.com ~all | proves Google may send our mail |
| TXT | google._domainkey | generated in Google Admin | DKIM signature |
| TXT | _dmarc | v=DMARC1; p=none; rua=mailto:(Jason's Workspace address) | email trust reports; tighten later |
| CNAME/TXT | per Stripe | from Stripe custom email domain setup | receipts from our domain |
- https: free certificate issued by the web host once the records point there.

## goldengates.company
- 301 permanent redirect, all paths, to https://goldengatescompany.com (Hover forwarding or the web host).
- Email: none (or forward to the main inbox).

Values marked "generated" are filled during setup; never guessed.
