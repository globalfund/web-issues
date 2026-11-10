# Global Fund Data Service: Issues and Feedback

This repository is the public place to report problems with, and suggest improvements to, the
**Global Fund Data Service**:

- the **Data API** at [fetch.theglobalfund.org](https://fetch.theglobalfund.org), an OData API over the Global Fund's
  grant, financial and results data
- the **Data Service website** at [data-service.theglobalfund.org](https://data-service.theglobalfund.org), where you can download ready-made data files
  and browse the API reference

The source code for both is kept in a private repository, so this repository holds no code. It is only for issues and
discussion. The team triages everything filed here and links it to the internal work that fixes it.

## The Data API

| What | Where |
|---|---|
| API | `https://fetch.theglobalfund.org/v{version}/odata/{EntitySet}`, for example [`/v5/odata/Grants?$top=10`](https://fetch.theglobalfund.org/v5/odata/Grants?$top=10) |
| Reference | The [API Reference](https://data-service.theglobalfund.org/api) page on the Data Service website |
| Supported versions | v5 (current), v4.2, v4.1 and v4 |

The API is an OData service, so the standard query options work: `$filter`, `$select`, `$expand`, `$orderby`,
`$top`, `$skip` and `$count`.

> Versions are chosen in the URL (`/v4.2/...`, `/v5/...`). New features land in the latest version.
> Older versions get fixes for serious bugs only.

## The Data Service website

| Page | What it's for |
|---|---|
| [Home](https://data-service.theglobalfund.org) | An overview of the data and how to get it |
| [Downloads](https://data-service.theglobalfund.org/downloads) | Ready-made data files by category, with each file's formats, size, last update, row count and columns. Search finds files and column names |
| [API Reference](https://data-service.theglobalfund.org/api) | The interactive reference for each API version (`/api?version=v4.1`) |

Every Downloads search and category has its own address (for example
`/downloads?category=grants/disbursements&q=kenya`), and each file card has a link you can copy. Paste these into
your issue so we can see exactly what you saw.

## Before you file an issue

1. **Search [existing issues](../../issues?q=is%3Aissue)**, open and closed. If yours is already there, add a 👍 or
   a comment with your details rather than opening a new one.
2. **Check the [API Reference](https://data-service.theglobalfund.org/api)** on the Data Service website to confirm the entity, field or
   query option exists in the version you are calling.
3. **Is it about the data, the API or the website?** Values that look wrong (a figure, a grant status, a country
   name) come from the Global Fund's source systems, and the same values appear in both the API and the download
   files. Report them as a data issue with the record's key, and we will route them.

## How to file

Choose **[New issue](../../issues/new/choose)** and pick a template:

- **🐞 API bug**: an error, a wrong or missing result, a slow query, or API behaviour that disagrees with the docs.
- **🖥️ Website bug**: a page that breaks, looks wrong or is hard to use, or a download file that won't open or
  doesn't match its description.
- **📊 Data issue**: a value or record that looks wrong or is missing, in the API or a download file.
- **✨ Feature request**: a new entity, field, filter, download file, website feature or version change.
- **📘 Documentation**: something in the API Reference or other website text that is unclear or wrong.

A good bug report includes:

- **For the API:** the full request URL, including the version and query options.
- **For the website:** the page address, your browser and device, and a screenshot if something looks wrong.
- What you **expected** and what you **got**: the HTTP status and error message, or what appeared on screen.
- **When** it happened (UTC), and whether it happens every time.

Please do **not** include API keys, tokens, personal data or anything confidential. Issues here are public.

## What happens next

Every issue gets an area label, `api`, `website` or `data`, plus a status label:

| Label | Meaning |
|---|---|
| `triage` | New, not yet reviewed |
| `confirmed` | Reproduced, and tracked in our internal backlog |
| `needs-info` | We need more details from you. Issues with no reply for 14 days are closed |
| `planned` / `wontfix` | Accepted for a future release, or declined with a reason |

Issues are closed when the fix is live, with a note saying what changed (and for the API, which version).
Notable changes are also listed in [Releases](../../releases).

## Security issues

**Don't open a public issue for a security problem** in the API or the website. Report it privately through
[**Report a vulnerability**](../../security/advisories/new) (the *Security* tab). Only the maintainers can see it.
See [SECURITY.md](SECURITY.md) for what to include and how quickly we respond.

## Questions and ideas

For "how do I…" questions or open-ended ideas, use [Discussions](../../discussions) instead of an issue.

## Code of conduct

Be respectful and constructive. See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md).
