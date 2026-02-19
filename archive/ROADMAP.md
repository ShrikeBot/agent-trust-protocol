# ATP Roadmap

## Current: Phase 1 (Bootstrap)

### Completed
- [x] Spec v0.4 finalized
- [x] atp-cli: identity create/verify/show/publish
- [x] atp-registry: GitHub mirror structure
- [x] ShrikeBot identity (GPG + wallet signed, IPFS published)

### In Progress
- [ ] Testnet inscription (blocked on testnet BTC)
- [ ] Mirror bot (auto-sync Bitcoin → GitHub)

### Pending
- [ ] Mainnet inscription (~$5)
- [ ] Explorer API
- [ ] Web frontend

---

## Phase 2: Infrastructure

- [ ] **Own Bitcoin node** — Move from public APIs to self-hosted node for trustless verification
- [ ] Attestation workflow in CLI
- [ ] Receipt signing flow
- [ ] IPFS pinning service integration

---

## Phase 3: Scale

- [ ] Explorer API with search
- [ ] Graph visualization  
- [ ] API tiers for sustainability
- [ ] Multiple community mirrors

---

## Infrastructure Notes

**Current:** Using Blockstream public API for Bitcoin queries and broadcast.  
**Future:** Run own Bitcoin node for maximum trustlessness. Sam will build when necessary.

> "At some point we should switch to trusting the most reliable source of truth, which is running our own bitcoin node." — Sam, 2026-02-03

---

## Decision Log

| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-02-03 | Start with public APIs | Faster bootstrap, node can come later |
| 2026-02-03 | Use OP_RETURN over inscriptions for MVP | Simpler, cheaper, still proves existence |
| 2026-02-03 | GitHub as mirror layer | Free, accessible, clonable, version history |
