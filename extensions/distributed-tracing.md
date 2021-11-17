# Distributed Tracing extension

This extension embeds context from 
[W3C TraceContext](https://www.w3.org/TR/trace-context/) into a CloudEvent.

The [OpenTelemetry specification](
https://github.com/open-telemetry/opentelemetry-specification/blob/main/specification/context/context.md#overview)
defines context as:

> A Context is a propagation mechanism which carries execution-scoped
 values across API boundaries and between logically associated execution units. Cross-cutting concerns access their data in-process using the same shared Context object.

Context propagation enables `Distributed Tracing`.
Also from [OpenTelemetry specification](https://github.com/open-telemetry/opentelemetry-specification/blob/main/specification/overview.md#tracing-signal):

> A distributed trace is a set of events, triggered as a result of a single logical operation, consolidated across various components of an application. A distributed trace contains events that cross process, network and security boundaries.

## Using the Distributed Tracing Extension

The [OpenTelemetry Semantic Conventions for CloudEvents](https://github.com/open-telemetry/opentelemetry-specification/blob/main/specification/trace/semantic_conventions/cloudevents.md) defines in which scenarios
this extension should be used and how to use it.

## Attributes

#### traceparent

- Type: `String`
- Description: Contains a version, trace ID, span ID, and trace options as
  defined in [section 3.2](https://www.w3.org/TR/trace-context/#traceparent-header)
- Constraints
  - REQUIRED

#### tracestate

- Type: `String`
- Description: a comma-delimited list of key-value pairs, defined by
  [section 3.3](https://www.w3.org/TR/trace-context/#tracestate-header).
- Constraints
  - OPTIONAL
