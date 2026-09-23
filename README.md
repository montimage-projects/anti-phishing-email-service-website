# Montimage Anti-Phishing Email Service: website and feedback

This repository holds the public website of the **Montimage Anti-Phishing Email Service** and its public issue tracker. It is the place to report a wrong verdict or a bug, request a feature, or send feedback.

**Website:** https://montimage-projects.github.io/anti-phishing-email-service-website/

## Get support or send feedback

| I want to… | Where |
|---|---|
| Report a phishing email called safe, or a genuine email flagged as phishing | [Wrong verdict form](https://github.com/montimage-projects/anti-phishing-email-service-website/issues/new?template=wrong_verdict.yml) |
| Report a problem (no reply, broken report, deployment issue) | [Bug report form](https://github.com/montimage-projects/anti-phishing-email-service-website/issues/new?template=bug_report.yml) |
| Suggest an improvement | [Feature request form](https://github.com/montimage-projects/anti-phishing-email-service-website/issues/new?template=feature_request.yml) |
| Share general feedback | [Feedback form](https://github.com/montimage-projects/anti-phishing-email-service-website/issues/new?template=feedback.yml) |
| Send something confidential, or ask about deployment and licensing | Email [developer@montimage.eu](mailto:developer@montimage.eu) |

> **Issues are public.** Never paste a suspicious email, its headers, email addresses or attachments into an issue. Give the **Reference** code printed at the foot of your report, and send the email itself to developer@montimage.eu if we ask for it.
>
> **antiphishing@montimage.eu only analyses emails.** Anything sent there is treated as a suspicious email and answered with a verdict. Support requests go to developer@montimage.eu.

See the [privacy policy](https://montimage-projects.github.io/anti-phishing-email-service-website/privacy.html) for how forwarded emails and support requests are handled.

---

<details>
<summary>Website development</summary>

Plain static HTML and CSS, no build step. Everything published lives in `site/`:

| Path | Content |
|---|---|
| `site/index.html` | Landing page (page-specific styles inline) |
| `site/support.html` | Support and feedback channels |
| `site/privacy.html` | Privacy policy |
| `site/404.html` | Not-found page served by GitHub Pages |
| `site/site.css` | Shared tokens, header, footer, buttons and inner-page styles |
| `site/fonts/` | Self-hosted fonts (SIL Open Font License, see the `OFL-*.txt` files) |

Preview locally:

```bash
python3 -m http.server 8000 --directory site
```

Then open http://localhost:8000.

Every push to `main` deploys `site/` to GitHub Pages through `.github/workflows/deploy-pages.yml`. The site loads nothing from third parties: keep fonts and images self-hosted, and update the privacy policy if that ever changes.

</details>

---

© 2026 Montimage, 39 rue Bobillot, 75013 Paris, France. All rights reserved. The Anti-Phishing Email Service is proprietary software licensed by Montimage. Fonts are distributed under the SIL Open Font License.
