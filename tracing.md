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

![](assets/tracing_example.png)

---

# Distributed Tracing

What is a span context?

![](assets/tracing_span_context.png)

<!--
The Span Context consists of a TraceID, SpanID and TraceFlags.

type SpanContext struct {
	traceID    TraceID [16]byte
	spanID     SpanID [8]byte
	traceFlags TraceFlags byte
}

-->

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

# TracING @ ING

![](assets/TracING_04.png)

---

# TracING @ ING

![](assets/TracING_03.png)

---

# TracING @ ING

![](assets/TracING_02.png)

---

# NextGen version of TracING

Grafana Tempo

![](assets/trace.png)

---

# NextGen version of TracING

- Open Telemetry
- Feature rich
  - Service graph
  - Metric generator
  - Node graph
  - TraceQL
- Known architecture
  - Grafana Mimir

---

# Open Telemetry

![bg right:70% fit](assets/otel_diagram.png)
<!-- ![h:583](assets/otel-collector_1.png) -->

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