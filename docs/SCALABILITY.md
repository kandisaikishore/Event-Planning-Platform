# Scalability baseline

Scale the application based on measured demand and real workflows. Avoid distributed components until profiling shows they are needed.

## Priorities
- Profile critical workflows and identify bottlenecks before adding replicas.
- Bound request and upload sizes, concurrent work, retries, connection pools, and provider timeouts.
- Paginate large datasets and optimize measured database queries/indexes.
- Externalize shared state before horizontal scaling; use durable queues with back-pressure for long-running tasks where appropriate.
- Add health/readiness checks, structured logs, request IDs, metrics, graceful shutdown, and rollback procedures for hosted services.
- Protect secrets and sensitive/user data from source control, logs, and diagnostics.
- Add automated build, unit, integration, security/dependency, and deployment smoke checks appropriate to the stack.

## Load validation
Test normal, peak, burst, and dependency-failure scenarios. Track throughput, p95/p99 latency, error rate, CPU/memory, database wait time, queue lag, and cost where relevant.

## Release gates
- [ ] Authorization and data isolation are tested.
- [ ] Retries are bounded and state-changing operations are idempotent where needed.
- [ ] Persistent data backup/restore and migration/rollback are validated.
- [ ] Capacity assumptions and measured load-test results are recorded.

This is a planning checklist, not evidence of completed load testing or production scaling.