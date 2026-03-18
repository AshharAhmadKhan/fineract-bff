# fineract-bff

Borrower Backend-for-Frontend (BFF) for Apache Fineract.

This repository contains the architecture design and GSoC 2026 proposal
for FINERACT-2439 — a standalone Spring Boot service that acts as the
trust boundary between borrowers and Apache Fineract.

## What this is

The Apache Fineract self-service module was removed in March 2026 after a
security review identified seven OWASP-class vulnerabilities, all rooted
in borrower authentication being built on Fineract's back-office security
model. This project builds the replacement: a dedicated BFF that owns
borrower identity independently of Fineract, calls Fineract exclusively
through a service account, and exposes consumer-facing APIs for
registration, login, account viewing, and loan repayment.

## Architecture

See [ARCHITECTURE.md](./ARCHITECTURE.md) for the full design including
system diagrams, authentication sequences, schema, and design decisions.

## GSoC 2026

- Ticket: https://issues.apache.org/jira/browse/FINERACT-2439
- Candidate: Ashhar Ahmad Khan
- Apache Fineract dev list: https://lists.apache.org/list.html?dev@fineract.apache.org

## License

Apache License 2.0
