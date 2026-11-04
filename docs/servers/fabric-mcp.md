# Fabric MCP Server

The Fabric MCP server is hosted at `https://mcp.equinix.com/fabric` and can be used with MCP-compatible AI agents.

For general information on MCP server setup and configuration, see [Getting Started](../getting-started.md).

**⚠️ Private Beta**

The Fabric MCP Server is currently in Private Beta. To join the Beta program, email [fabric-intelligence-support@equinix.com](mailto:fabric-intelligence-support@equinix.com) or reach out to your Equinix account representative.


## Tools

The Fabric MCP server exposes the following MCP tools that allow AI assistants to interact with your Equinix Fabric resources. Each tool corresponds to a specific Fabric API endpoint.

**ℹ️ Recommendation**

Enable human confirmation for tool execution, especially for operations that create, update, or delete resources. This helps prevent unintended changes to your Fabric infrastructure.

**⚠️ Current Limitations**

Delete functionality is not currently supported in the Fabric MCP Server. This includes deletion of connections, ports, and Cloud Routers.

### Connections

| Tool                | Description                                                                     | API Endpoint                                                                                  |
|---------------------|---------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------| 
| `create_connection` | Create a new Fabric Connection                                                  | [Create Connection](https://docs.equinix.com/api-catalog/fabricv4/#tag/Connections/operation/createConnection)        |
| `search_connection` | Search for Fabric Connections using advanced filtering, pagination, and sorting | [Search Connection](https://docs.equinix.com/api-catalog/fabricv4/#tag/Connections/operation/searchConnections)       |
| `update_connection` | Update an Equinix Fabric Connection using its UUID                              | [Update Connection](https://docs.equinix.com/api-catalog/fabricv4/#tag/Connections/operation/updateConnectionByUuid)  |
| `validate_connection` | Validate a Fabric Connection configuration before creation                      | [Validate Connection](https://docs.equinix.com/api-catalog/fabricv4/#tag/Connections/operation/validateConnections)   |
| `retry_connection_action` | Perform actions on a Fabric Connection                                          | [Connection Actions](https://docs.equinix.com/api-catalog/fabricv4/#tag/Connections/operation/createConnectionAction) |
| `check_connection` | Validate a connection configuration before creation. |  |
| `retry_connection` | Retry a connection operation (creation or deletion). |  |
| `search_connections` | Get a list of user's virtual connections using search criteria. | [Search Connections](https://docs.equinix.com/api-catalog/fabricv4/#tag/Connections/operation/searchConnections) |
| `operate_connection` | Retry a connection operation (creation or deletion). | [Create Connection Action](https://docs.equinix.com/api-catalog/fabricv4/#tag/Connections/operation/createConnectionAction) |
| `validate_connection_request` | Before creating a connection, validate its payload and auth key. | [Validate Connection](https://docs.equinix.com/api-catalog/fabricv4/#tag/Connections/operation/validateConnections) |

### Fabric Metros

| Tool | Description | API Endpoint |
|---------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `get_metro` | Retrieve detailed information about a specific Fabric Metro by passing its Metro Code | [Get Metro by Code](https://docs.equinix.com/api-catalog/fabricv4/#tag/Metros/operation/getMetroByCode) |
| `list_metro` | Fetch all metros available in Fabric | [Get All Metros](https://docs.equinix.com/api-catalog/fabricv4/#tag/Metros/operation/getMetros) |
| `list_metros` | Fetch all metros available in Equinix Fabric. | [List Available Metros](https://docs.equinix.com/api-catalog/fabricv4/#tag/Metros/operation/getMetros) |
| `list_ne_metros` | Retrieve Network Edge metros — optionally filtered to a single metro by code. | [List Available Metros](https://docs.equinix.com/api-catalog/network-edgev1/#tag/Availability-and-Metros/operation/getMetros) |

### Ports

| Tool | Description | API Endpoint |
|------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `get_port` | Retrieve detailed information about a specific Fabric Port by passing its UUID | [Get Port by UUID](https://docs.equinix.com/api-catalog/fabricv4/#tag/Ports/operation/getPortByUuid) |
| `search_port` | Search for Fabric Ports using advanced filtering, pagination, and sorting | [Search Ports](https://docs.equinix.com/api-catalog/fabricv4/#tag/Ports/operation/searchPorts) |
| `update_port` | Update a Fabric Port configuration | [Update Port](https://docs.equinix.com/api-catalog/fabricv4/#tag/Ports/operation/updatePortByUuid) |
| `get_vlan_port` | Get VLAN configurations for a specific port | [Get Port VLANs](https://docs.equinix.com/api-catalog/fabricv4/#tag/Ports/operation/getVlans) |
| `attach_physical_ports_to_lag` | Add one or more physical ports to an existing virtual LAG port. | [Add to Lag](https://docs.equinix.com/api-catalog/fabricv4/#tag/Ports/operation/addToLag) |
| `create_port` | Create a new Equinix Fabric port (XF_PORT) via the Fabric API. | [Create Port](https://docs.equinix.com/api-catalog/fabricv4/#tag/Ports/operation/createPort) |
| `search_ports` | Search for Equinix Fabric ports using advanced filtering, sorting, and pagination. | [Search Ports](https://docs.equinix.com/api-catalog/fabricv4/#tag/Ports/operation/searchPorts) |

### Cloud Routers

| Tool | Description | API Endpoint |
|-------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `search_router` | Search for Equinix Fabric Cloud Routers using advanced filtering, pagination, and sorting | [Search Cloud Routers](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/searchCloudRouters) |
| `create_router` | Create a new Fabric Cloud Router | [Create Cloud Router](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/createCloudRouter) |
| `update_router` | Update an existing Fabric Cloud Router | [Update Cloud Router](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/updateCloudRouterByUuid) |
| `get_router_package` | Get details about a Cloud Router package | [Get Router Package](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/getCloudRouterPackageByCode) |
| `create_router_commands` | Initiate router commands such as ping or traceroute | [Create Router Commands](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/createCloudRouterCommand) |
| `search_router_commands` | Search for router command execution results | [Search Router Commands](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/searchCloudRouterCommands) |
| `search_routes` | Search for routes including advertised, received, and active routes | [Search Routes](https://docs.equinix.com/fabric-cloud-router/fcr-api/manage-routing-tables-api/) |
| `load_routes` | Create route table actions for a Cloud Router | [Create Route Actions](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/createCloudRouterAction) |
| `create_router_command` | Initiate a PING command on a Fabric Cloud Router by UUID. | [Get Commands](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/getAllCloudRouterCommands) |
| `list_router_packages` | Retrieve all Fabric Cloud Router package available in Equinix Fabric. | [List Packages](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Router-Packages/operation/getCloudRouterPackages) |
| `refresh_routes` | Loads the user's routing table of a Fabric Cloud Router (FCR). | [Create Route Table Action](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/createCloudRouterAction) |
| `search_routers` | Search for Equinix Fabric Cloud Routers using advanced filtering, sorting, and pagination. | [Search Routers](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Routers/operation/searchCloudRouters) |

### Routing Protocols

| Tool            | Description                                                         | API Endpoint                                                                                                              |
|-----------------|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------| 
| `get_routing_protocols` | Search for a Routing Protocol using connection                      | [Get Routing Protocols](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/getConnectionRoutingProtocols)             |
| `create_routing_protocols` | Create a new Routing Protocol                                       | [Create Routing Protocols](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/createConnectionRoutingProtocol)        |
| `update_routing_protocols` | Update an existing Routing Protocol                                 | [Update Routing Protocols](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/patchConnectionRoutingProtocolByUuid)   |
| `replace_routing_protocols` | Replace an existing Routing Protocol                                | [Update Routing Protocols](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/replaceConnectionRoutingProtocolByUuid) |
| `attach_route_aggregation` | Attach a Route Aggregation to a connection. | [Attach Aggregation](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/attachConnectionRouteAggregation) |
| `attach_route_filter` | Attach a Route Filter to a connection. | [Attach Route Filter](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/attachConnectionRouteFilter) |
| `create_routing_protocol` | Create a single Routing Protocol (DIRECT or BGP) for a connection. | [Create Routing Protocol](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/createConnectionRoutingProtocol) |
| `create_routing_protocol_action` | Create a BGP action on a routing protocol for a connection. | [Clear/Reset BGP](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/postConnectionRoutingProtocolBgpActionByUuid) |
| `list_route_aggregations_for_connection` | Get all Route Aggregations attached to a connection, with optional filtering by UUID. | [Get Connection Route Aggregations](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/getConnectionRouteAggregations) |
| `list_route_filters_for_connection` | Get all Route Filters attached to a connection, with optional filtering by UUID. | [Get Connection Route Filters](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/getConnectionRouteFilters) |
| `list_routing_protocol_actions` | Get BGP actions for a routing protocol on a connection, optionally filtering by action UUID. | [Get BGP Actions](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/getConnectionRoutingProtocolAllBgpActions) |
| `list_routing_protocols` | This tool fetches Routing Protocols for a specific connection. | [Get Routing Protocols](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/getConnectionRoutingProtocols) |
| `replace_routing_protocol` | Replace a Routing Protocol on a connection using PUT with a full payload. | [Replace Protocol](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/replaceConnectionRoutingProtocolByUuid) |
| `update_routing_protocol` | Update a Routing Protocol using JSON Patch operations. | [Patch Protocol](https://docs.equinix.com/api-catalog/fabricv4/#tag/Routing-Protocols/operation/patchConnectionRoutingProtocolByUuid) |

### Projects

| Tool | Description | API Endpoint |
|-------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `search_projects` | Fetch all projects available in Equinix Resource Manager | [Get Projects](https://docs.equinix.com/api-catalog/getprojectsv2/#tag/Project/operation/getAllProjects) |
| `list_project` | Fetch all projects available in the Equinix Substrate Governance API. |  |
| `list_projects` | Fetch all projects available in the Equinix Substrate Governance API. | [Get Projects](https://docs.equinix.com/api-catalog/getprojectsv2/#tag/Project/operation/getAllProjects) |

### Pricing

| Tool | Description | API Endpoint |
|-------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `search_prices` | Search for pricing information across Fabric resources | [Search Prices](https://docs.equinix.com/api-catalog/fabricv4/#tag/Prices/operation/searchPrices) |

### Precision Time

| Tool | Description | API Endpoint |
|-------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `get_time_service` | Retrieve detailed information about a specific Precision Time service by UUID | [Get Time Service](https://docs.equinix.com/api-catalog/fabricv4/#tag/Precision-Time/operation/getTimeServicesById) |
| `search_time_service` | Search for Equinix Precision Time services | [Search Time Services](https://docs.equinix.com/api-catalog/fabricv4/#tag/Precision-Time/operation/searchTimeServices) |
| `update_time_service` | Update a Precision Time service configuration | [Update Time Service](https://docs.equinix.com/api-catalog/fabricv4/#tag/Precision-Time/operation/updateTimeServicesById) |

### Service Profiles

| Tool | Description | API Endpoint |
|------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `search_service_profile` | Search for Fabric Service Profiles using advanced filtering | [Search Service Profiles](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Profiles/operation/searchServiceProfiles) |
| `create_service_profile` | Create a new Fabric Service Profile | [Create Service Profile](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Profiles/operation/createServiceProfile) |
| `update_service_profile` | Update an existing Service Profile | [Update Service Profile](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Profiles/operation/updateServiceProfileByUuid) |
| `replace_service_profile` | Replace a Service Profile configuration | [Replace Service Profile](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Profiles/operation/putServiceProfileByUuid) |
| `get_service_profile_metros` | Get metro information for a specific Service Profile | [Get Service Profile Metros](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Profiles/operation/getServiceProfileMetrosByUuid) |
| `get_service_profile` | Retrieve detailed information about a specific service profile by its UUID. | [Get Service Profile](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Profiles/operation/getServiceProfileByUuid) |
| `list_service_profile_metros` | Retrieve the list of metros where a specific service profile is available. | [Get Service Profile Metros](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Profiles/operation/getServiceProfileMetrosByUuid) |
| `search_service_profiles` | Search for Equinix Fabric service profiles using advanced filtering, sorting, and pagination. | [Search Service Profiles](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Profiles/operation/searchServiceProfiles) |

### Service Tokens

| Tool | Description | API Endpoint |
|---------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `search_service_tokens` | Search for Fabric Service Tokens | [Search Service Tokens](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Tokens/operation/searchServiceTokens) |
| `create_service_token` | Create a new Service Token | [Create Service Token](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Tokens/operation/createServiceToken) |
| `update_service_token` | Update an existing Service Token | [Update Service Token](https://docs.equinix.com/api-catalog/fabricv4/#tag/Service-Tokens/operation/updateServiceTokenByUuid) |

### Route Filters

| Tool | Description | API Endpoint |
|---------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `search_route_filter` | Search for Cloud Router Route Filters | [Search Route Filters](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/searchRouteFilters) |
| `create_route_filter` | Create a new Route Filter for traffic management | [Create Route Filter](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/createRouteFilter) |
| `update_route_filter` | Update an existing Route Filter configuration | [Update Route Filter](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/patchRouteFilterByUuid) |
| `get_route_filter_change` | Retrieve a specific change or update log of an Equinix Route Filter Policy. | [Get Change By ID](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/getRouteFilterChangeByUuid) |
| `list_route_filter_changes` | Retrieve changes or update history of an Equinix Route Filter Policy. | [Get Route Filter Changes](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/getRouteFilterChanges) |
| `list_route_filter_connections` | Retrieve all connections using a specific Route Filter Policy. | [Get All Connections on Route Filter](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/getRouteFilterConnections) |
| `search_route_filter_attachments_for_fcr` | Search for Equinix Route Filter Attachments using advanced filtering, sorting, and pagination. | [Search Cloud Router Route Filter Attachments](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/searchCloudRouterRouteFilterAttachments) |
| `search_route_filters` | Search for Equinix Route Filter Policies using advanced filtering, sorting, and pagination. | [Search Route Filters](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filters/operation/searchRouteFilters) |

### Route Filter Rules

| Tool | Description | API Endpoint |
|------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `get_all_route_filter_rules` | List all rules for a specific Route Filter | [List Route Filter Rules](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filter-Rules/operation/getRouteFilterRules) |
| `get_route_filter_rule` | Get detailed information about a specific Route Filter Rule | [Get Route Filter Rule](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filter-Rules/operation/getRouteFilterRuleByUuid) |
| `create_route_filter_rule` | Create new rules for a Route Filter | [Create Route Filter Rules](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filter-Rules/operation/createRouteFilterRule) |
| `update_route_filter_rule` | Update an existing Route Filter Rule | [Update Route Filter Rule](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filter-Rules/operation/patchRouteFilterRuleByUuid) |
| `get_route_filter_rule_change` | Retrieve a specific change or update log of an Equinix Route Filter Rule. | [Get Change By ID](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filter-Rules/operation/getRouteFilterRuleChangeByUuid) |
| `list_route_filter_rule_changes` | Retrieve changes or update history of an Equinix Route Filter Rule. | [Get Route Filter Rule Changes](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filter-Rules/operation/getRouteFilterRuleChanges) |
| `list_route_filter_rules` | Retrieve all Route Filter Rules under a specific Route Filter Policy. | [Get Route Filter Rules](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Filter-Rules/operation/getRouteFilterRules) |

### Route Aggregation

| Tool                       | Description                                                                 | API Endpoint                                                                                        |
|----------------------------| -----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------| 
| `search_route_aggregation` | Search for Cloud Router Route Aggregation | [Search Route Aggregation](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/searchRouteAggregations) |
| `create_route_aggregation` | Create a new Route Aggregation for traffic management | [Create Route Aggregation](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/createRouteAggregation) |
| `update_route_aggregation` | Update an existing Route Aggregation configuration | [Update Route Aggregation](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/patchRouteAggregationByUuid) |
| `get_route_aggregation` | Retrieve details for a specific Route Aggregation Policy by UUID. | [Get Aggregation](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/getRouteAggregationByUuid) |
| `get_route_aggregation_change` | Retrieve a specific change or update log of an Equinix Route Aggregation Policy. | [Get Change By ID](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/getRouteAggregationChangeByUuid) |
| `list_route_aggregation_changes` | Retrieve changes or update history of an Equinix Route Aggregation Policy. | [Get Route Aggregation Changes](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/getRouteAggregationChanges) |
| `list_route_aggregation_connections` | Retrieve all connections using a specific Route Aggregation Policy. | [Get Route Aggregation Connections](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/getRouteAggregationConnections) |
| `search_route_aggregation_attachments_for_fcr` | Search for Equinix Route Aggregation Attachments using advanced filtering, sorting, and pagination. | [Search Cloud Router Route Aggregation Attachments](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/searchCloudRouterRouteAggregationAttachments) |
| `search_route_aggregations` | Search for Equinix Route Aggregation Policies using advanced filtering, sorting, and pagination. | [Search Route Aggregations](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregations/operation/searchRouteAggregations) |

### Route Aggregation Rules

| Tool                                     | Description                                                      | API Endpoint                                                                                                  |
|------------------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------| 
| `get_all_route_aggregation_rules` | List all rules for a specific Route Aggregation                  | [List Route Aggregation Rules](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregation-Rules/operation/getRouteAggregationRules) |
| `get_route_aggregation_rule`      | Get detailed information about a specific Route Aggregation Rule | [Get Route Aggregation Rule](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregation-Rules/operation/getRouteAggregationRuleByUuid) |
| `create_route_aggregation_rule`   | Create new rules for a Route Aggregation                              | [Create Route Aggregation Rules](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregation-Rules/operation/createRouteAggregationRule) |
| `update_route_aggregation_rule`   | Update an existing Route Aggregation Rule                             | [Update Route Aggregation Rule](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregation-Rules/operation/patchRouteAggregationRuleByUuid) |
| `get_route_aggregation_rule_change` | Retrieve a specific change or update log of an Equinix Route Aggregation Rule. | [Get Change By ID](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregation-Rules/operation/getRouteAggregationRuleChangeByUuid) |
| `list_route_aggregation_rule_changes` | Retrieve changes or update history of an Equinix Route Aggregation Rule. | [Get Route Aggregation Rule Changes](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregation-Rules/operation/getRouteAggregationRuleChanges) |
| `list_route_aggregation_rules` | Retrieve all Route Aggregation Rules under a specific Route Aggregation Policy. | [Get Route Aggregation Rules](https://docs.equinix.com/api-catalog/fabricv4/#tag/Route-Aggregation-Rules/operation/getRouteAggregationRules) |


### Observability - Streams

| Tool                                     | Description                                                             | API Endpoint                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------| 
| `list_streams`                     | List all telemetry streams in your account                              | [Get Streams](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/getStreams)                                                 |
| `get_stream_details`               | Get detailed information about a specific stream                        | [Get Stream Details](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/getStreamByUuid)                                     |
| `create_stream`                    | Create a new telemetry stream                                           | [Create Stream](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/createStreams)                                            |
| `update_stream`                    | Update an existing telemetry stream                                     | [Update Stream](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/updateStreamByUuid)                                       |
| `list_stream_attached_assets`      | List assets attached to a stream                                        | [List Stream Assets](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/getStreamAssetByUuid)                                |
| `get_stream_attached_asset_details` | Get details about a specific asset attached to a stream                 | [Get Stream Asset Details](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/getStreamAssetByUuid)                          |
| `attach_stream_asset`              | Attach an asset to a telemetry stream                                   | [Attach Asset to Stream](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/updateStreamAssetByUuid)                         |
| `search_attached_assets`           | Search for assets attached to a telemetry stream                        | [Search Asset to Stream](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/getStreamsAssets)                                |
| `list_stream_subscriptions`        | List all telemetry stream subscription for a specific telementry Stream | [List Stream Subscription](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Subscriptions/operation/getStreamSubscriptions)           |
| `get_stream_subscription_details`  | Get details about a specific telemetry stream subscription              | [Get Stream Subscription](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Subscriptions/operation/getStreamSubscriptionByUuid)       |
| `create_stream_subscription`       | Create a new telemetry stream subscription                              | [Create Stream Subscription](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Subscriptions/operation/createStreamSubscriptions)      |
| `update_stream_subscription`      | Update an existing telemetry stream subscription                        | [Update Stream Subscription](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Subscriptions/operation/updateStreamSubscriptionByUuid) |
| `get_stream` | Retrieve comprehensive details about an Equinix Fabric Stream. | [Get Stream](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/getStreamByUuid) |
| `get_stream_attached_asset` | Retrieve comprehensive details about a specific attached asset for an Equinix Fabric Stream. | [Get Asset](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/getStreamAssetByUuid) |
| `get_stream_network_edge_device` | Retrieve details of a network edge device attached to an Equinix Fabric Stream. | [API Reference](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/getStreamNetworkEdgeDevices) |
| `get_stream_subscription` | Retrieve comprehensive details about a specific stream subscription for an Equinix Fabric Stream. | [Get Subscription](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Subscriptions/operation/getStreamSubscriptionByUuid) |
| `list_stream_attached_assets_by_type` | Retrieve a list of all attached assets with the specified type for a specific Equinix Fabric Stream. | [API Reference](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/getStreamAssets) |
| `update_stream_network_edge_device` | Attach or replace a network edge device on an Equinix Fabric Stream. | [API Reference](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/updateStreamNetworkEdgeDevice) |
| `search_stream_subscriptions` | Search Equinix Fabric stream subscriptions using advanced filters, nested OR clauses, sorting, and pagination. | [Search Stream Subscriptions](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Subscriptions/operation/searchStreamSubscriptions) |
| `search_streams` | Search Equinix Fabric streams using filters, wildcard matching, sorting, and pagination. | [Search Streams](https://docs.equinix.com/api-catalog/fabricv4/#tag/Streams/operation/searchStreams) |

### Observability - Stream Alert Rules

| Tool | Description | API Endpoint |
|------------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `list_stream_alert_rules` | List all alert rules for a stream | [Get Alert Rules](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Alert-Rules/operation/getStreamAlertRules) |
| `get_stream_alert_rule_details` | Get detailed information about a specific alert rule | [Get Alert Rule Details](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Alert-Rules/operation/getStreamAlertRuleByUuid) |
| `create_stream_alert_rule` | Create a new alert rule for a stream | [Create Alert Rule](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Alert-Rules/operation/createStreamAlertRules) |
| `update_stream_alert_rule` | Update an existing alert rule | [Update Alert Rule](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Alert-Rules/operation/updateStreamAlertRuleByUuid) |
| `get_stream_alert_rule` | Retrieve comprehensive details about a specific alert rule for an Equinix Fabric Stream. | [Get Stream Alert Rule](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Alert-Rules/operation/getStreamAlertRuleByUuid) |
| `replace_stream_alert_rule` | Replace an existing alert rule for an Equinix Fabric Stream. | [Update Stream Alert Rule](https://docs.equinix.com/api-catalog/fabricv4/#tag/Stream-Alert-Rules/operation/updateStreamAlertRuleByUuid) |

### Observability - Cloud Events

| Tool | Description | API Endpoint |
|-------------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `get_cloud_event` | Get details about a specific cloud event | [Get Cloud Event](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Events/operation/getCloudEventByAssetId) |
| `search_cloud_events` | Search for cloud events across your Fabric resources | [Search Cloud Events](https://docs.equinix.com/api-catalog/fabricv4/#tag/Cloud-Events/operation/searchCloudEvents) |

### Observability - Metrics

| Tool | Description | API Endpoint |
|------------------|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| `get_metrics` | Get metrics for a specific asset by asset ID | [Get Metrics](https://docs.equinix.com/api-catalog/fabricv4/#tag/Metrics/operation/getMetricByAssetId) |
| `search_metrics` | Search for metrics across multiple assets | [Search Metrics](https://docs.equinix.com/api-catalog/fabricv4/#tag/Metrics/operation/searchMetrics) |
| `list_metrics_by_metros` | Retrieve real-time metric details for all Equinix Fabric Metros. | [Get Metrics by Name](https://docs.equinix.com/api-catalog/fabricv4/#tag/Metrics/operation/getMetricByName) |

### Application Domain

| Tool | Description | API Endpoint |
| --- | --- | --- |
| `create_application_domain` | Create a new Equinix Fabric Application Domain. | [Create Domain](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Domains/operation/createAppDomain) |
| `get_application_domain` | Retrieve details for a specific Fabric Application Domain by application domain ID. | [Get Domain](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Domains/operation/getAppDomainByUuid) |
| `search_application_domains` | Get a list of user's application domains using search criteria. | [Search Domains](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Domains/operation/searchAppDomains) |

### Application Link

| Tool | Description | API Endpoint |
| --- | --- | --- |
| `attach_application_domain_to_link` | Attach an application domain to an application link in Equinix Fabric. |  |
| `attach_application_service_to_link` | Attach a application service to a application link in Equinix Fabric. |  |
| `create_application_link` | Create a new Equinix Fabric Application Link. | [Create Link](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Links/operation/createAppLink) |
| `get_application_link` | Retrieve details for a specific Fabric Application Link by application link ID. | [Get Link](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Links/operation/getAppLinkByUuid) |
| `search_application_links` | Get a list of user's application links using search criteria. | [Search Links](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Links/operation/searchAppLinks) |

### Application Service

| Tool | Description | API Endpoint |
| --- | --- | --- |
| `create_application_service` | Create a new Equinix Fabric Application Service. | [Create Service](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Services/operation/createAppService) |
| `search_application_services` | Get a list of user's application services using search criteria. | [Search Services](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Services/operation/searchAppServices) |

### Application Subscription

| Tool | Description | API Endpoint |
| --- | --- | --- |
| `create_application_subscription` | Create a new Equinix Fabric application subscription for application link and application service. | [Create Subscription](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Subscriptions/operation/createAppSubscription) |
| `search_application_subscriptions` | Get a list of user's application subscriptions using search criteria. | [Search Subscriptions](https://docs.equinix.com/api-catalog/fabricv4/#tag/Application-Subscriptions/operation/searchAppSubscriptions) |

### Networks

| Tool | Description | API Endpoint |
| --- | --- | --- |
| `create_network` | Create a new Equinix Fabric Network. | [Create Network](https://docs.equinix.com/api-catalog/fabricv4/#tag/Networks/operation/createNetwork) |
| `search_networks` | Search for Equinix Fabric Networks using advanced filtering, sorting, and pagination. | [Search Networks](https://docs.equinix.com/api-catalog/fabricv4/#tag/Networks/operation/searchNetworks) |
| `update_network` | Update an Equinix Fabric Network attribute. | [Update Network By ID](https://docs.equinix.com/api-catalog/fabricv4/#tag/Networks/operation/updateNetworkByUuid) |

### Acl Templates

| Tool | Level | Description | API Reference |
| ----- | ----- | ----- | ----- |
| `list_acl_templates` | Viewer | Retrieve Network Edge ACL (Access Control List) templates for the account. | [Get ACL Templates](https://docs.equinix.com/api-catalog/network-edgev1/#tag/ACL-Template/operation/getDeviceACLTemplate) |

### Asns

| Tool | Level | Description | API Reference |
| ----- | ----- | ----- | ----- |
| `create_asn` | Operator | Create (provision) a new ASN. | [Create ASN](https://docs.equinix.com/api-catalog/fabricv4/#tag/ASNs/operation/createAsn) |
| `get_asn` | Viewer | Retrieve full details of a single ASN by its UUID. | [Get ASN](https://docs.equinix.com/api-catalog/fabricv4/#tag/ASNs/operation/getAsnById) |
| `search_asns` | Viewer | Search ASNs (Autonomous System Numbers) with filters, pagination and sort. | [Search ASNs](https://docs.equinix.com/api-catalog/fabricv4/#tag/ASNs/operation/searchAsns) |
| `update_asn_ownership_signature` | Operator | Submit the signed RPKI challenge to complete PUBLIC_ASN ownership proof. | [Update ASN](https://docs.equinix.com/api-catalog/fabricv4/#tag/ASNs/operation/patchAsnById) |

### Backups

| Tool | Level | Description | API Reference |
| ----- | ----- | ----- | ----- |
| `list_virtual_device_backups` | Viewer | List the backups of one Network Edge virtual device. | [Get Backups of Device](https://docs.equinix.com/api-catalog/network-edgev1/#tag/Device-Backup-and-Restore/operation/getDeviceBackups) |

### Company Profiles

| Tool | Level | Description | API Reference |
| ----- | ----- | ----- | ----- |
| `get_company_profile` | Viewer | Retrieve detailed information about a specific Equinix Fabric company profile by its UUID. | [Get Company Profile by ID](https://docs.equinix.com/api-catalog/fabricv4/#tag/Company-Profiles/operation/getCompanyProfile) |
| `list_company_profile_service_profiles` | Viewer | List all service profiles attached to an Equinix Fabric company profile. | [Get Service Profiles](https://docs.equinix.com/api-catalog/fabricv4/#tag/Company-Profiles/operation/getCompanyProfileServiceProfiles) |
| `search_company_profiles` | Viewer | Search for Equinix Fabric company profiles using advanced filtering, sorting, and pagination. | [Search Company Profiles](https://docs.equinix.com/api-catalog/fabricv4/#tag/Company-Profiles/operation/searchCompanyProfile) |

### Internet Access

| Tool | Level | Description | API Reference |
| ----- | ----- | ----- | ----- |
| `attach_ip_block_to_eia_service` | Operator | Add one IP block route to an EIA Internet Access service. | [Update Internet Access Service by ID](https://docs.equinix.com/api-catalog/fabricv4/#tag/Internet-Access-Services/operation/patchEiaService) |
| `create_internet_access_fabric_port` | Operator | Create an Equinix Internet Access Service (EIA) over a Fabric port. | [Create Internet Access Service](https://docs.equinix.com/api-catalog/fabricv4/#tag/Internet-Access-Services/operation/createEiaService) |
| `create_internet_access_network_edge` | Operator | Create an Equinix Internet Access Service (EIA) from a Network Edge virtual device. | [Create Internet Access Service](https://docs.equinix.com/api-catalog/fabricv4/#tag/Internet-Access-Services/operation/createEiaService) |
| `search_internet_access` | Viewer | Search for Equinix Internet Access Services (EIA) using advanced filtering, sorting, and pagination. | [Search Internet Access Services](https://docs.equinix.com/api-catalog/fabricv4/#tag/Internet-Access-Services/operation/searchEiaServices) |
| `update_internet_access_bandwidth` | Operator | Update the bandwidth of an existing Equinix Internet Access Service (EIA). | [Update Internet Access Service by ID](https://docs.equinix.com/api-catalog/fabricv4/#tag/Internet-Access-Services/operation/patchEiaService) |

### Ip Blocks

| Tool | Level | Description | API Reference |
| ----- | ----- | ----- | ----- |
| `create_ip_block` | Operator | Submit a new customer-owned (PI) or Equinix-assigned (PA) IP block request. | [Create IP Block](https://docs.equinix.com/api-catalog/fabricv4/#tag/IP-Blocks/operation/submitIpBlock) |
| `get_ip_block` | Viewer | Retrieve a single IP block by UUID. | [Retrieve IP Block by ID](https://docs.equinix.com/api-catalog/fabricv4/#tag/IP-Blocks/operation/getIpBlock) |
| `search_ip_blocks` | Viewer | Search IP blocks with filters, pagination, and sort. | [Search IP Blocks](https://docs.equinix.com/api-catalog/fabricv4/#tag/IP-Blocks/operation/searchIpBlocks) |



## Example Commands

Once you have configured the Fabric MCP server in your AI agent, you can use natural language to interact with your Fabric resources. The following are examples of common queries:

### Basic Queries

- **"Show me all active connections in the SV metro."** – Searches for and displays all active connections in the Silicon Valley metro.
- **"Which ports are currently over-utilized or have negative available bandwidth?"** – Analyzes port utilization to identify capacity issues.
- **"Summarize all my Fabric Cloud Routers."** – Provides an overview of all Cloud Routers in your account.
- **"How do I create a Cloud Router and what projects can I use?"** – Guides you through the Cloud Router creation process and lists available projects.
- **"Can you update the bandwidth for the connection named `<connection_name>`?"** – Modifies the bandwidth allocation for a specific connection.
- **"Can you ping this router-based connection?"** – Executes a ping command to test connectivity through a Cloud Router connection.

### Advanced Queries

The MCP server can help with complex analysis and optimization tasks:

- **"We're looking to rationalize our network footprint. Can you analyze our active and provisioned port, router, and connection utilization across all metros, identify underutilized resources, and suggest optimization strategies to reduce our monthly costs while maintaining performance? Also, can you suggest adding redundancy options to improve resiliency of our network?"** – Performs comprehensive network analysis to identify cost optimization opportunities while maintaining or improving network resilience.
- **"Find metros where we should establish redundant paths but currently don't have them."** – Analyzes network topology to identify single points of failure across metros and recommends redundancy improvements.
- **"Analyze our connection patterns and identify any single points of failure in our network topology."** – Examines connection architecture to detect vulnerabilities and suggest architectural improvements.
