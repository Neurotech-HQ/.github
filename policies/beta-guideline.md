# Beta guideline

Beta lets us put new features in front of real customers early, safely. This page has two parts: the rules we follow, and what beta means for customers.

## For our teams

### What a beta feature must have

- **A switch per organisation.** It is off by default and turned on for named customers only. We can turn it off in minutes without a deploy.
- **Security review done.** It passes the same review as any feature: auth, input checks, rate limits, audit of staff actions, and no secrets or personal data in logs.
- **Data review done.** We know what personal data it touches, where that data goes and how long we keep it. Every AI feature also follows the [AI and data handling guideline](ai-and-data-handling.md).
- **Metering.** Anything that costs money is metered, even when beta use is free.
- **A clear label.** The product shows a Beta badge wherever the feature appears.
- **An owner.** One named person answers for it.

### What beta does not change

Beta is never an excuse for weaker security, weaker data protection or wrong billing. Those rules apply in full from the first customer.

### Leaving beta

A feature becomes generally available when:

1. it has run for at least 4 weeks with real customers and no open SEV1 or SEV2,
2. its known issues are fixed or documented,
3. support has a guide and docs are public,
4. pricing is final, and
5. the owner and leadership agree.

A beta that does not reach this within 6 months is either improved with a plan, or removed.

## For customers

When you turn on a beta feature:

- **It may change.** We may change or remove it. We will tell you before we do.
- **There is no service level.** Our uptime and response commitments do not cover it, though we still fix problems fast.
- **Your data stays yours.** It is protected exactly as in the rest of the product. We never use it to train AI models.
- **You can leave at any time.** Ask us to turn it off and your normal service carries on. Data the beta created is kept or deleted, as you choose.
- **Tell us what you think.** Your feedback shapes the product. Email support@neurotech.africa or speak to your account manager.
