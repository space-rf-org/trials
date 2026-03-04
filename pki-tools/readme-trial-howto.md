# pki-tools Trial Edition

## Getting Started

Extract the archive and place the binaries somewhere on your `PATH`:

```bash
tar xzf pki-tools-trial-linux-x86_64.tar.gz
sudo cp pki-tool cert-monitor tls-probe keystore-tool \
        cert-lint sign-tool secret-tool /usr/local/bin/
```

Or run directly from the extracted directory:

```bash
./pki-tool init-ca --cn "My Root CA" --days 3650 --out ./my-ca
```

### Requirements

- Linux x86_64
- OpenSSL 3.x shared libraries (`libssl.so.3`, `libcrypto.so.3`)

Install on Debian/Ubuntu:
```bash
sudo apt install libssl3
```

Install on RHEL/Fedora:
```bash
sudo dnf install openssl-libs
```

## Included Tools

| Tool             | Purpose                                        |
|------------------|------------------------------------------------|
| `pki-tool`       | Certificate lifecycle (CA, issue, verify, CRL) |
| `cert-monitor`   | Certificate expiration monitoring               |
| `tls-probe`      | TLS endpoint inspection                         |
| `keystore-tool`  | PKCS#12 keystore management                     |
| `cert-lint`      | Certificate standards compliance checking       |
| `sign-tool`      | CMS/PKCS#7 digital signatures                   |
| `secret-tool`    | CMS envelope encryption/decryption              |

Run any tool without arguments to see its usage:

```bash
./pki-tool
./cert-lint
```

## Permitted Environment

**This trial edition is licensed for use in development environments only.**

You may use the Software on developer workstations and local development
machines for the sole purpose of evaluation and development-time testing.
Use of the Software in any other environment — including but not limited to
QA, staging, testing, pre-production, production, or any shared/deployed
infrastructure — is strictly prohibited and constitutes a violation of this
license.  A full licensed build is required for all non-development use.

## Trial Limits

This trial edition permits **100 combined invocations** across all 7 tools.
Every run of any tool counts toward the shared limit.

- **Invocations 1-89**: tools run normally, no messages.
- **Invocations 90-100**: tools run normally, a warning is printed to stderr:
  ```
  Trial warning: 93/100 invocations used.
  ```
- **After 100**: all tools refuse to run:
  ```
  Trial expired: 100/100 invocations used. Please purchase a license.
  ```

Usage state is stored locally at `~/.pki-tools/.usage.dat`.

## Purchasing a License

To obtain an unrestricted licensed build, contact:

  Chiradip Mandal <chiradip@chiradip.com>

---

## End-User License Agreement (EULA)

**IMPORTANT -- READ CAREFULLY BEFORE USING THIS SOFTWARE.**

By extracting, installing, copying, or otherwise using pki-tools Trial
Edition ("the Software"), you agree to be bound by the terms of this
Agreement.  If you do not agree, do not use the Software and delete all
copies immediately.

### 1. Grant of License

You are granted a limited, non-exclusive, non-transferable, revocable
license to use the Software solely for evaluation purposes in development
environments, subject to the usage limits embedded in the Software.  This
license is personal to you and may not be sublicensed.

**The Software may only be used on developer workstations and local
development machines.**  Use in any test, QA, staging, pre-production,
production, or other non-development environment is expressly prohibited and
constitutes a material breach of this Agreement.

### 2. Usage Limits

The Software is limited to 100 combined invocations across all included
tools.  You shall not circumvent, disable, tamper with, or attempt to bypass
this usage limitation by any means, including but not limited to:

- Modifying, patching, or reverse-engineering the binaries.
- Tampering with, deleting, replacing, or forging the usage tracking data.
- Using debuggers, disassemblers, or instrumentation tools to alter runtime
  behavior.
- Deploying the Software in a manner designed to reset or evade the counter.

Any attempt to exceed or circumvent the permitted usage constitutes a
material violation of this Agreement.

### 3. Restrictions

You shall NOT:

- Deploy or use the Software in any test, QA, staging, pre-production,
  production, or other non-development environment.
- Use the Software beyond the trial invocation limit without purchasing a
  license.
- Distribute, sublicense, rent, lease, or lend the Software to any third
  party.
- Copy, reproduce, or redistribute the Software except as a single backup
  for your own use.
- Reverse-engineer, decompile, or disassemble the Software, except to the
  extent expressly permitted by applicable law.
- Remove or alter any proprietary notices, labels, or marks.
- Use the Software for any unlawful purpose.

### 4. Export Compliance

The Software contains cryptographic functionality.  You are solely
responsible for determining whether your use, possession, import, or export
of the Software complies with all applicable export control laws,
regulations, and sanctions, including but not limited to:

- United States Export Administration Regulations (EAR)
- European Union Dual-Use Regulation (EC 428/2009)
- The Wassenaar Arrangement
- Any local laws governing the use, import, or export of cryptographic
  software in your jurisdiction

You shall not export, re-export, or transfer the Software to any country,
entity, or person prohibited by applicable export control laws.  It is your
responsibility to obtain any required export permits or licenses before
distributing or deploying the Software.

### 5. Intellectual Property

The Software is the proprietary property of Chiradip Mandal and is protected
by copyright law and international treaty provisions.  This Agreement does
not convey any ownership interest in the Software.  All rights not expressly
granted herein are reserved.

### 6. No Warranty

THE SOFTWARE IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE, AND NONINFRINGEMENT.  IN NO EVENT SHALL
THE AUTHOR BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY ARISING FROM
THE USE OF THE SOFTWARE.

### 7. Limitation of Liability

IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY INDIRECT, INCIDENTAL,
SPECIAL, CONSEQUENTIAL, OR PUNITIVE DAMAGES, OR ANY LOSS OF PROFITS,
REVENUE, DATA, OR USE, WHETHER IN AN ACTION OF CONTRACT, TORT, OR OTHERWISE,
ARISING OUT OF OR IN CONNECTION WITH THIS AGREEMENT OR THE USE OF THE
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGES.

### 8. Piracy and Unlawful Use

Piracy, unauthorized reproduction, distribution, or any other unlawful use
of the Software is strictly prohibited and may subject you to civil and
criminal penalties under applicable law.

### 9. Termination

This license is effective until terminated.  It terminates automatically if
you fail to comply with any term of this Agreement.  Upon termination you
must destroy all copies of the Software in your possession.

### 10. Governing Law

This Agreement shall be governed by and construed in accordance with
applicable law.  You consent to the jurisdiction of the courts in the
jurisdiction of the author's principal place of business for resolution of
any disputes.

---

Copyright (c) 2025 Chiradip Mandal. All rights reserved.
