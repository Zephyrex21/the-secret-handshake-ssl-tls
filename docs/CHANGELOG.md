# Update Notes

## Presentation refinement

- Slide 6 now runs its three-stage reveal only on the first visit. A Replay animation button restarts it on demand. Its content distinguishes certificate-based identity/signatures from ephemeral key agreement and symmetric traffic encryption.
- Slide 18 now uses a balanced three-column, two-row arrangement for its six summary cards, with responsive layouts for smaller viewports and a tidy contributor row.
- Updated TLS explanations across the deck: public-key signatures versus key agreement, hash versus authenticated integrity, certificate expiry versus private-key compromise, TLS 1.3 handshake messages, TLS 1.2/1.3 round trips, AEAD record protection, 0-RTT replay risk, and HTTP/3 over QUIC.
- Improved keyboard navigation so arrow keys operate focused controls rather than changing slides, and changed the slide rail to labelled, keyboard-focusable buttons.
- Refined slide fitting and long-content wrapping to prevent visible content from extending beyond the viewport.
- Updated README and project documentation; refreshed runtime SHA-256 values in `source-manifest.json`.

## Validation

- JavaScript syntax checked with Node.js.
- Browser-rendered all 18 slides at desktop, laptop and phone viewport sizes; no visible content overflow was detected.
- Verified slide 6 starts three reveal animations on first entry, does not restart them on revisiting, and starts them again when Replay is clicked.
- Verified the TLS 1.3 handshake timeline has eight distinct messages and the presentation emits no browser page errors during the interaction checks.
