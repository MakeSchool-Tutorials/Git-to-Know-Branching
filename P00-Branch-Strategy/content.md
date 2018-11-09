---
title: "Git Branching Strategies"
slug: branching-strategies
---

> If you ever talk to a great programmer, you'll find they know their tools like an artist knows their paintbrushes. - _Bill Gates_

This tutorial details a step-by-step strategy to enhance your development workflow called **_git branching_**. Branching is often referred to as the "killer feature" of Git.

# Purpose of Branching

Successful teams follow **three rules to integrate git into their daily workflow**:

1. **Commit early and often.**
1. **Don't break master.**
    * The code in `origin/master` **always** works.
    * **No errors**, no UI glitches.
    * **No exceptions**.
1. **Use branches.** A branch can represent:
    * A brand new **feature**.
    * **Bug fixes**.
    * Works **in progress**.
    * Individual contributions **that aren't ready to be deployed**.
