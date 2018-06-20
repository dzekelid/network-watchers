---
swagger: "2.0"
x-collection-name: Azure Virtual Network
x-complete: 1
info:
  title: NetworkManagementClient
  description: the-microsoft-azure-network-management-api-provides-a-restful-set-of-web-services-that-interact-with-microsoft-azure-networks-service-to-manage-your-network-resources--the-api-has-entities-that-capture-the-relationship-between-an-end-user-and-the-microsoft-azure-networks-service-
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers/{networkWatcherName}
  : put:
      summary: Network Watchers Create Or Update
      description: Creates or updates a network watcher in the specified resource
        group.
      operationId: NetworkWatchers_CreateOrUpdate
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchername-put
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters that define the network watcher resource
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
    get:
      summary: Network Watchers Get
      description: Gets the specified network watcher by resource group.
      operationId: NetworkWatchers_Get
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchername-get
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
    delete:
      summary: Network Watchers Delete
      description: Deletes the specified network watcher resource.
      operationId: NetworkWatchers_Delete
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchername-delete
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers:
    get:
      summary: Network Watchers List
      description: Gets all network watchers by resource group.
      operationId: NetworkWatchers_List
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchers-get
      parameters:
      - in: query
        name: No Name
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  /subscriptions/{subscriptionId}/providers/Microsoft.Network/networkWatchers:
    get:
      summary: Network Watchers List All
      description: Gets all network watchers by subscription.
      operationId: NetworkWatchers_ListAll
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-networknetworkwatchers-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers/{networkWatcherName}/topology
  : post:
      summary: Network Watchers Get Topology
      description: Gets the current network topology by resource group.
      operationId: NetworkWatchers_GetTopology
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchernametopology-post
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters that define the representation of topology
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers/{networkWatcherName}/ipFlowVerify
  : post:
      summary: Network Watchers Verify IPFlow
      description: Verify IP flow from the specified VM to a location given the currently
        configured NSG rules.
      operationId: NetworkWatchers_VerifyIPFlow
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchernameipflowverify-post
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters that define the IP flow to be verified
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers/{networkWatcherName}/nextHop
  : post:
      summary: Network Watchers Get Next Hop
      description: Gets the next hop from the specified VM.
      operationId: NetworkWatchers_GetNextHop
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchernamenexthop-post
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters that define the source and destination endpoint
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers/{networkWatcherName}/securityGroupView
  : post:
      summary: Network Watchers Get VMSecurity Rules
      description: Gets the configured and effective security group rules on the specified
        VM.
      operationId: NetworkWatchers_GetVMSecurityRules
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchernamesecuritygroupview-post
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters that define the VM to check security groups for
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers/{networkWatcherName}/troubleshoot
  : post:
      summary: Network Watchers Get Troubleshooting
      description: Initiate troubleshooting on a specified resource
      operationId: NetworkWatchers_GetTroubleshooting
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchernametroubleshoot-post
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher resource
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters that define the resource to troubleshoot
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers/{networkWatcherName}/queryTroubleshootResult
  : post:
      summary: Network Watchers Get Troubleshooting Result
      description: Get the last completed troubleshooting result on a specified resource
      operationId: NetworkWatchers_GetTroubleshootingResult
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchernamequerytroubleshootresult-post
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher resource
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters that define the resource to query the troubleshooting
          result
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers/{networkWatcherName}/configureFlowLog
  : post:
      summary: Network Watchers Set Flow Log Configuration
      description: Configures flow log on a specified resource.
      operationId: NetworkWatchers_SetFlowLogConfiguration
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchernameconfigureflowlog-post
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher resource
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters that define the configuration of flow log
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the network watcher resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
  ? /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/networkWatchers/{networkWatcherName}/queryFlowLogStatus
  : post:
      summary: Network Watchers Get Flow Log Status
      description: Queries status of flow log on a specified resource.
      operationId: NetworkWatchers_GetFlowLogStatus
      x-api-path-slug: subscriptionssubscriptionidresourcegroupsresourcegroupnameprovidersmicrosoft-networknetworkwatchersnetworkwatchernamequeryflowlogstatus-post
      parameters:
      - in: path
        name: networkWatcherName
        description: The name of the network watcher resource
      - in: query
        name: No Name
      - in: body
        name: parameters
        description: Parameters that define a resource to query flow log status
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceGroupName
        description: The name of the network watcher resource group
      responses:
        200:
          description: OK
      tags:
      - Network Watchers
---