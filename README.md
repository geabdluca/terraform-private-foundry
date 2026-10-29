# Terraform private Foundry

Standalone Terraform deployment for private Microsoft Foundry infrastructure.

**Status: repository scaffold. Deployable Terraform is not included yet. No Azure deployment has been validated from this repository.**

## Intended scope

- A new Foundry account and project with private connectivity.
- A configurable model deployment.
- New or existing virtual networking and private DNS zones.
- Separate private-endpoint and correctly delegated agent subnets.
- New or existing supporting resources required by the selected setup.
- Explicit resource ownership and narrowly scoped identity permissions.
- Optional custom-CA trust once supported configuration and lifecycle behavior are verified against public documentation.

The deployment does not require a hub/spoke topology, VPN gateway, DNS VM, or firewall stack. Reusing an existing network still requires appropriate routing, DNS resolution, and access for the deployment client.

Agent creation is outside this repository's scope.

## Agent samples

After infrastructure is deployed and validated, use the existing samples to create and run agents:

https://github.com/geabdluca/FoundryAgentsSamples

Individual samples can require additional resources and configuration. A successful basic agent run does not establish that custom-CA trust works.

## Implementation and validation

Infrastructure implementation will include example parameters, validation of new/existing resource choices, and documented outputs for configuring samples. Custom-CA configuration and update/refresh behavior must be documented and tested before being described as supported here.

Do not use the scaffold as a deployment recipe. Implementation and deployment instructions will be added with their validation results.

## References

https://learn.microsoft.com/azure/foundry/how-to/configure-private-link

https://learn.microsoft.com/azure/foundry/agents/how-to/virtual-networks

## License

MIT. See `LICENSE`.
