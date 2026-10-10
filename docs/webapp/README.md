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

A custom GitHub Actions workflow uploads only `site/` and deploys it to GitHub Pages on pushes to `main`. It does not deploy pull requests.

**Visibility blocker:** GitHub currently reports that Pages is unavailable while this repository is private unless the organization upgrades its plan. Making the repository public would expose the published site. Do not merge/deploy until the team chooses a visibility route and Pages is enabled accordingly.

For an internal reference, prefer private Pages access through an eligible GitHub Enterprise plan. If public hosting is chosen, first review every page and example for information suitable for public release.
