<div align="center">

# The Secret Handshake

### SSL/TLS — Computer Networks · Unit V · Security

An interactive 18-slide presentation explaining how SSL/TLS helps two endpoints communicate securely over a public network.

![HTML5](https://img.shields.io/badge/HTML5-e34f26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572b6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-f7df1e?style=flat-square&logo=javascript&logoColor=black)
![Dependencies](https://img.shields.io/badge/runtime-dependency--free-success?style=flat-square)

</div>

---

## Overview

**The Secret Handshake** is a browser-based teaching presentation for the SSL/TLS topic in Computer Networks. It introduces the security problem with plain HTTP, explains the cryptographic building blocks used by TLS, walks through certificates and trust, demonstrates the TLS 1.3 handshake, and connects the ideas to real-world protocols and attacks.

The original presentation was supplied as a single HTML file. This repository version keeps the presentation content and JavaScript behavior intact while separating the embedded stylesheet and script into dedicated files for easier maintenance.

## Highlights

- **18 interactive slides** organized into five learning sections.
- **Animated security visuals**, including the title illustration, particle-network background, moving packets, and the TLS handshake sequence.
- **Cryptography learning demos** for a Caesar shift, small RSA example, Diffie–Hellman shared-secret calculation, and SHA-256 fingerprint changes.
- **Certificate and trust interactions** for exploring certificate fields, a CA trust chain, and a tampered-message concept.
- **TLS demonstrations** for the TLS 1.3 handshake, TLS 1.2 vs 1.3, record transfer concept, and man-in-the-middle scenarios.
- Responsive layout, progress indicator, slide rail, keyboard controls, touch navigation, and fullscreen mode.
- No framework, package manager, or build step is required.

## Presentation Structure

| Section | Slides | Topics |
|:--|:--:|:--|
| **01 · The Problem** | 1–4 | Introduction, plain HTTP, privacy/integrity/authenticity, TLS position and history |
| **02 · The Toolkit** | 5–9 | Symmetric encryption, public/private keys, RSA, Diffie–Hellman, SHA-256 hashing |
| **03 · Trust** | 10–12 | Digital signatures, website certificates, certificate-authority trust chain |
| **04 · The Handshake** | 13–15 | TLS 1.3 handshake, TLS 1.2 vs 1.3, TLS record protocol |
| **05 · Real World** | 16–18 | Attacks and defences, protocols and tools, summary |

## Run the Presentation

### Option 1 — Open directly

1. Download or clone this repository.
2. Open `index.html` in a modern desktop browser.

Most slides and demonstrations work when opened directly. The SHA-256 demonstration uses the browser Web Crypto API; some browsers restrict this API on `file://` pages.

### Option 2 — Run with a local web server (recommended)

Using Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Or open the project folder in VS Code and use the Live Server extension.

## Controls

| Input | Action |
|:--|:--|
| `→`, `↓`, `Space`, `PageDown` | Next slide |
| `←`, `↑`, `PageUp` | Previous slide |
| `F` | Toggle fullscreen |
| Mouse wheel | Move between slides |
| Touch swipe | Move between slides on touch devices |
| Bottom navigation buttons | Previous / next / fullscreen |
| Right-side dots | Jump to a specific slide |
| Interactive controls on slides | Change the demo input or replay a demonstration |

## Interactive Demonstrations

| Slide | Demonstration | Educational purpose |
|:--:|:--|:--|
| 4 | Add/remove TLS in the protocol stack | Show where TLS sits in the presented stack |
| 5 | Caesar-shift control | Demonstrate a simple substitution shift |
| 7 | RSA message slider | Calculate a toy modular-exponentiation example |
| 8 | Diffie–Hellman sliders | Show both parties deriving the same modular shared value |
| 9 | Editable SHA-256 input | Show how a changed message produces a different fingerprint |
| 10 | Tamper toggle | Illustrate the idea of signature verification failure |
| 11 | Certificate fields | Explore the role of certificate information |
| 12 | Break/repair trust chain | Illustrate why a broken chain causes a browser warning |
| 13 | Replay handshake | Animate the browser/server exchange |
| 15 | Send securely | Visualize a message being represented as transmitted data and restored |
| 16 | HTTP / HTTPS / fake-certificate selector | Compare what an on-path observer and browser see in each scenario |

## Technical Notes and Demonstration Limits

This is an **educational presentation**, not a production TLS implementation or a cryptographic testing tool.

- The RSA demonstration uses deliberately tiny values (`p = 5`, `q = 11`) so the arithmetic can be followed by hand. It is not secure RSA.
- The Diffie–Hellman demonstration uses a small toy prime and generator for visibility. It is not secure key exchange.
- The SHA-256 slide calls the browser's Web Crypto API to calculate a real SHA-256 digest when the page is served in a supported secure context.
- The signature tampering control is a visual teaching simulation; it does not create or verify a real digital signature.
- The record-transfer animation is a visual simulation; it does not encrypt application data with AES or establish a real TLS connection.
- The handshake sequence is an explanatory animation. It does not perform a network handshake with a server.

These boundaries are documented so the visual demonstrations are not mistaken for live cryptographic operations.

## Project Structure

```text
ssl-tls-computer-networks-project/
├── index.html                     # Presentation document and slide mount points
├── assets/
│   ├── css/
│   │   └── styles.css             # Theme, layout, responsive rules and animations
│   ├── js/
│   │   └── app.js                 # Slide data, navigation, interactions and animation logic
│   └── screenshots/
│       └── README.md              # Notes for adding repository preview images
├── docs/
│   └── PROJECT_OVERVIEW.md        # Project architecture and content notes
├── .gitignore
└── README.md
```

The JavaScript is intentionally kept as one runtime file in this first repository organization. The original slide templates and interactions share state and DOM references; splitting them further without a regression test could change behavior. The stylesheet and runtime are already separated from the HTML, so future refactoring can be done incrementally.

## Team

The presentation source lists the following group members:

- Saurabh Raj Shekhar
- Sumit Gupta
- Gaurav Kumar

**Course:** Computer Networks · **Unit:** V — Security

> Before making the repository public, review the team details displayed inside the presentation and remove any personal identifiers that the contributors do not want to publish.

## Deployment to GitHub Pages

1. Create a GitHub repository and upload the contents of this project folder.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Select the `main` branch and `/ (root)` folder, then save.
5. After GitHub Pages finishes deploying, the presentation will be available at the Pages URL shown in repository settings.

## License

No license file is included because the contributors' preferred reuse terms have not been specified. Agree on a license as a team before adding one or publishing the repository for reuse.

---

<div align="center">

*From an open postcard to a trusted, encrypted connection.*

</div>
