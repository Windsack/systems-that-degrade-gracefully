# Principles

The following principles guide the design of systems that must remain usable,
understandable and trustworthy when conditions degrade.

They are not rules.  
They are lenses through which design decisions can be evaluated,
especially in environments where assumptions break and inputs lose integrity.

---

## 1. Degradation is the normal operating mode

Perfect inputs and full capability are temporary states.

Systems should be designed with the expectation that signals weaken,
data becomes sparse, timing drifts, references disappear, components fail
and the environment does not behave as the model assumes.

A system that only works under ideal conditions is **fragile by design**.

---

## 2. Predictability beats precision

When accuracy degrades, behaviour must remain predictable.

A less precise output that is stable and well-characterised
is preferable to a highly accurate output that fails abruptly
or changes behaviour without warning.

Users and operators adapt more easily to **known uncertainty**
than to unexpected failure.

---

## 3. Uncertainty should be visible, not hidden

Degraded inputs should surface as degraded confidence.

Systems should:

- expose uncertainty explicitly
- avoid presenting false certainty
- allow downstream decisions to account for reduced integrity

Silence or overconfidence under uncertainty **erodes trust**
faster than reduced accuracy.

---

## 4. Fallbacks must be deliberate, not accidental

Fallback modes are not emergency hacks.  
They are part of the system design.

Each fallback should have:

- a clear purpose
- known limitations
- defined entry and exit conditions

If a fallback is undocumented, it is not a feature — **it is a liability**.

---

## 5. Simplicity increases survivability

Under degraded conditions, complexity becomes a risk factor.

Design should favour:

- fewer dependencies
- clear data paths
- observable state

When systems are stressed, **simple behaviour is easier to reason about,
debug and trust**.

---

## 6. Documentation is a system component

A system is not only its code or hardware.  
Documentation defines how it is understood and used under pressure.

Design intent, assumptions and limitations should be recorded
while they are still obvious to the designer.

Undocumented decisions tend to be rediscovered
**at the worst possible time**.

---

## 7. Responsibility does not degrade

Responsibility must remain clear, even when capabilities degrade.

Systems can degrade.  
**Responsibility cannot.**

Interfaces, signalling and state communication should preserve
operational agency — not dissolve it.

---

## Closing

These principles are starting points, not conclusions.
They evolve as systems, environments and understanding evolve.

Clarity takes precedence over performance.
Predictability takes precedence over elegance.
Trust takes precedence over precision.
