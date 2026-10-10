# Lifecycle reference webapp

**Status:** Initial design on branch `feat/lifecycle-reference-site`. The site is static HTML, CSS, and JavaScript in [site/index.html](../../site/index.html).

## What it teaches

1. The company-wide lifecycle and core invariants.
2. The universal eight stages and typical stage outputs.
3. The eight shared states, separately from stage.
4. Typical state transitions, guards, and evidence.
5. Animated end-to-end department journeys curated to BABAI: technology, marketing, operations, and sales.

The department diagrams animate a path and allow each stage to be selected for its action, evidence, and acceptance focus. Motion is decorative; reduced-motion preferences are respected. Examples are guides, not new policy. The transition roles and exact evidence gates stay subject to the reviewed contract in [Bulb #7](https://github.com/nekurama/Bulb/issues/7).

## BABAI context used

- The restaurant-first WhatsApp-native local-business platform and its product boundaries.
- The first-ten-restaurant pilot and founder-led validation.
- Channel/menu/order/payment/fulfillment and human-takeover flows.
- The implementation roadmap and human-authorized AI execution principles.

Source context: [Bulb #1](https://github.com/nekurama/Bulb/issues/1), [#2](https://github.com/nekurama/Bulb/issues/2), and [#4](https://github.com/nekurama/Bulb/issues/4).

## Hosting

**Target address:** `https://sdlc.nekurama.com`.

The repository is public and GitHub Pages is enabled with the `github-actions` publishing source. The workflow uploads only `site/` and deploys it to GitHub Pages on pushes to `main`; it does not deploy pull requests. Until the custom domain is connected, the site is available at `https://nekurama.github.io/sdlc/` after a successful deployment.

The DNS name `sdlc.nekurama.com` did not resolve when checked on 2026-10-10, so the custom address cannot be confirmed yet. At the DNS provider for `nekurama.com`, add a `CNAME` record named `sdlc` pointing to `nekurama.github.io`. Then set `sdlc.nekurama.com` as the repository's Pages custom domain and wait for GitHub's DNS check and HTTPS provisioning. Verify `nekurama.com` for the GitHub organization before use to reduce domain-takeover risk. With this custom Actions workflow, configure the custom domain in repository Pages settings; a `CNAME` file is not required.

The published site is public because the repository and GitHub Pages site are public. Keep its content suitable for public viewing.
