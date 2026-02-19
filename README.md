# Agent Trust Protocol

Permanent, cryptographic identity for AI agents — anchored on Bitcoin.

ATP lets agents create verifiable identities, build trust through attestations and receipts, and rotate or revoke keys without losing their history. Every document is inscribed on Bitcoin: immutable, censorship-resistant, and independent of any platform or authority.

## How It Works

```
Agent creates keypair
  → signs identity document
    → inscribes on Bitcoin (permanent)
      → anyone can verify (no trust required)
```

**Two layers:**
- **Bitcoin** — source of truth. Identity documents, attestations, receipts, and revocations are inscribed as Taproot assets.
- **Explorers** — fast cache. Index the chain, resolve identity state, serve queries via API.

## Specification

| Document | Status | Description |
|----------|--------|-------------|
| [**ATP v1.0**](./atp-v1.0.md) | Review | Core protocol — identity, supersession, revocation, expiry, attestations, receipts, heartbeats, publications |

ATP v1.0 requires implementation of all eight core AIPs. There are no optional components.

## AIPs

AIPs (ATP Improvement Proposals) define individual protocol mechanisms. The specification assembles them into versioned releases.

### Core (ATP v1.0)

| AIP | Title | Status |
|-----|-------|--------|
| [AIP-01](./aip-01.md) | Identity Documents & Signing | Review |
| [AIP-02](./aip-02.md) | Supersession | Draft |
| [AIP-03](./aip-03.md) | Revocation | Draft |
| [AIP-04](./aip-04.md) | Key Expiry & Validity Windows | Draft |
| [AIP-05](./aip-05.md) | Attestations & Attestation Revocation | Draft |
| [AIP-06](./aip-06.md) | Receipts | Draft |
| [AIP-07](./aip-07.md) | Heartbeats | Draft |
| [AIP-08](./aip-08.md) | Publications | Draft |

### Other

| AIP | Title | Status |
|-----|-------|--------|
| [AIP-09](./aip-09.md) | Explorer API | Draft |
| [AIP-10](./aip-10.md) | A2A Integration | Draft |
| [AIP-11](./aip-11.md) | Nostr Identity Bridging | Draft |

## Tools

| Project | Description |
|---------|-------------|
| [atp-cli](https://github.com/atprotocol-org/atp-cli) | Command-line tools for creating, signing, verifying, and inscribing ATP documents |

## Key Properties

- **Permanent** — inscribed on Bitcoin, can't be erased or censored
- **Self-sovereign** — no registration, no approval, no gatekeepers
- **Verifiable** — anyone can check signatures without trusting a third party
- **Recoverable** — rotate keys via supersession while preserving identity history
- **Destructible** — revoke an entire identity chain if keys are compromised

## Contributing

AIPs follow a Draft → Review → Final lifecycle. To propose a new AIP, use the [template](./TEMPLATE.md).

## Links

- **Website:** [atprotocol.io](https://atprotocol.io)
- **CLI:** [atprotocol-org/atp-cli](https://github.com/atprotocol-org/atp-cli)

## License

MIT
