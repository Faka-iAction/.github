## FAKA iAction

**Scan → interact → pay → outcome.**

FAKA iAction is a platform, being built, that lets an audience interact with a creator by scanning a QR code or opening a link. A **creator** is anyone with an audience: a DJ, a musician, a radio presenter, a podcaster. The creator decides what the audience can do. An audience member scans, picks what they want, pays if there is a price, and the creator responds. The audience member does not need to install an app or create an account.

**FAKA iRequest**, for song requests and similar, is the first product on the platform.

> **Nothing is live yet.** There is no running service and no app to download. The web app, the API and the mobile app are built and tested on developers' machines; none of it is deployed. Their public repositories show how the code is organised, not its implementation. See the [roadmap](https://github.com/Faka-iAction/docs-public/blob/main/ROADMAP.md) for what each milestone has and still needs.

### What a creator can offer

| Creator Action | For the audience member |
|---|---|
| **Request** | "I choose." Pick from what the creator made available, such as a song from tonight's playlist. |
| **Vote** | "We choose." Vote on options the creator set. |
| **Bid** | "I want priority." A paid offer, ranked against other bids. |
| **Shout-out** | A message for the creator to read out or display. |
| **Tip** | "Thank you." An amount you choose, with nothing owed in return. |

If a creator does not deliver something that was paid for, the money is refunded automatically. FAKA iAction holds no money and has no wallet. A licensed payment provider collects, holds and pays out the money, and the platform keeps the record.

### Start here

1. **[What is FAKA iAction?](https://github.com/Faka-iAction/docs-public/blob/main/WHAT_IS_FAKA_IACTION.md)** explains the idea in plain language, with worked examples.
2. **[MVP1 scope](https://github.com/Faka-iAction/docs-public/blob/main/MVP1_SCOPE.md)** lists what the first release includes and leaves out.
3. **[Architecture overview](https://github.com/Faka-iAction/architecture-public/blob/main/OVERVIEW.md)** covers the engineering design.
4. **[Glossary](https://github.com/Faka-iAction/docs-public/blob/main/GLOSSARY.md)** defines terms such as Creator Action, cool-off and pending balance.

### Repositories

| Repository | What it holds |
|---|---|
| [docs-public](https://github.com/Faka-iAction/docs-public) | Plain-language introduction, scope, roadmap and glossary |
| [architecture-public](https://github.com/Faka-iAction/architecture-public) | Architecture overview and design decisions |
| [contracts-public](https://github.com/Faka-iAction/contracts-public) | The contract-first approach: the API and event contracts that every backend follows |
| [api-symfony-public](https://github.com/Faka-iAction/api-symfony-public) | Reference implementation (Symfony / PHP): the web experience and the API. Public skeleton: structure and signatures |
| [api-spring-public](https://github.com/Faka-iAction/api-spring-public) | Backend in Spring Boot (Java), planned after the pilot |
| [api-dotnet-public](https://github.com/Faka-iAction/api-dotnet-public) | Backend in ASP.NET Core (C#), planned after the pilot |
| [api-python-public](https://github.com/Faka-iAction/api-python-public) | Backend in FastAPI (Python), planned after the pilot |
| [flutter-public](https://github.com/Faka-iAction/flutter-public) | Mobile app for Android and iOS. Public skeleton: structure and signatures |
| [ui-public](https://github.com/Faka-iAction/ui-public) | The design system shared by the web, the mobile app and the admin, and screenshots of every screen |
| [react-public](https://github.com/Faka-iAction/react-public) | Future React client, not part of the first release |
| [video-gen-public](https://github.com/Faka-iAction/video-gen-public) | Tooling that renders tutorial and explainer videos |

### How the project is built

- **Contract first.** The API and events are specified before any code, and every backend is tested against the same conformance fixtures.
- **One database, four backends.** Symfony is the reference implementation. Spring Boot, ASP.NET Core and FastAPI implement the same contract against the same database.
- **Web and mobile at parity.** A server-rendered web experience and a Flutter app, with the same rules and wording in both.
- **Built in public.** Each tutorial and write-up names the exact tagged version it describes, so you can reproduce the project at a known point. Production configuration, commercial terms and security-sensitive detail stay private by design.

### Licence

The public repositories are all rights reserved, with a limited permission for educational use. See the `LICENSE.md` in each repository. The licence is a draft pending legal review.

<sub>FAKA iAction is a project of Faka Action (Pty) Ltd. Initial focus: creators in South Africa.</sub>
