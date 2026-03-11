# Data Plane Signaling Best Practices

This document provides recommendations, patterns, and best practices for implementing and extending
the [Data Plane Signaling (DPS) specification](https://github.com/eclipse-dataplane-signaling/dataplane-signaling). The
DPS specification defines a protocol that enables connector control planes and data planes to
orchestrate data transfers within dataspaces.

### Purpose and Scope

The DPS specification establishes the foundational protocol for control plane and data plane communication.
Implementation details and operational considerations are left to implementers. The specification of profiles for DPS
is left to consortia with an interest in cross-vendor interoperability between control planes and data planes. This best
practices document guides these activities by:

- showcasing **architectural patterns** for scalable and resilient data transfer systems
- providing recommendations and examples for **endpoint type profiles** for common protocols

### Target Audience

This guide is intended for:

- authors of profiles for DPS and DSP in the context of specification bodies
- developers implementing DPS control plane or data plane components
- organizations evaluating DPS for their dataspace products

### Relationship to the DPS Specification

This best practices guide is **non-normative** and **complementary** to the DPS specification, not a replacement. Only
the specification defines the normative requirements that all implementations MUST follow for interoperability.
When conflicts arise,
the [DPS specification](https://github.com/eclipse-dataplane-signaling/dataplane-signaling/blob/main/docs/signaling.md)
always takes precedence. The spec group will work to align the best practices with the specification as it evolves.

**Normative extensions** to the DPS specification (namely endpoint type profiles) 
reside exclusively in the [endpoint-type-registry repository](https://github.com/eclipse-dataplane-signaling/endpoint-type-registry).
This best practices repository provides examples how to write such profiles.

### Contributing

If you've encountered related topics not covered here, we encourage you to contribute through issues and discussions on
the [repository](https://github.com/eclipse-dataplane-signaling/dataplane-signaling).
