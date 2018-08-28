---
name: HERE
x-slug: here
description: HERE Technologies enables people, enterprises and cities around the world
  to harness the power of location and create innovative solutions that make our lives
  safer and more efficient. We transform information from devices, vehicles, infrastructure
  and...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
x-kinRank: "7"
x-alexaRank: "3011"
tags: Encoded
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/here/apis.md
specificationVersion: "0.14"
apis:
- name: Map Tile API - Multiple Base64 Encoded Map Tiles
  x-api-slug: maptilenewestnormal-day63024256png8-get
  description: "*Request multiple base64 encoded map tiles*\n\nA square consisting
    of multiple base64 encoded tiles is requested by adding the parameters `output=base64`
    and `range=NxN` to the request URL. The `column` and `row` in the path of the
    URL, defining the top left-hand corner of the tile group must be divisible by
    the value of the `range` parameter.\n  \n  Click on the response to decode the
    tiles returned.\n\n\n\n* **output**  `text`\n \\- Indicates whether to return
    the tile as base64 encoded text.\n\n* **range**  `enum`\n \\- Indicates the size
    of the array of tiles returned. Valid values are `2x2`, `3x3` or `4x4`\n\n Valid
    values are : `2x2`, `3x3`, `4x4`\n\n* **app_id**  `text`\n \\- A 20 byte Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an `app_id` with every request.\n\n* **app_code**  `text`\n
    \\- A 20 byte Base64 URL-safe encoded string used for the authentication of the
    client application.    You must include an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/here/maptilenewestnormal-day63024256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/here/maptilenewestnormal-day63024256png8-get-openapi.md
- name: Map Tile API - Base64 Encoded Map Tile
  x-api-slug: maptilenewestnormal-day11525761256png8-get
  description: "*Request a base64 encoded map tile*\n\nBase64 encoded tiles are requested
    by adding the parameter `output=base64` to the request URL.\n  \n  Click on the
    response to decode the tile returned.\n\n\n\n* **output**  `text`\n \\- Indicates
    whether to return the tile as base64 encoded text.\n\n* **app_id**  `text`\n \\-
    A 20 byte Base64 URL-safe encoded string used for the authentication of the client
    application.    You must include an `app_id` with every request.\n\n* **app_code**
    \ `text`\n \\- A 20 byte Base64 URL-safe encoded string used for the authentication
    of the client application.    You must include an `app_code` with every request."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://1.aerial.maps.cit.api.here.com//maptile/2.1/maptile/newest
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/here/maptilenewestnormal-day11525761256png8-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/here/maptilenewestnormal-day11525761256png8-get-openapi.md
- name: Venue Maps - Base64 Encoded Map Tiles
  x-api-slug: 0tilesiab64l112022001101210030210-js-get
  description: |-
    *Request a base64 encoded map tile and associated room definitions with a single request*

    A base64 encoded map tile together with the room definitions, is requested by passing `tiles-ia-b64` in the path of the request URL, along with a known `floor` and `quadkey` and associated authentication credentials.



    * **app_id**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_id` with every request.

    * **app_code**  `text`
     \- A 20 byte Base64 URL-safe encoded string used for the authentication of the client application.    You must include an `app_code` with every request.

    * **Signature**  `text`
     \- Signature

    * **Policy**  `text`
     \- Policy

    * **Key-Pair-Id**  `text`
     \- Key-Pair-Id
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://signature.venue.maps.cit.api.here.com//venues/signature
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/here/0tilesiab64l112022001101210030210-js-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/here/0tilesiab64l112022001101210030210-js-get-openapi.md
x-common:
- type: x-blog-rss
  url: https://developer.here.com/blog/feed
- type: x-github
  url: https://github.com/heremaps
- type: x-postman-collection
  url: https://github.com/heremaps/postman-collections
- type: x-api-gallery
  url: http://healthcare.gov.api.gallery.streamdata.io
- type: x-api-stack
  url: http://here.stack.network
- type: x-blog
  url: https://developer.here.com/blog
- type: x-crunchbase
  url: https://crunchbase.com/organization/here-inc
- type: x-developer
  url: https://developer.here.com
- type: x-email
  url: dirk.popp@here.com
- type: x-email
  url: sebastian.kurme@here.com
- type: x-email
  url: jordan.stark@here.com
- type: x-email
  url: amy.stupavsky@here.com
- type: x-email
  url: minna.laub@here.com
- type: x-email
  url: stefanie.sirc@here.com
- type: x-email
  url: rachel.kuta@here.com
- type: x-email
  url: laurel.davis-lyons@here.com
- type: x-email
  url: linda.bradley@here.com
- type: x-email
  url: press@here.com
- type: x-twitter
  url: https://twitter.com/here
- type: x-website
  url: https://here.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---