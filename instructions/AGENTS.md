# Company Development Standards

These are our team's standing conventions for building in this app. Apply them whenever generating or modifying app elements, regardless of which module is being worked on. This is a test

## Naming Conventions

- Entities: PascalCase, singular nouns (e.g., Customer, OrderLine — not Customers or customer)
- Microflows: prefix by purpose — ACT_ for user-triggered actions, SUB_ for sub-microflows, VAL_ for validation logic
- Pages: suffix by purpose — _Overview for list pages, _NewEdit for create/edit forms, _View for read-only detail pages

## Security

- Never grant the Anonymous role write access to any entity.
- Any entity holding customer or personal data must have an access rule limiting visibility to the owning user or an appropriate role — not a blanket "all users" rule.

## General

- Prefer reusing an existing microflow or snippet over duplicating similar logic.
- Every microflow should have a short description explaining what it does and why, not just what it's called.
