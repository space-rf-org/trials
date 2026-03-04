# pki-tools

A suite of seven command-line tools covering the X.509 PKI lifecycle: certificate generation, format conversion, policy enforcement, monitoring, TLS inspection, digital signatures, and hybrid encryption. Written in C11 against OpenSSL 3.x with no other dependencies.

**Author:** Chiradip Mandal <chiradip@chiradip.com>

## Tools

| Binary | Purpose |
|--------|---------|
| `pki-tool` | Certificate authority management — CA init, Sub-CAs, cert issuance, CSRs, CRLs, revocation, renewal |
| `cert-monitor` | Certificate expiry scanning — files, directories, serial databases, live TLS endpoints |
| `tls-probe` | TLS handshake inspection — protocol version, cipher suite, chain, verification, mTLS |
| `keystore-tool` | Format conversion — PEM, DER, PKCS#12 with split, merge, convert, and auto-detection |
| `cert-lint` | Policy validation — enforce key size, validity, extensions, algorithms, SAN, self-signed rules |
| `sign-tool` | Detached CMS/PKCS#7 signatures — sign and verify with configurable hash and format |
| `secret-tool` | Hybrid encryption via CMS EnvelopedData — multi-recipient encrypt/decrypt |

All tools share a common interface: `--output-format json|text` and `--env-prefix PREFIX` for passphrase resolution via environment variables.
