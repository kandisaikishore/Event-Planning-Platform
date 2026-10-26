# Development, Configuration, and QA Guide

This repository describes an AI Studio event-planning application starter. Verify the current source and package manifests before assuming a particular event workflow, backend, database, or AI integration is implemented. The README currently states that a live deployment URL has not been verified.

## Setup and configuration

```bash
git clone https://github.com/saikishore2410/Event-Planning-Platform.git
cd Event-Planning-Platform
```

Inspect the package manifest and source to identify the supported runtime, dependency manager, and actual scripts. Use those declared commands to install, run, test, lint, and build the app.

Document each environment variable used by source code with its purpose and whether it is required. Provide safe placeholders only. Keep API keys, database credentials, tokens, and private user data out of version control.

## QA checklist

For implemented event workflows, test:
- Required event fields, invalid dates, and end-before-start ranges
- Time-zone display and date preservation when editing an event
- Capacity limits, repeated registration, and cancellation if supported
- Empty, loading, success, and recoverable error states
- Failed AI/provider requests and malformed provider responses if AI is integrated
- Keyboard navigation, form labels, and responsive layouts

Do not present a request as successful until the relevant operation has actually succeeded. Mock external AI and calendar services in automated tests.

## Deployment status

A repository URL is not a live application URL. Only add a deployment URL after opening it and verifying the application responds as expected. Record the verification date and any known demo limitations.

## Pull-request checklist

- [ ] Run the project-defined lint, test, and build commands.
- [ ] Add regression coverage for the changed event workflow.
- [ ] Check that missing configuration fails with an actionable message.
- [ ] State which external integrations were mocked or not tested.
- [ ] Do not claim deployment or unimplemented features as verified.
