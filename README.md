# The Artists' Collective — Studio (Usernode dApp)

The artist side of **The Artists' Collective**, a community-owned art gallery, built for the Usernode Dapp Hackathon.

Buyers use the public website (fiat checkout, no wallet). **Artists** use this dApp inside the Usernode app: their on-chain identity, their stake in the gallery, the **governance vote** (signed with their own key), the treasury, and every sale verified on the ledger.

## How it works
- Single self-contained `index.html` + the Usernode bridge (`usernode-bridge.js`).
- A **chain adapter** calls the real bridge (`getNodeAddress` / `sendTransaction` / `getTransactions`) when running inside the Usernode app, and falls back to in-page mock when opened standalone — so it's demoable on its own and deploy-ready for the app.

## Run locally
Open `index.html` (uses mock data), or serve with the Usernode dapp-starter's `node server.js --local-dev` for mock-endpoint parity.

## Status
Prototype. Identity + ledger reads go live in-app; on-chain **writes** (artist enrolment, the user-key governance vote, sale records) are being wired to the chain next.
