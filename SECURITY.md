# Security policy

This policy covers the **Global Fund Data Service**:

- the Data API at [fetch.theglobalfund.org](https://fetch.theglobalfund.org)
- the Data Service website at [data-service.theglobalfund.org](https://data-service.theglobalfund.org)

## Reporting a vulnerability

**Please don't report security problems in a public issue, discussion or pull request.**

Report them privately through [**Report a vulnerability**](../../security/advisories/new) on this repository's
*Security* tab. Only the maintainers can see your report.

Please include:

- the affected URL, endpoint or page, and the API version if it applies
- the steps to reproduce, with example requests
- what an attacker could do with it, and what you observed
- whether you have shared the issue with anyone else

## What to expect

| Step | Our aim |
|---|---|
| Acknowledge your report | Within 3 working days |
| Confirm whether it is a vulnerability, and how severe | Within 10 working days |
| Fix or mitigate | As quickly as severity requires. We'll keep you updated until it's resolved |

When the fix is live, we'll publish a security advisory here and credit you, unless you'd rather stay anonymous.

## Scope

**In scope:** the Data API, the Data Service website, and the download files they serve.

**Out of scope:**

- theglobalfund.org and other Global Fund sites and systems. Report those through the Global Fund's own channels.
- Denial-of-service and load testing, automated scanning that floods the service, and social engineering of staff.
- Reports that a public dataset contains data. The data is published on purpose. If you think something was published
  by mistake, such as personal data, do report it privately here.

## Testing guidelines

While you investigate, please:

- only use your own access, and stop as soon as you've confirmed the issue
- don't access, change or delete data that isn't public
- keep request rates low so the service stays available for others
- give us reasonable time to fix the issue before you disclose it publicly

We won't pursue or support legal action against anyone who reports in good faith and follows these guidelines.
