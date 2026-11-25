# AI and data handling

How we use AI at work, and how AI in our products handles our customers' data. This guideline is in beta: it will change as we learn, and every change is announced to the team.

## Data classes

| Class | What it covers | Rule |
|---|---|---|
| **Public** | Marketing pages, public docs, open source code | Share freely |
| **Internal** | Our code, designs, plans, metrics with no customer detail | Staff and approved tools only |
| **Confidential** | Customer names, contracts, prices, aggregate usage | Need to know only |
| **Restricted** | Personal data: names with phone numbers, emails, NIDA and other ID numbers, addresses. Call recordings and transcripts, message content, payment and wallet data, health data, passwords, keys and tokens | Never leaves production systems except as the product needs. Never in AI tools, chat, tickets, screenshots or tests |

When unsure, treat it as restricted.

## Using AI tools at work

- **Approved tools only**, on company accounts with training on our data turned off. Leadership keeps the list of approved tools.
- **Never paste restricted data** into any AI tool: no production rows, recordings, transcripts, customer messages, logs with personal data, keys or tokens.
- **Use sample data** in prompts, screenshots, tests and demos. Make it up, never copy it from production.
- **Do not let AI tools query production** databases or read production secrets.
- **A person is responsible** for every change AI helped write. It is reviewed like any other code before it merges.
- **Check what AI tells you.** It can be wrong with confidence. Facts about law, money or security need a second source.

## AI in our products

This covers every product feature that sends data to a model: the Sema voice agent, Minions, Sarufi bots, and our internal agents.

1. **Send the least data needed.** Give the model only what the task needs. Mask or remove personal data that it does not need.
2. **No personal data in logs.** Prompts, tool calls and model replies are logged without personal data, using our shared redaction helpers.
3. **Approved model providers only**, under contracts that forbid training on our data. We record which country each provider processes data in.
4. **Keep it only as long as needed.** Recordings, transcripts and AI conversation history have a set retention period per product, and are deleted after it.
5. **Say it is AI.** People always know when they are talking to an AI, and can ask for a person.
6. **Customers stay in control.** An organisation can turn AI features off. Their data is never used to train models.
7. **A person decides what matters.** AI does not move money, close accounts or change access on its own. A person or a fixed, tested rule confirms it.
8. **Guard the tools.** An AI agent can only act within the organisation it serves. Every tool call it makes is checked against the user's permissions and audited. Text from customers, documents or web pages is treated as data, never as instructions.
9. **Test before release.** Each AI feature is tested for leaking data across customers, for prompt injection, and for harmful replies, and it ships as beta under the [beta guideline](beta-guideline.md) until its data review passes.

## The law

We follow Tanzania's Personal Data Protection Act, 2022, and the laws of each country we serve:

- we collect personal data for a clear purpose, with a lawful basis such as consent or contract,
- people can ask to see, correct or delete their data, and we answer within 30 days,
- data sent to providers outside Tanzania is covered by a contract with proper safeguards.

## When something goes wrong

If personal data reaches a place it should not, including an AI tool or a model provider, it is a **SEV1** incident. Follow the [incident response policy](incident-response.md) straight away. Reporting a mistake quickly is always right, and never punished.
