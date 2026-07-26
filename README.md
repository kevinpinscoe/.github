# Default Community Health Files

## Summary

A general guide explaining how to contribute to the open-source projects
Kevin P. Inscoe maintains. It covers reporting issues, proposing changes,
and the conventions contributors are expected to follow.

**➡️ Read the guide: [CONTRIBUTING.md](CONTRIBUTING.md)**

## Status

Production

## Purpose

Maintaining several public projects means repeating the same contribution
guidance in each one. This public `.github` repository is the canonical source
for GitHub's default community health files. GitHub applies them to repositories
owned by `kevinpinscoe` that do not provide their own files.

- **Problem it solves:** scattered, inconsistent contribution instructions.
- **Who uses it:** anyone who wants to contribute to a project Kevin maintains.
- **What depends on it:** public repositories owned by `kevinpinscoe` that do
  not override these files.

## Repository Layout

```
.github/
├── CONTRIBUTING.md   # the contribution guide itself
├── SECURITY.md       # how to report security vulnerabilities
├── LICENSE           # CC BY 4.0
├── README.md         # this file
├── RUNBOOK.md        # how to maintain and publish this repo
├── mise.toml         # tool version pinning (mise)
└── .gitignore
```

## Security

This repository contains documentation only — no executable code or secrets.
To report a security vulnerability, do **not** open a public issue. Use GitHub's
**"Report a vulnerability"** button on the Security tab, or email
[kevin.inscoe@gmail.com](mailto:kevin.inscoe@gmail.com) — encrypted with the
OpenPGP key `FEDA 8FCB A361 BCF2 1C5A  EE68 400D 8321 5F67 26D6` if the report
contains an exploit or sensitive data. See [SECURITY.md](SECURITY.md) for the
full policy, including the disclosure timeline and safe-harbor terms.

## Ownership and Support

- **Maintainer:** Kevin P. Inscoe
- **Contact:** [kevin.inscoe@gmail.com](mailto:kevin.inscoe@gmail.com)

## Related Documentation

- [Contributing](CONTRIBUTING.md)
- [Security Policy](SECURITY.md)
- [Runbook](RUNBOOK.md)

## License

Licensed under [Creative Commons Attribution 4.0 International](LICENSE)
(CC BY 4.0). You may share and adapt this material with attribution.
