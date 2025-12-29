---
title: The standard pod scaling ap...
---

The standard pod scaling approach requires pods to restart when applying new resource requests and limits. While this can work for stateless applications, it may still introduce latency and service disruptions, making it less suitable for workloads that demand continuous uptime. In addition, this method may add operational overhead for teams to manage it effectively.To address these challenges, **In-place Workload Right-sizing** is available. This feature is ideal for services where stability is critical, allowing you to improve performance seamlessly, reduce disruption risks due to restarts, and make the optimization process even more flexible and efficient.With in-place changes enabled, you can:
