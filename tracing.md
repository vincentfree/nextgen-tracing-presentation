---
marp: true
theme: ing
backgroundImage: url('https://marp.app/assets/hero-background.svg')
# _class: lead
---
<!-- _class: cover -->

![bg opacity:.5](assets/airstrip.jpg)

# Tracing 2.0
## Our evolution to Open Telemetry with Grafana Tempo
---

![bg right](assets/FullSizeRender.jpg)
# About me

```yaml
Name: Vincent Free
Title: Engineer V
Age: 36
Experience:
  - GoLang
  - Kotlin
  - Containerization(k8s,swarm)
```

---

# Distributed Tracing

What is a trace?

![](assets/trace%20small.png)

---

# TracING @ ING

- Started out as a Tibco library
- Current version was created in **2017**

![](assets/TracING_01.png)

<!-- 
TracING started out as a Tibco specific library, It evolved into the current JVM based product in 2017. 
-->

<!--
This makes the current version 6 years old(the previous version redates my involvement with the product).
-->

---

# NextGen version of TracING

---
![bg right:33%](assets/tools.jpg)

# Migration phase

- Interoperability between old and new
  - update span ID's from UUID to the W3C trace-context standard

<!--
The old ID format was implemented before there was an official standard.
-->

- Backwards compatible with Jaeger Uber ID injecting/extraction 

<!--
The jaeger format was used in the old version of tracing. 
With the new environment we are using the W3C standard.
-->

---