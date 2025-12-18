# Degraded Mode

Degraded mode describes a state in which a system continues to operate
with reduced capability, reduced accuracy, or reduced confidence —
without failing completely.

This document outlines general considerations for designing
and reasoning about degraded operation.

---

## What degraded mode is not

Degraded mode is not:
- a failure state
- an exception handler
- a temporary workaround

It is a **designed operating mode** with defined behavior.

---

## Typical causes of degradation

Degradation can arise from many sources, including:
- reduced sensor quality or availability
- partial loss of external references
- timing drift or synchronization issues
- environmental interference
- resource constraints (power, bandwidth, compute)

In many systems, multiple degradations occur simultaneously.

---

## Design goals in degraded mode

A well-designed degraded mode aims to:
- preserve core functionality where possible
- reduce output fidelity in a controlled way
- maintain internal consistency
- communicate reduced integrity clearly

The goal is not to maintain performance,
but to maintain **trustworthiness**.

---

## Graceful loss of capability

Capabilities should be lost gradually, not abruptly.

Examples of graceful degradation include:
- switching from absolute to relative measurements
- reducing update rates instead of stopping updates
- widening confidence bounds instead of freezing outputs

Each reduction should be intentional and explainable.

---

## Entry and exit conditions

Transitions into and out of degraded mode should be explicit.

Design should define:
- which signals or conditions trigger degradation
- how long degradation is tolerated
- how recovery is detected and validated

Flapping between modes is often more harmful than staying degraded longer.

---

## Observability and communication

Operators and downstream systems must be able to answer:
- *What still works?*
- *What no longer works?*
- *How reliable is the remaining output?*

Clear signaling of degraded state is essential,
even if it complicates interfaces.

---

## Degraded does not mean unsafe — but it can

Degraded operation is acceptable only within known limits.

Design must ensure that:
- degraded outputs cannot be mistaken for nominal ones
- unsafe interpretations are prevented or clearly discouraged
- responsibility boundaries remain clear

When safe operation can no longer be guaranteed,
degraded mode must transition to shutdown or fail-safe behavior.
