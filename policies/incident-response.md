# Incident response

An incident is anything that harms, or could harm, our customers, their data or their money: an outage, a leak, a breach, a bad deploy or a provider failure. When in doubt, declare one. Standing one down costs nothing.

## Severity

| Level | What it means | Examples | Response |
|---|---|---|---|
| **SEV1** | Customer data or money exposed, or a product down for everyone | Personal data leaked, money moved wrongly, keys exposed, payments or calls failing for all customers | Now, at any hour. Leadership told within 30 minutes |
| **SEV2** | A major feature broken, or many customers affected | Campaigns not sending, one provider down, billing wrong for some customers | Within 1 hour, in working hours or on call |
| **SEV3** | Small impact, with a workaround | A slow page, a failed job that can be rerun | Next working day |

## Roles

- **Incident lead:** runs the response, makes decisions, and is the one voice on it. This is the first person to declare it, until they hand over.
- **Comms:** tells customers and staff what is happening, and keeps the status page up to date.
- **Scribe:** keeps a timeline of what was seen, decided and done, with times.

For a SEV3, one person may hold all three.

## The first hour

1. **Declare.** Post in the incidents channel: the severity, what is affected, and who leads.
2. **Contain.** Stop the harm before you look for the cause. Roll back, turn the feature off, block the key, or pause the job.
3. **Rotate.** If a secret may have leaked, rotate it now, then check where it was used.
4. **Keep evidence.** Do not delete logs, rows or files. Take copies before you change anything.
5. **Update.** Post an update at least every 30 minutes for a SEV1 and every hour for a SEV2, even when nothing has changed.

## Telling people

- **Customers:** comms tells affected customers within 24 hours of a SEV1, in plain words: what happened, what it means for them, and what we are doing.
- **Regulators:** where personal data is breached, we notify the Personal Data Protection Commission within 72 hours, as the Personal Data Protection Act requires. Leadership decides, and the incident lead supplies the facts.
- **Partners:** banks, mobile networks and payment partners are told when their contract says so.

Nobody talks to the press or posts publicly about an incident except leadership.

## After the incident

Within 5 working days, the lead writes a short review and shares it with the team. It is blameless: we fix systems, not people.

```
Title, severity, date, lead
What happened (two or three sentences)
Timeline (times, in East Africa Time)
Impact: who, how many, for how long, any data or money involved
Cause: why it happened, and why we did not catch it sooner
What we changed already
Follow-ups: each with an owner and a date, tracked as issues
```

A SEV1 or SEV2 is not closed until its follow-ups are tracked.
