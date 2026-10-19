# API access control tester

Final year project, Keele University, Sep 2026 – May 2027. **Work in progress.**

A tool that reads an API's OpenAPI spec and a table of which roles may do what, then tests every role against every endpoint to find broken access control. A second phase injects faults into the system's dependencies to check whether access control still holds when things fail.

## Research questions
1. Does giving the tool the access rules upfront find more broken access control than existing scanners (e.g. OWASP ZAP)?
2. Does access control still hold, or fail open, when dependencies go down?

## Planned stack
Python · Docker Compose · Toxiproxy · pytest · OpenAPI

## Test targets
VAmPI and crAPI (deliberately vulnerable APIs), plus a small custom service with a deliberate fail-open fallback as a control.

## Progress
- [ ] OpenAPI parser
- [ ] Rules table format
- [ ] Role-by-endpoint scanner
- [ ] Ownership (BOLA) tests
- [ ] Fault injection
- [ ] Evaluation against ZAP
