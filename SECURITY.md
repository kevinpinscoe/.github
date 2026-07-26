# Security Policy

Thank you for helping keep these projects and their users safe. This policy
applies to the open-source projects maintained by Kevin P. Inscoe. Where a
project has its own `SECURITY.md`, that project's policy takes precedence.

## Supported Versions

| Project type | Supported | Notes |
|---|---|---|
| Latest tagged release | ✅ | Security fixes are released here first. |
| Current `main` branch | ✅ | Fixes land here at the same time. |
| Previous minor release | ⚠️ | Backported only for critical severity. |
| Anything older | ❌ | Upgrade to the latest release. |
| Untagged / no-release repos | ✅ `main` only | Notes, configs, and dotfiles repos. |

If a fix cannot be backported, the advisory will say so and name the minimum
version you must upgrade to. A project's own `SECURITY.md` may define a
different support policy.

## Reporting a Vulnerability

**Do not report security vulnerabilities through public issues, pull requests,
or discussions.** Public disclosure before a fix is available puts users at
risk.

Use one of these private channels instead:

1. **GitHub Private Vulnerability Reporting (preferred).** On the affected
   repository, go to the **Security** tab and click
   **"Report a vulnerability"**. This is enabled on every repository covered by
   this policy. It opens a private, tracked report visible only to the
   maintainer, and it is encrypted in transit and at rest.
2. **Email (fallback).** Send the details to
   **[kevin.inscoe@gmail.com](mailto:kevin.inscoe@gmail.com)**.

   Plain email is **not** a secure channel. If your report contains a working
   exploit, credentials, or user data, please encrypt it with the OpenPGP key
   below.

### OpenPGP Key

Use this key to encrypt an emailed report.

| | |
|---|---|
| **Primary fingerprint** | `FEDA 8FCB A361 BCF2 1C5A  EE68 400D 8321 5F67 26D6` |
| **User ID** | Kevin P Inscoe `<kevin.inscoe@gmail.com>` |
| **Algorithm** | ed25519 (signing) / cv25519 (encryption) |
| **Valid** | 2025-05-02 through 2030-05-01 |

Fetch the key from either source — both serve the same key:

```bash
# Preferred — GitHub account key endpoint
curl -sSL https://github.com/kevinpinscoe.gpg | gpg --import

# Alternative — direct download
curl -sSL https://raw.githubusercontent.com/kevinpinscoe/dotfiles/main/kevinpinscoe_gpg_public_key.asc | gpg --import
```

