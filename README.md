# PKI Chain Validator

A fully client-side certificate chain validation tool designed for static hosting on GitHub Pages or Cloudflare Pages.

## Features

- Accepts pasted PEM certificate bundles
- Accepts uploaded `.pem`, `.crt`, `.cer`, and `.der` files
- Converts DER to PEM in the browser
- Auto-detects leaf, intermediate, and root certificates
- Validates chain consistency and signature path
- Flags likely root/intermediate family mismatch such as GlobalSign R5 vs E46
- Checks basic ECC leaf policy:
  - EC public key
  - 384-bit key size
  - `ecdsa-with-SHA256`
- Suggests likely bundle correction when the wrong root or intermediate is supplied
- Runs fully in the browser with no backend

## Files

- `index.html` — main application

## GitHub Hosting

1. Create a new repository on GitHub.
2. Upload `index.html` and this `README.md`.
3. Commit to the `main` branch.
4. If needed, enable GitHub Pages under repository settings.

## Cloudflare Pages Hosting

- Build command: leave empty
- Output directory: `/`

## Operational Note

This tool is intended for validation and triage support. For production assurance, confirm important trust decisions with OpenSSL or enterprise PKI validation tooling.
