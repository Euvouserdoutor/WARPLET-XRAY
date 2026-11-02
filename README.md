# Donut Factory — Farcaster Mini App Prototype

A React and Vite experiment for generating personalized donut artwork from Farcaster profile information. The current app title in `src/App.tsx` and `index.html` is **Donut Factory**. The repository retains its historical name, `WARPLET-XRAY`.

> **Development status:** Experimental source code, not a verified live service. Wallet-connected, AI-generation and onchain features require their own configuration and testing. No production-readiness claim is made here.

## What is in this repository?

| Component | Implementation |
| --- | --- |
| User interface | React 18, TypeScript and Vite |
| Farcaster integration | Mini app SDK and profile information |
| Artwork workflow | Personalized donut prompt and image-generation services |
| Wallet interaction | Wagmi and Viem integrations |
| Onchain-related modules | Contract interaction and metadata upload code; not validated here |
| Owner view | Treasury-related UI code; not independently security-audited |

**Current implementation references:**
- [Main app](src/App.tsx) — title, mini app lifecycle and wallet connection flow
- [Donut builder](src/components/DonutMaker.tsx) — user input, artwork flow and status handling
- [Image generation](src/services/donutService.ts) — prompt generation
- [Owner panel](src/components/AdminPanel.tsx) — restricted interface code
- [Configuration](package.json) — available scripts and dependencies

## Local development

Use a compatible Node.js environment.

```bash
git clone https://github.com/Euvouserdoutor/WARPLET-XRAY.git
cd WARPLET-XRAY
npm ci
npm run dev
```

The development server is managed by Vite. The repository also defines these scripts:

```bash
npm run lint
npm run build
npm run preview
```

These commands are documented from `package.json`; successful installation, build and deployment have **not** been independently verified as part of this README update. External services and permissions may be required for optional features.

## Security and deployment notes

- **Do not commit API tokens, private keys or credentials.**
- Variables prefixed with `VITE_` are included in client-side builds; **do not store long-lived secrets in them**.
- Before public deployment, move any credential-requiring operations to a properly authenticated server-side service, review access controls, and test error handling.
- Verify the Farcaster manifest, remote image URLs, service configurations and onchain integrations against the intended deployment environment.
- Treat prototype screens and integration code as work in progress until tested.

## Contributing

Focused bug reports, documentation improvements and reproducible test cases are welcome. For a code contribution, open a pull request explaining the problem, the changes, and how they were validated. Avoid sharing credentials or other sensitive information in public issues.

## License

See [LICENSE](LICENSE).
