# 🎨 SaveSoft Wallet Selector Kit

A zero-dependency, embeddable UI toolkit that lets **any dApp or platform** fully customize the wallet connection experience — from branding and layout to wallet ordering, filtering, and behavior — all without forking or maintaining UI code.

## ✨ Why Use This?

Standard wallet connectors often force generic modals, fixed wallet orders, or limited theming — breaking brand consistency and user trust. The Wallet Selector Kit puts *you* in control:

- ✅ Match your app’s colors, fonts, icons, and tone — down to hover states and animations  
- ✅ Curate which wallets appear (and in what order) — e.g., prioritize mobile wallets on iOS, show hardware options only on desktop  
- ✅ Hide, rename, or add custom descriptions per wallet (e.g., “Recommended for beginners” or “Supports Solana NFTs”)  
- ✅ Inject contextual guidance (“Connect with MetaMask to access exclusive rewards”)  
- ✅ Localize labels, tooltips, and errors in 12+ languages — or bring your own  

## 🛠️ Core Capabilities  

- **Declarative Config**: Define everything in a simple JSON/YAML config — no JS logic required  
  ```yaml
  theme:
    primary: "#4f46e5"
    borderRadius: "12px"
    logo: "/assets/myapp-logo.svg"

  wallets:
    - id: "metamask"
      label: "MyApp Wallet"
      description: "Fast & secure — built for speed"
      priority: 1
      visible: true

    - id: "ledger"
      label: "Ledger Hardware"
      description: "Maximum security for long-term holders"
      visible: { platform: "desktop" }


Framework-Agnostic: Works with React, Vue, Svelte, plain HTML/JS — or as a standalone iframe

Lightweight: <8 KB gzipped; no external dependencies

Privacy-First: Zero telemetry; no tracking; all logic runs client-side

Extensible: Add custom wallet buttons (e.g., “Email Login”, “Passkey”, “In-App Wallet”) via plugin hooks
## 🚀 Quick Start
```
<!-- Embed in any page -->
<div id="wallet-selector"></div>

<script src="https://cdn.savesoft.online/selector/v1.2.0/bundle.js"></script>
<script>
  SaveSoftSelector.init({
    container: '#wallet-selector',
    configUrl: '/config/wallets.yaml', // or inline object
    onConnect: (account) => console.log('Connected:', account)
  });
</script>
```
🔗 https://selector.savesoft.online/demo | 📄 https://docs.savesoft.online/selector/config | 🐙 https://github.com/savesoft-labs/selector-kit