# Skycoin Next Gen — Product Status

Canonical SKYCOIN4444 branch **#54**.

## Current evidence

This repository contains an existing TypeScript/React application with an Express server, tRPC, Drizzle/MySQL integration, Web3 dependencies, Vitest tests, and production build scripts. This branch does not rewrite that application or claim integrations are live merely because code or dependencies exist.

## Verification gates

A merge candidate must pass, on the exact submitted head:

1. frozen pnpm dependency installation;
2. TypeScript `pnpm check`;
3. `pnpm test`;
4. `pnpm build`;
5. production dependency audit at high severity.

## Explicit boundaries

Until independently verified, this checkpoint does **not** claim:

- a deployed production environment;
- a reachable production database;
- working OAuth or external identity providers;
- live wallet, chain, payment, AI, email, storage, or other third-party providers;
- production secrets or key custody;
- migrations applied to a production database;
- TLS, monitoring, backups, restore drills, HA, or disaster recovery;
- audited smart contracts or financial/compliance certification.

Any feature requiring those systems must fail clearly or remain unavailable when its dependency is absent. Test fixtures and mock data are not live-provider evidence.

## Status

**Engineering beta / stabilization checkpoint.** Merge only after the exact PR head passes every declared CI gate.