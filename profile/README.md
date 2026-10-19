<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/logo-primary-dark.svg">
    <img alt="CypherGrid" src="./assets/logo-primary-light.svg" width="320">
  </picture>
</p>

<p align="center"><sub><b>English</b> · <a href="https://github.com/CypherGrid/.github/blob/main/profile/README.pt-BR.md">Português (Brasil)</a></sub></p>

<p align="center">
  <strong>Continuous authentication through behavioral biometrics.</strong><br>
  Know it is still the same person, from login to the last transaction.
</p>

---

## The problem

Authentication happens once, at login. Fraud happens after it.

Account takeover, social engineering, coerced transactions and automated
scripts all operate inside sessions that have already passed every
authentication factor. Passwords, one-time codes and device checks confirm
who opened the session. They say nothing about who is operating it a few
minutes later.

## What we build

**CypherGrid Collect** verifies identity continuously and silently, based on
*how* a person interacts with an application, not on what they type.

- **Behavioral DNA.** A lightweight SDK observes the shape of the
  interaction - typing rhythm, touch and pointer dynamics, device motion,
  navigation cadence - and builds a behavioral profile for each user over
  time.
- **Risk scoring.** Every session is scored against that profile and against
  signs of automation, so the platform can tell the legitimate user apart from
  a third party, a script or an agent driving the application.
- **Checkpoints and actions.** Integrators mark the sensitive moments of their
  own flows - login, payments, adding a beneficiary, changing a password - and
  define simple rules for each: for example, request step-up authentication
  when risk is high.
- **Verifiable decisions.** Each evaluation returns a short-lived, signed
  decision token that the integrator's backend verifies before authorizing the
  operation. The decision is a control on the server, not a hint on the
  device.
- **No extra friction.** Legitimate users see no new steps. Friction is added
  only where the risk justifies it.

CypherGrid delivers the behavioral signal and the decision at each
checkpoint. It is designed to complement, not replace, the fraud and risk
engines our customers already run.

## Privacy by design

Behavioral data is sensitive, and the platform is built around that fact.

- **Shape, not content.** The SDK never captures what is typed, pasted or
  displayed - only timing and movement characteristics.
- **Pseudonymous by default.** Users and devices are identified by
  per-customer pseudonymous identifiers.
- **Data minimization.** Raw interaction data is retained only when a session
  requires investigation, and for a limited period.
- **Built for regulated environments.** Designed with the Brazilian LGPD and
  the European GDPR in mind, for organizations that must justify every piece
  of personal data they process.

## Platforms

| Platform | Status |
|---|---|
| Web - JavaScript, React, Vue, Angular | **Beta** · fully functional |
| Android - native Kotlin | In development |
| iOS - native Swift | Planned |

Capture and feature extraction live in a single Rust core shared by every
SDK, so the same behavior produces the same signal on every platform.

## Who it is for

Banks, payment institutions, fintechs and any digital product where a single
compromised session is expensive: financial transactions, account recovery,
credential changes, onboarding and high-value operations.

## Early access

CypherGrid is in **early access**, working with a small group of design
partners to validate the platform in real production flows. Contact details
will be published here soon.

---

<p align="center"><sub>© CypherGrid · São Paulo, Brazil</sub></p>
