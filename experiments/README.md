# Experiments

Status: `NOT_STARTED`

This directory currently defines experiment principles only. No real benchmark
or model/API experiment was started in the repository bootstrap.

## Controlled comparison

When a residual gap is justified, prefer:

```text
same model
same repository
same starting state
same task
```

Change the Harness or control configuration as the experimental variable and
compare, where applicable:

- baseline;
- an existing mature solution;
- a minimal internal extension.

## Measures

At minimum, make the following observable where relevant:

- task success;
- false completion;
- wrong-trajectory persistence;
- scope creep;
- Human rescue;
- unnecessary intervention;
- regression;
- token, cost, and runtime overhead;
- time to a correct solution.

## Evidence boundary

An experiment must state its input identity, configuration, stopping rule,
observed outputs, and limitations. A local pass or a successful fixture does
not automatically establish production value, generality, or authorization to
expand the implementation envelope.