The key is also browsable at
[`kevinpinscoe/dotfiles`](https://github.com/kevinpinscoe/dotfiles/blob/main/kevinpinscoe_gpg_public_key.asc).

**Always verify the fingerprint before using the key.** Do not trust a key
merely because it downloaded over HTTPS:

```bash
gpg --fingerprint 400D83215F6726D6
```

The output must match the primary fingerprint in the table above exactly. If it
does not, stop and report the mismatch — through GitHub Private Vulnerability
Reporting, not by email.

> An older key with fingerprint `FEB6 17CC F66F CE4D 3D6A  D859 DB96 387D 487E 557B`
> is superseded and must not be used.

## What to Include

A good report helps the issue get fixed faster. Please include:

- A description of the vulnerability and its potential impact.
- The affected project, and the version or commit where you found it.
- Step-by-step instructions to reproduce it (a minimal proof of concept is
  ideal).
- Any suggested remediation, if you have one.

## What to Expect

| Stage | Target |
|---|---|
| Acknowledgement of your report | 5 business days |
| Triage — severity and scope confirmed | 10 business days |
| Status update while work is in progress | every 14 days |
| Fix released — critical / high severity | 30 days from triage |
| Fix released — medium / low severity | 90 days from triage |

**Acknowledgement, triage, and status updates are commitments.** If one of those
is missed, you are free to act on the disclosure terms below.

**The fix windows are targets, not guarantees.** These are personal projects
maintained by one person. Actual timing may depend on the complexity of the
fix, maintainer availability, coordinated-disclosure requirements involving
upstream or downstream parties, and other circumstances outside the
maintainer's control. Where a target will be missed, you will be told before it
lapses, given the reason, and given a revised estimate — silence is not an
acceptable outcome, and the status-update commitment above still applies.

The fix will be developed privately. A disclosure timeline will be coordinated
with you before any public release.

**Credit:** with your permission, you will be credited when the fix is
published. Let me know if you prefer to remain anonymous.

## Disclosure Policy

These projects follow coordinated vulnerability disclosure.

- The **default embargo is 90 days** from the date you report the issue. After
  90 days you are free to publicly disclose, whether or not a fix has shipped.
- If a fix ships sooner, the advisory is published as soon as a release
  containing the fix is available, and the embargo ends at that point.
- If the vulnerability is **already being exploited in the wild**, the embargo
  is void — tell me, and details will be published immediately alongside any
  mitigation available.
- If you do not hear back within the acknowledgement window above, treat that
  as a failure on my part. Please escalate by opening a **public** issue that
  says only that you sent a private report and received no reply — do not
  include the vulnerability details.

Every fixed vulnerability is published as a **GitHub Security Advisory (GHSA)**
on the affected repository, and a CVE is requested through GitHub where the
issue warrants one. Advisories are public and permanent — they are the record
of how defects in these projects were handled.

## Safe Harbor

If you make a good-faith effort to follow this policy while researching a
vulnerability:

- Your research is considered **authorized**, and no legal action will be
  pursued or supported against you.
- You will be treated as having complied with this policy even if you make an
  honest mistake, so long as you report it.
- If a third party brings action against you for research conducted under this
  policy, this authorization will be made known to them.

To stay within safe harbor, please:

- Make a good-faith effort to avoid privacy violations, data destruction, and
  service degradation.
- Use only your own accounts and test data — never another person's.
- Stop as soon as you have confirmed a vulnerability, and report it. Do not
  pivot, escalate, or exfiltrate further than needed to demonstrate the issue.
- Keep the details private until the embargo above has ended.

Nothing in this section authorizes activity against third-party systems, or
against anything not covered by the **Scope** section below.

## Scope

This policy covers the source code, build and release pipelines, and released
artifacts of the projects it applies to — including the packages published
through these distribution channels:

| Channel | Repository |
|---|---|
| Homebrew tap | [`kevinpinscoe/homebrew-tap`](https://github.com/kevinpinscoe/homebrew-tap) |
| Debian / APT | [`kevinpinscoe/apt`](https://github.com/kevinpinscoe/apt) |
| Fedora / RPM | [`kevinpinscoe/rpm`](https://github.com/kevinpinscoe/rpm) |
| Scoop bucket | [`kevinpinscoe/scoop-bucket`](https://github.com/kevinpinscoe/scoop-bucket) |

Supply-chain reports are explicitly in scope: tampered formulas or manifests,
broken or forged artifact signatures, compromised release workflows, and
malicious dependencies reaching a published package.

This policy does **not** cover:

- Vulnerabilities in third-party dependencies — report those to the upstream
  project (a heads-up here is still welcome, and the dependency will be bumped).
- Issues that require physical access to a user's machine or
  already-compromised credentials.
- Findings against **forked** repositories that reproduce upstream behavior —
  report those to the upstream project. Changes made in a fork's `personal`
  branch are in scope.
- Automated scanner output submitted without a demonstrated impact.

## Verifying Release Artifacts

Go release artifacts are signed with [Cosign](https://github.com/sigstore/cosign)
using keyless Sigstore signing. Verify a download before trusting it:

```bash
cosign verify-blob \
  --bundle checksums.txt.sigstore.json \
  --certificate-identity-regexp \
    'https://github.com/kevinpinscoe/<repo>/.github/workflows/release.yml@refs/tags/v.*' \
  --certificate-oidc-issuer 'https://token.actions.githubusercontent.com' \
  checksums.txt
```

A signature that fails to verify is itself a security report — please send it
through the private channels above.

## No Bug Bounty

These are personal open-source projects maintained by one person in their own
time. There is **no bug bounty and no monetary reward**. What is offered is a
prompt response, a real fix, public credit, and a published advisory. Please
report anyway — it is genuinely appreciated.

## Questions

For non-sensitive questions about this policy, open a regular issue or email
[kevin.inscoe@gmail.com](mailto:kevin.inscoe@gmail.com).
