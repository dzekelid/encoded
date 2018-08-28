swagger: "2.0"
x-collection-name: Predix
x-complete: 1
info:
  title: VIEWS
  version: 1.0.0
host: thetaray-anomaly-service.run.aws-usw02-pr.ice.predix.io
basePath: /v1
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
    put:
      summary: Creates/Updates a given resource for a given zone. The resourceIdentifier
        must be URL encoded in application/x-www-form-urlencoded format with UTF-8.
      description: Creates/updates a given resource for a given zone. the resourceidentifier
        must be url encoded in application/x-www-form-urlencoded format with utf-8..
      operationId: putResourceV1UsingPUT_1
      x-api-path-slug: v1resourceresourceidentifier-put
      parameters:
      - in: body
        name: resource
        description: resource
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: resourceIdentifier
        description: resourceIdentifier
      responses:
        200:
          description: Successful response
      tags:
      - Creates
      - S
      - Given
      - Resourcea
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
    delete:
      summary: Deletes the resource for a given zone. The resourceIdentifier must
        be URL encoded in application/x-www-form-urlencoded format with UTF-8.
      description: Deletes the resource for a given zone. the resourceidentifier must
        be url encoded in application/x-www-form-urlencoded format with utf-8..
      operationId: deleteResourceV1UsingDELETE
      x-api-path-slug: v1resourceresourceidentifier-delete
      parameters:
      - in: path
        name: resourceIdentifier
        description: resourceIdentifier
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Resourcea
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
  /v1/subject/{subjectIdentifier}:
    get:
      summary: Retrieves the subject for the given zone. The subjectIdentifier must
        be URL encoded in application/x-www-form-urlencoded format with UTF-8.
      description: Retrieves the subject for the given zone. the subjectidentifier
        must be url encoded in application/x-www-form-urlencoded format with utf-8..
      operationId: getSubjectUsingGET
      x-api-path-slug: v1subjectsubjectidentifier-get
      parameters:
      - in: query
        name: includeInheritedAttributes
        description: includeInheritedAttributes
      - in: path
        name: subjectIdentifier
        description: subjectIdentifier
      responses:
        200:
          description: Successful response
      tags:
      - Retrieves
      - Subjectthe
      - Given
      - Zone
      - ""
      - SubjectIdentifier
      - Must
      - Be
      - URL
      - Encoded
      - In
      - Application
      - X-www-form-urlencoded
      - Format
      - UTF-8
    delete:
      summary: Deletes the subject for a given zone. The subjectIdentifier must be
        URL encoded in application/x-www-form-urlencoded format with UTF-8.
      description: Deletes the subject for a given zone. the subjectidentifier must
        be url encoded in application/x-www-form-urlencoded format with utf-8..
      operationId: deleteSubjectUsingDELETE_1
      x-api-path-slug: v1subjectsubjectidentifier-delete
      parameters:
      - in: path
        name: subjectIdentifier
        description: subjectIdentifier
      responses:
        200:
          description: Successful response
      tags:
      - S
      - Subjecta
      - Given
      - Zone
      - ""
      - SubjectIdentifier
      - Must
      - Be
      - URL
      - Encoded
      - In
      - Application
      - X-www-form-urlencoded
      - Format
      - UTF-8