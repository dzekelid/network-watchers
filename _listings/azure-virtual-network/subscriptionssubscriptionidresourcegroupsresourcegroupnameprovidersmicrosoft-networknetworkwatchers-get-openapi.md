---
swagger: "2.0"
x-collection-name: Azure Virtual Network
x-complete: 0
info:
  title: Azure Virtual Network API Network Watchers List
  description: Gets all network watchers by resource group.
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
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---