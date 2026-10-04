# Contributing to TrustMint

Thanks for considering a contribution. TrustMint is an early-stage open-source project exploring reusable Soroban patterns for real-world asset applications on Stellar. Contributions that improve correctness, documentation, accessibility, and developer experience are welcome.

## Get the project running

Prerequisites: Rust, the `wasm32-unknown-unknown` target, Stellar CLI, and Node.js 20 or newer.

```bash
git clone https://github.com/zeemscript/TrustMint
cd TrustMint
rustup target add wasm32-unknown-unknown
```

For contract work:

```bash
cargo fmt --all -- --check
cargo clippy --all --all-targets -- -D warnings
cargo test --features testutils
```

For dashboard work:

```bash
cd frontend
npm install
npm run lint
npm run build
```

The dashboard needs deployed contract IDs in `frontend/.env` for network-backed workflows. Never commit `.env` files, secrets, private keys, or personal identity data.

## Propose a change

1. Open or find an issue to discuss substantial changes, especially contract interface or storage changes.
2. Create a focused branch, for example `feat/property-claims` or `fix/expiry-check`.
3. Include or update tests for behavior changes and update documentation when user-visible behavior changes.
4. Open a pull request with the motivation, implementation summary, test commands and results, and any migration or security considerations.

Contract changes deserve particular care: explain authorization assumptions, state changes, failure behavior, and any effect on existing deployments. Do not include real customer data in examples or fixtures.

## Where help is useful

- Contract correctness and SEP-41 compatibility
- Soroban integration and lifecycle coverage
- Clear deployment and operator documentation
- Dashboard usability and accessibility
- TypeScript SDK examples and API documentation

## Versioning

TrustMint uses Semantic Versioning for tagged contract-suite releases. Changes to a contract’s public interface or persistent storage can affect deployed integrations and should be discussed before implementation. When preparing a release, update the relevant contract crate versions and document user-visible changes in [CHANGELOG.md](CHANGELOG.md).

## Community standards

Participation is governed by the [Code of Conduct](code-of-conduct.md). For security vulnerabilities, follow the private process in [SECURITY.md](SECURITY.md) instead of opening a public issue.
