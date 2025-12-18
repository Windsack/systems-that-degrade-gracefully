# Principles

The following principles guide the design of systems that must remain usable,
understandable and trustworthy even when conditions degrade.

They are not rules.
They are lenses through which design decisions can be evaluated.

---

## 1. Degradation is the normal operating mode

Perfect inputs and full capability are temporary states.
Systems should be designed with the expectation that
signals weaken, data becomes sparse, timing drifts, or components fail.

A system that only works under ideal conditions is fragile by design.

---

## 2. Predictability beats precision

When accuracy degrades, behavior must remain predictable.

A less precise output that is stable and well-characterized
is preferable to a highly accurate output that fails abruptly
or changes behavior without warning.

Users and operators adapt more easily to known uncertainty
than to unexpected failure.

---

## 3. Uncertainty should be visible, not hidden

Degraded inputs should surface as degraded confidence.

Systems should:
- expose uncertainty explicitly
- avoid presenting false certainty
- allow downstream decisions to account for reduced integrity

Silence or overconfidence under uncertainty erodes trust.

---

## 4. Fallbacks must be deliberate, not accidental

Fallback modes are not emergency hacks.
They are part of the system design.

Each fallback should have:
- a clear purpose
- known limitations
- defined entry and exit conditions

If a fallback is undocumented, it is not a feature — it is a liability.

---

## 5. Simplicity increases survivability

Under degraded conditions, complexity becomes a risk factor.

Design should favor:
- fewer dependencies
- clear data paths
- observable state

When systems are stressed, simple behavior is easier to reason about,
debug and trust.

---

## 6. Documentation is a system component

A system is not only its code or hardware.
Its documentation defines how it is understood and used under pressure.

Design intent, assumptions and limitations should be recorded
while they are still obvious to the designer.

Undocumented decisions tend to be rediscovered at the worst possible time.
