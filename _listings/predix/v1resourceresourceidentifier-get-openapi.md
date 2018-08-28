---
swagger: "2.0"
x-collection-name: Predix
x-complete: 0
info:
  title: Predix Access Control Retrieves the resource for the given zone. The resourceIdentifier
    must be URL encoded in application/x-www-form-urlencoded format with UTF-8.
  description: Retrieves the resource for the given zone. the resourceidentifier must
    be url encoded in application/x-www-form-urlencoded format with utf-8..
  version: 1.0.0
host: predix-acs.run.aws-usw02-pr.ice.predix.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/resource/{resourceIdentifier}:
    get:
      summary: Retrieves the resource for the given zone. The resourceIdentifier must
        be URL encoded in application/x-www-form-urlencoded format with UTF-8.
      description: Retrieves the resource for the given zone. the resourceidentifier
        must be url encoded in application/x-www-form-urlencoded format with utf-8..
      operationId: getResourceV1UsingGET
      x-api-path-slug: v1resourceresourceidentifier-get
      parameters:
      - in: query
        name: includeInheritedAttributes
        description: includeInheritedAttributes
      - in: path
        name: resourceIdentifier
        description: resourceIdentifier
      responses:
        200:
          description: Successful response
      tags:
      - Retrieves
      - Resourcethe
      - Given
      - Zone
      - ""
      - ResourceIdentifier
      - Must
      - Be
      - URL
      - Encoded
      - In
      - Application
      - X-www-form-urlencoded
      - Format
      - UTF-8
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