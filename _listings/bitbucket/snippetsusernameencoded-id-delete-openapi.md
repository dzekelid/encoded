---
swagger: "2.0"
x-collection-name: Bitbucket
x-complete: 0
info:
  title: Bitbucket Delete Snippets Username Encoded
  description: Deletes a snippet and returns an empty response.
  termsOfService: https://www.atlassian.com/legal/customer-agreement
  contact:
    name: Bitbucket Support
    url: https://support.atlassian.com/bitbucket
    email: support@bitbucket.org
  version: 1.0.0
host: api.bitbucket.org
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /snippets/{username}/{encoded_id}:
    delete:
      summary: Delete Snippets Username Encoded
      description: Deletes a snippet and returns an empty response.
      operationId: deleteSnippetsUsernameEncoded
      x-api-path-slug: snippetsusernameencoded-id-delete
      parameters:
      - in: path
        name: encoded_id
        description: The snippets id
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
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