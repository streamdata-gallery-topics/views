---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Users API List user page views
  description: List user page views.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/{user_id}/page_views:
    get:
      summary: List user page views
      description: List user page views.
      operationId: list-user-page-views
      x-api-path-slug: usersuser-idpage-views-get
      parameters:
      - in: query
        name: end_time
        description: The end of the time range from which you want page views
      - in: query
        name: start_time
        description: The beginning of the time range from which you want page views
      responses:
        200:
          description: OK
      tags:
      - Users
      - User
      - Id
      - Page
      - Views
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