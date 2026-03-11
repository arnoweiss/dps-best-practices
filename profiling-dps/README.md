## Authoring Transfer Type Profiles

Each Transfer Type Profile defines a set of objects embedded in DPS messages and a set of expected behavior in the
systems processing the messages.

### Extensible objects

#### The DPS `transferType`

As part of the `DataFlowPrepareMessage` and `DataFlowStartMessage`, it is a logical superset of the
`DataAddress.endpointType` property and completes it with a hint on whether a transfer follows the push or pull
paradigm.

#### The DPS `DataAddress`

`endpointType` determines the schema of the `DataAddress` by declaring additional properties mandatory or optional and
defining their semantics. It is independent of flow direction and can be reused as specific to a wire-protocol specific
but referable by multiple Transfer Types.

```json
{
  "type": "https://w3id.org/idsa/v4.1/HTTP",
  "endpoint": "http://dataplane.provider.com/api/public",
  "authType": "bearer",
  "endpointType": "https://w3id.org/idsa/v4.1/HTTP",
  "authorization": "<AUTH_TOKEN>"
}
```

#### The DPS `metadata`

As part of the `DataFlowPrepareMessage` and the `DataFlowStartMessage`, it forwards metadata from the Provider Control
Plane to the Provider Data Plane. This may include objects obtained from the negotiation process that may be relevant
for scoping the access to the dataplane. They are specific to a Transfer Type Profile and may thus contain data relevant
for business processes that transcend the domain of data transport.

#### The DPS `labels`

### Scoping a profile

Profiles may be scoped to facilitate data transfer on the level of transport protocols or even be specific to a certain
dataspace usecase that also encompasses business logic. In the latter case, profile authors are encouraged to reference
existing transport-protocol level Transfer Type Profiles specifications. This fosters reuse, enables interoperability
and accelerates profile development.

### Artifacts

Profiles should explicitly define json schemas for the objects they specify. Those json schemas must refer to the
relevant base schemas from the DPS specification.

### Relationship to Dataspace Protocol and its Profiles


