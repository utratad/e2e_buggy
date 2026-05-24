# Buggy App — Maestro Test Suite

## Requirements

- [Maestro](https://maestro.dev/) **0.9.1**

## Running Flows

Open the repository via Maestro
Project's structure will be visible on the right-hand side of the screen - select a flow
In the test session results, select Run Test
full_flow.yaml contains a beginning-to-end flow for Buggy app: registration form validation, registering, login/logout, applying and veryfing job offers, inspecting profile page for applied-for job offers

## Environment Variables

Some flows require env vars (e.g. `LOGIN`, `PASSWORD`):

### Option 1 — Declare in the flow file

Add an `env:` block at the top of the flow, before the `---` separator:

```yaml
appId: com.example.buggy
env:
  LOGIN: user@example.com
  PASSWORD: Secret123!
---
- launchApp:
    clearState: true
```

### Option 2 — Maestro UI (Manage Environments)

1. Open the Maestro desktop app.
2. In test session results, drop-down the "None" list and go to **Manage Environments → Create**.
3. Declare your variable-value pairs (e.g. `LOGIN` / `user@example.com`).
4. Select the environment when running a flow — Maestro will inject the variables automatically.
