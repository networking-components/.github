# networking-components organization handbook

> Shared operating defaults for repositories maintained under **networking-components**. Repository-local policy may strengthen these rules but should not silently weaken them.

## Mission

networking-components maintains reusable networking libraries, protocol implementations, gateways, proxies, and infrastructure components. This `.github` repository is the canonical home for shared policy, reusable templates, community health files, and planning links.

## Repository contract

Each active repository must document purpose, ownership, maturity, supported protocols and platforms, development and test commands, authoritative wire and configuration formats, release and rollback procedures, compatibility policy, and GitHub Project/Linear links. Networking components should also document connection lifecycle, framing, ordering, backpressure, timeouts, retries, idempotency, authentication, encryption, resource limits, observability, and degraded modes.

## Change workflow

1. Anchor work in an issue, Linear item, or documented maintenance objective.
2. Keep branches and pull requests focused.
3. Explain motivation, scope, protocol and compatibility risk, validation, migration, and rollback.
4. Test connect, disconnect, reconnect, timeout, packet loss, reorder, duplicate, overload, malformed input, and partial-failure paths as relevant.
5. Resolve conflicts semantically by reconstructing both sides' intent.
6. Prefer squash merges for focused work unless commit structure materially improves auditability.

## Evidence, security, and documentation

Pull requests should include reproducible commands, protocol fixtures or captures sanitized of private data, expected and observed behavior, negative-path and load evidence, documentation updates, and CI or local-equivalent results. Never commit credentials, private keys, production captures, or sensitive logs. Follow `SECURITY.md` for private reporting. Keep wire formats, limits, compatibility, trust boundaries, and important protocol and operational decisions explicit.

## Planning ownership

GitHub owns code, reviews, checks, releases, and delivery evidence. Linear owns priority, dependencies, sequencing, and cross-project planning. The organization GitHub Project is the cross-repository execution view; see `PROJECTS.md` for routing details.

## Organization health

- [ ] Profiles, descriptions, topics, and READMEs are current.
- [ ] Community health files and reusable issue/PR guidance are present.
- [ ] Protocols, lifecycle, framing, limits, retries, backpressure, security, and degraded modes are documented.
- [ ] Required checks cover malformed traffic, failure, load, compatibility, security, and supply-chain risk.
- [ ] Stale repositories are archived or clearly marked.
- [ ] GitHub Project and Linear links resolve and reflect completed work.
