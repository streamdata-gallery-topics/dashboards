swagger: "2.0"
x-collection-name: Server Density
x-complete: 1
info:
  title: Widgets API
  description: the-widgets-api-
  version: 1.0.0
host: api.serverdensity.io.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/dashboards/dashboardId:
    "":
      summary: Deleting a dashboard
      description: Deleting a dashboard.
      operationId: deleting-a-dashboard
      x-api-path-slug: usersdashboardsdashboardid-
      parameters:
      - in: path
        name: dashboardId
        description: ID of the dashboard to delete
        type: string
      - in: path
        name: layout
        description: Dictionary with the ids of the widgets from this dashboard as
          keys
        type: string
      - in: body
        name: layout
        description: Dictionary with the ids of the widgets from this dashboard as
          keys
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: Name of the dashboard
        type: string
      - in: body
        name: name
        description: Name of the dashboard
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: token
        description: Your API token
        type: string
      - in: body
        name: token
        description: Your API token
        schema:
          $ref: '#/definitions/holder'
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Dashboards
  /users/dashboards/duplicate/dasboardId:
    "":
      summary: Duplicating a dashboard
      description: Duplicating a dashboard.
      operationId: duplicating-a-dashboard
      x-api-path-slug: usersdashboardsduplicatedasboardid-
      parameters:
      - in: body
        name: dashboardId
        description: ID of the dashboard to duplicate
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: new_name
        description: Name of the new, duplicated dashboard
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: token
        description: Your API token
        schema:
          $ref: '#/definitions/holder'
      responses:
        apps:
          description: app_allow
        devices:
          description: device_link
        members:
          description: member_invite
        passwords:
          description: tfa_enable
        sharing:
          description: shmodel_create
        team_admin_actions:
          description: sf_external_accept_allow
      tags:
      - Dashboards