# Project Overview — The Secret Handshake

## Purpose

This project is an interactive academic presentation for SSL/TLS in Computer Networks (Unit V — Security). Its teaching path is:

1. Establish the risk: plain HTTP can expose or allow modification of data in transit.
2. Introduce the desired security properties: privacy, integrity, and authenticity.
3. Explain the cryptographic toolkit: symmetric encryption, public/private keys, RSA, Diffie–Hellman, and hashing.
4. Explain identity and trust: digital signatures, certificates, and certificate authorities.
5. Walk through the TLS 1.3 handshake and compare TLS 1.2 with TLS 1.3.
6. Explain protected records, common attack scenarios, and other protocols that use TLS.

## Runtime Architecture

- `index.html` contains the document metadata, page-level controls, the presentation container, and external file references.
- `assets/css/styles.css` contains the visual theme, slide layout, component styles, responsive rules, and CSS animations.
- `assets/js/app.js` builds the 18 slides and manages navigation, interactive examples, SVG/canvas animations, and the title illustration.

The app uses browser-native APIs and does not require a bundler or package installation.

## Browser APIs

- Canvas 2D for the animated particle network.
- SVG for diagrams and moving visual elements.
- Web Crypto API for the SHA-256 digest demonstration.
- BigInt for modular exponentiation in the toy RSA and Diffie–Hellman examples.
- Fullscreen API for presentation mode.

## Content Fidelity

The slide wording, sequence, examples, and teaching framing are carried over from the supplied HTML source. The repository packaging separates presentation files but does not intentionally rewrite the educational content.

## Important Limitations

Some interactions are intentionally illustrative. The simulated signature check, record transfer, and handshake animation do not constitute real cryptographic signing, AES encryption, or a live TLS session. The toy RSA and Diffie–Hellman parameter values are too small for security. Refer to the README for the per-demo distinctions.
