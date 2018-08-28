---
name: Bitbucket
x-slug: bitbucket
description: Collaborate on code with inline comments and pull requests. Manage and
  share your Git repositories to build and ship software, as a team.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
x-kinRank: "8"
x-alexaRank: "901"
tags: Encoded
created: "2018-08-27"
modified: "2018-08-27"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/apis.md
specificationVersion: "0.14"
apis:
- name: Bitbucket - Delete Snippets Username Encoded
  x-api-slug: snippetsusernameencoded-id-delete
  description: Deletes a snippet and returns an empty response.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-id-delete-openapi.md
- name: Bitbucket - Get Snippets Username Encoded
  x-api-slug: snippetsusernameencoded-id-get
  description: |-
    Retrieves a single snippet.

    Snippets support multiple content types:

    * application/json
    * multipart/related
    * multipart/form-data


    application/json
    ----------------

    The default content type of the response is `application/json`.
    Since JSON is always `utf-8`, it cannot reliably contain file contents
    for files that are not text. Therefore, JSON snippet documents only
    contain the filename and links to the file contents.

    This means that in order to retrieve all parts of a snippet, N+1
    requests need to be made (where N is the number of files in the
    snippet).


    multipart/related
    -----------------

    To retrieve an entire snippet in a single response, use the
    `Accept: multipart/related` HTTP request header.

        $ curl -H "Accept: multipart/related" https://api.bitbucket.org/2.0/snippets/evzijst/1

    Response:

        HTTP/1.1 200 OK
        Content-Length: 2214
        Content-Type: multipart/related; start="snippet"; boundary="===============1438169132528273974=="
        MIME-Version: 1.0

        --===============1438169132528273974==
        Content-Type: application/json; charset="utf-8"
        MIME-Version: 1.0
        Content-ID: snippet

        {
          "links": {
            "self": {
              "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj"
            },
            "html": {
              "href": "https://bitbucket.org/snippets/evzijst/kypj"
            },
            "comments": {
              "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/comments"
            },
            "watchers": {
              "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/watchers"
            },
            "commits": {
              "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/commits"
            }
          },
          "id": kypj,
          "title": "My snippet",
          "created_on": "2014-12-29T22:22:04.790331+00:00",
          "updated_on": "2014-12-29T22:22:04.790331+00:00",
          "is_private": false,
          "files": {
            "foo.txt": {
              "links": {
                "self": {
                  "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/files/367ab19/foo.txt"
                },
                "html": {
                  "href": "https://bitbucket.org/snippets/evzijst/kypj#file-foo.txt"
                }
              }
            },
            "image.png": {
              "links": {
                "self": {
                  "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/files/367ab19/image.png"
                },
                "html": {
                  "href": "https://bitbucket.org/snippets/evzijst/kypj#file-image.png"
                }
              }
            }
          ],
          "owner": {
            "username": "evzijst",
            "display_name": "Erik van Zijst",
            "uuid": "{d301aafa-d676-4ee0-88be-962be7417567}",
            "links": {
              "self": {
                "href": "https://api.bitbucket.org/2.0/users/evzijst"
              },
              "html": {
                "href": "https://bitbucket.org/evzijst"
              },
              "avatar": {
                "href": "https://bitbucket-staging-assetroot.s3.amazonaws.com/c/photos/2013/Jul/31/erik-avatar-725122544-0_avatar.png"
              }
            }
          },
          "creator": {
            "username": "evzijst",
            "display_name": "Erik van Zijst",
            "uuid": "{d301aafa-d676-4ee0-88be-962be7417567}",
            "links": {
              "self": {
                "href": "https://api.bitbucket.org/2.0/users/evzijst"
              },
              "html": {
                "href": "https://bitbucket.org/evzijst"
              },
              "avatar": {
                "href": "https://bitbucket-staging-assetroot.s3.amazonaws.com/c/photos/2013/Jul/31/erik-avatar-725122544-0_avatar.png"
              }
            }
          }
        }

        --===============1438169132528273974==
        Content-Type: text/plain; charset="us-ascii"
        MIME-Version: 1.0
        Content-Transfer-Encoding: 7bit
        Content-ID: "foo.txt"
        Content-Disposition: attachment; filename="foo.txt"

        foo

        --===============1438169132528273974==
        Content-Type: image/png
        MIME-Version: 1.0
        Content-Transfer-Encoding: base64
        Content-ID: "image.png"
        Content-Disposition: attachment; filename="image.png"

        iVBORw0KGgoAAAANSUhEUgAAABQAAAAoCAYAAAD+MdrbAAABD0lEQVR4Ae3VMUoDQRTG8ccUaW2m
        TKONFxArJYJamCvkCnZTaa+VnQdJSBFl2SMsLFrEWNjZBZs0JgiL/+KrhhVmJRbCLPx4O+/DT2TB
        cbblJxf+UWFVVRNsEGAtgvJxnLm2H+A5RQ93uIl+3632PZyl/skjfOn9Gvdwmlcw5aPUwimG+NT5
        EnNN036IaZePUuIcK533NVfal7/5yjWeot2z9ta1cAczHEf7I+3J0ws9Cgx0fsOFpmlfwKcWPuBQ
        73Oc4FHzBaZ8llq4q1mr5B2mOUCt815qYR8eB1hG2VJ7j35q4RofaH7IG+Xrf/PfJhfmwtfFYoIN
        AqxFUD6OMxcvkO+UfKfkOyXfKdsv/AYCHMLVkHAFWgAAAABJRU5ErkJggg==
        --===============1438169132528273974==--

    multipart/form-data
    -------------------

    As with creating new snippets, `multipart/form-data` can be used as an
    alternative to `multipart/related`. However, the inherently flat
    structure of form-data means that only basic, root-level properties
    can be returned, while nested elements like `links` are omitted:

        $ curl -H "Accept: multipart/form-data" https://api.bitbucket.org/2.0/snippets/evzijst/kypj

    Response:

        HTTP/1.1 200 OK
        Content-Length: 951
        Content-Type: multipart/form-data; boundary=----------------------------63a4b224c59f

        ------------------------------63a4b224c59f
        Content-Disposition: form-data; name="title"
        Content-Type: text/plain; charset="utf-8"

        My snippet
        ------------------------------63a4b224c59f--
        Content-Disposition: attachment; name="file"; filename="foo.txt"
        Content-Type: text/plain

        foo

        ------------------------------63a4b224c59f
        Content-Disposition: attachment; name="file"; filename="image.png"
        Content-Transfer-Encoding: base64
        Content-Type: application/octet-stream

        iVBORw0KGgoAAAANSUhEUgAAABQAAAAoCAYAAAD+MdrbAAABD0lEQVR4Ae3VMUoDQRTG8ccUaW2m
        TKONFxArJYJamCvkCnZTaa+VnQdJSBFl2SMsLFrEWNjZBZs0JgiL/+KrhhVmJRbCLPx4O+/DT2TB
        cbblJxf+UWFVVRNsEGAtgvJxnLm2H+A5RQ93uIl+3632PZyl/skjfOn9Gvdwmlcw5aPUwimG+NT5
        EnNN036IaZePUuIcK533NVfal7/5yjWeot2z9ta1cAczHEf7I+3J0ws9Cgx0fsOFpmlfwKcWPuBQ
        73Oc4FHzBaZ8llq4q1mr5B2mOUCt815qYR8eB1hG2VJ7j35q4RofaH7IG+Xrf/PfJhfmwtfFYoIN
        AqxFUD6OMxcvkO+UfKfkOyXfKdsv/AYCHMLVkHAFWgAAAABJRU5ErkJggg==
        ------------------------------5957323a6b76--
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-id-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded
  x-api-slug: snippetsusernameencoded-id-parameters
  description: Parameters snippets username encoded
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-id-parameters-openapi.md
- name: Bitbucket - Update Snippets Username Encoded
  x-api-slug: snippetsusernameencoded-id-put
  description: |-
    Used to update a snippet. Use this to add and delete files and to
    change a snippet's title.

    To update a snippet, one can either PUT a full snapshot, or only the
    parts that need to be changed.

    The contract for PUT on this API is that properties missing from the
    request remain untouched so that snippets can be efficiently
    manipulated with differential payloads.

    To delete a property (e.g. the title, or a file), include its name in
    the request, but omit its value (use `null`).

    As in Git, explicit renaming of files is not supported. Instead, to
    rename a file, delete it and add it again under another name. This can
    be done atomically in a single request. Rename detection is left to
    the SCM.

    PUT supports three different content types for both request and
    response bodies:

    * `application/json`
    * `multipart/related`
    * `multipart/form-data`

    The content type used for the request body can be different than that
    used for the response. Content types are specified using standard HTTP
    headers.

    Use the `Content-Type` and `Accept` headers to select the desired
    request and response format.


    application/json
    ----------------

    As with creation and retrieval, the content type determines what
    properties can be manipulated. `application/json` does not support
    file contents and is therefore limited to a snippet's meta data.

    To update the title, without changing any of its files:

        $ curl -X POST -H "Content-Type: application/json" https://api.bitbucket.org/2.0/snippets/evzijst/kypj             -d '{"title": "Updated title"}'


    To delete the title:

        $ curl -X POST -H "Content-Type: application/json" https://api.bitbucket.org/2.0/snippets/evzijst/kypj             -d '{"title": null}'

    Not all parts of a snippet can be manipulated. The owner and creator
    for instance are immutable.


    multipart/related
    -----------------

    `multipart/related` can be used to manipulate all of a snippet's
    properties. The body is identical to a POST. properties omitted from
    the request are left unchanged. Since the `start` part contains JSON,
    the mechanism for manipulating the snippet's meta data is identical
    to `application/json` requests.

    To update one of a snippet's file contents, while also changing its
    title:

        PUT /2.0/snippets/evzijst/kypj HTTP/1.1
        Content-Length: 288
        Content-Type: multipart/related; start="snippet"; boundary="===============1438169132528273974=="
        MIME-Version: 1.0

        --===============1438169132528273974==
        Content-Type: application/json; charset="utf-8"
        MIME-Version: 1.0
        Content-ID: snippet

        {
          "title": "My updated snippet",
          "files": {
              "foo.txt": {}
            }
        }

        --===============1438169132528273974==
        Content-Type: text/plain; charset="us-ascii"
        MIME-Version: 1.0
        Content-Transfer-Encoding: 7bit
        Content-ID: "foo.txt"
        Content-Disposition: attachment; filename="foo.txt"

        Updated file contents.

        --===============1438169132528273974==--

    Here only the parts that are changed are included in the body. The
    other files remain untouched.

    Note the use of the `files` list in the JSON part. This list contains
    the files that are being manipulated. This list should have
    corresponding multiparts in the request that contain the new contents
    of these files.

    If a filename in the `files` list does not have a corresponding part,
    it will be deleted from the snippet, as shown below:

        PUT /2.0/snippets/evzijst/kypj HTTP/1.1
        Content-Length: 188
        Content-Type: multipart/related; start="snippet"; boundary="===============1438169132528273974=="
        MIME-Version: 1.0

        --===============1438169132528273974==
        Content-Type: application/json; charset="utf-8"
        MIME-Version: 1.0
        Content-ID: snippet

        {
          "files": {
            "image.png": {}
          }
        }

        --===============1438169132528273974==--

    To simulate a rename, delete a file and add the same file under
    another name:

        PUT /2.0/snippets/evzijst/kypj HTTP/1.1
        Content-Length: 212
        Content-Type: multipart/related; start="snippet"; boundary="===============1438169132528273974=="
        MIME-Version: 1.0

        --===============1438169132528273974==
        Content-Type: application/json; charset="utf-8"
        MIME-Version: 1.0
        Content-ID: snippet

        {
            "files": {
              "foo.txt": {},
              "bar.txt": {}
            }
        }

        --===============1438169132528273974==
        Content-Type: text/plain; charset="us-ascii"
        MIME-Version: 1.0
        Content-Transfer-Encoding: 7bit
        Content-ID: "bar.txt"
        Content-Disposition: attachment; filename="bar.txt"

        foo

        --===============1438169132528273974==--


    multipart/form-data
    -----------------

    Again, one can also use `multipart/form-data` to manipulate file
    contents and meta data atomically.

        $ curl -X PUT http://localhost:12345/2.0/snippets/evzijst/kypj             -F title="My updated snippet" -F file=@foo.txt

        PUT /2.0/snippets/evzijst/kypj HTTP/1.1
        Content-Length: 351
        Content-Type: multipart/form-data; boundary=----------------------------63a4b224c59f

        ------------------------------63a4b224c59f
        Content-Disposition: form-data; name="file"; filename="foo.txt"
        Content-Type: text/plain

        foo

        ------------------------------63a4b224c59f
        Content-Disposition: form-data; name="title"

        My updated snippet
        ------------------------------63a4b224c59f

    To delete a file, omit its contents while including its name in the
    `files` field:

        $ curl -X PUT https://api.bitbucket.org/2.0/snippets/evzijst/kypj -F files=image.png

        PUT /2.0/snippets/evzijst/kypj HTTP/1.1
        Content-Length: 149
        Content-Type: multipart/form-data; boundary=----------------------------ef8871065a86

        ------------------------------ef8871065a86
        Content-Disposition: form-data; name="files"

        image.png
        ------------------------------ef8871065a86--

    The explicit use of the `files` element in `multipart/related` and
    `multipart/form-data` is only required when deleting files.
    The default mode of operation is for file parts to be processed,
    regardless of whether or not they are listed in `files`, as a
    convenience to the client.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-id-put-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Comments
  x-api-slug: snippetsusernameencoded-idcomments-get
  description: |-
    Used to retrieve a paginated list of all comments for a specific
    snippet.

    This resource works identical to commit and pull request comments.

    The default sorting is oldest to newest and can be overridden with
    the `sort` query parameter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcomments-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Comments
  x-api-slug: snippetsusernameencoded-idcomments-parameters
  description: Parameters snippets username encoded  comments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcomments-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcomments-parameters-openapi.md
- name: Bitbucket - Add Snippets Username Encoded  Comments
  x-api-slug: snippetsusernameencoded-idcomments-post
  description: |-
    Creates a new comment.

    The only required field in the body is `content.raw`.

    To create a threaded reply to an existing comment, include `parent.id`.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcomments-post-openapi.md
- name: Bitbucket - Delete Snippets Username Encoded  Comments Comment
  x-api-slug: snippetsusernameencoded-idcommentscomment-id-delete
  description: |-
    Deletes a snippet comment.

    Comments can only be removed by their author.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-delete-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Comments Comment
  x-api-slug: snippetsusernameencoded-idcommentscomment-id-get
  description: Get snippets username encoded  comments comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Comments Comment
  x-api-slug: snippetsusernameencoded-idcommentscomment-id-parameters
  description: Parameters snippets username encoded  comments comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-parameters-openapi.md
- name: Bitbucket - Update Snippets Username Encoded  Comments Comment
  x-api-slug: snippetsusernameencoded-idcommentscomment-id-put
  description: |-
    Updates a comment.

    Comments can only be updated by their author.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-put-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Commits
  x-api-slug: snippetsusernameencoded-idcommits-get
  description: Returns the changes (commits) made on this snippet.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommits-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Commits
  x-api-slug: snippetsusernameencoded-idcommits-parameters
  description: Parameters snippets username encoded  commits
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommits-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommits-parameters-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Commits Revision
  x-api-slug: snippetsusernameencoded-idcommitsrevision-get
  description: Get snippets username encoded  commits revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Commits Revision
  x-api-slug: snippetsusernameencoded-idcommitsrevision-parameters
  description: Parameters snippets username encoded  commits revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-parameters-openapi.md
- name: Bitbucket - Delete Snippets Username Encoded  Watch
  x-api-slug: snippetsusernameencoded-idwatch-delete
  description: |-
    Used to stop watching a specific snippet. Returns 204 (No Content)
    to indicate success.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatch-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatch-delete-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Watch
  x-api-slug: snippetsusernameencoded-idwatch-get
  description: |-
    Used to check if the current user is watching a specific snippet.

    Returns 204 (No Content) if the user is watching the snippet and 404 if
    not.

    Hitting this endpoint anonymously always returns a 404.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatch-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Watch
  x-api-slug: snippetsusernameencoded-idwatch-parameters
  description: Parameters snippets username encoded  watch
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatch-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatch-parameters-openapi.md
- name: Bitbucket - Update Snippets Username Encoded  Watch
  x-api-slug: snippetsusernameencoded-idwatch-put
  description: Used to start watching a specific snippet. Returns 204 (No Content).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatch-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatch-put-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Watchers
  x-api-slug: snippetsusernameencoded-idwatchers-get
  description: Returns a paginated list of all users watching a specific snippet.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatchers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatchers-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Watchers
  x-api-slug: snippetsusernameencoded-idwatchers-parameters
  description: Parameters snippets username encoded  watchers
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatchers-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idwatchers-parameters-openapi.md
- name: Bitbucket - Delete Snippets Username Encoded  Node
  x-api-slug: snippetsusernameencoded-idnode-id-delete
  description: |-
    Deletes the snippet.

    Note that this only works for versioned URLs that point to the latest
    commit of the snippet. Pointing to an older commit results in a 405
    status code.

    To delete a snippet, regardless of whether or not concurrent changes
    are being made to it, use `DELETE /snippets/{encoded_id}` instead.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-delete-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Node
  x-api-slug: snippetsusernameencoded-idnode-id-get
  description: |-
    Identical to `GET /snippets/encoded_id`, except that this endpoint
    can be used to retrieve the contents of the snippet as it was at an
    older revision, while `/snippets/encoded_id` always returns the
    snippet's current revision.

    Note that only the snippet's file contents are versioned, not its
    meta data properties like the title.

    Other than that, the two endpoints are identical in behavior.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Node
  x-api-slug: snippetsusernameencoded-idnode-id-parameters
  description: Parameters snippets username encoded  node
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-parameters-openapi.md
- name: Bitbucket - Update Snippets Username Encoded  Node
  x-api-slug: snippetsusernameencoded-idnode-id-put
  description: |-
    Identical to `UPDATE /snippets/encoded_id`, except that this endpoint
    takes an explicit commit revision. Only the snippet's "HEAD"/"tip"
    (most recent) version can be updated and requests on all other,
    older revisions fail by returning a 405 status.

    Usage of this endpoint over the unrestricted `/snippets/encoded_id`
    could be desired if the caller wants to be sure no concurrent
    modifications have taken place between the moment of the UPDATE
    request and the original GET.

    This can be considered a so-called "Compare And Swap", or CAS
    operation.

    Other than that, the two endpoints are identical in behavior.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-put-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Node  Files Path
  x-api-slug: snippetsusernameencoded-idnode-idfilespath-get
  description: |-
    Retrieves the raw contents of a specific file in the snippet. The
    `Content-Disposition` header will be "attachment" to avoid issues with
    malevolent executable files.

    The file's mime type is derived from its filename and returned in the
    `Content-Type` header.

    Note that for text files, no character encoding is included as part of
    the content type.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-idfilespath-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-idfilespath-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Node  Files Path
  x-api-slug: snippetsusernameencoded-idnode-idfilespath-parameters
  description: Parameters snippets username encoded  node  files path
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-idfilespath-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idnode-idfilespath-parameters-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Revision Diff
  x-api-slug: snippetsusernameencoded-idrevisiondiff-get
  description: |-
    Returns the diff of the specified commit against its first parent.

    Note that this resource is different in functionality from the `patch`
    resource.

    The differences between a diff and a patch are:

    * patches have a commit header with the username, message, etc
    * diffs support the optional `path=foo/bar.py` query param to filter the
      diff to just that one file diff (not supported for patches)
    * for a merge, the diff will show the diff between the merge commit and
      its first parent (identical to how PRs work), while patch returns a
      response containing separate patches for each commit on the second
      parent's ancestry, up to the oldest common ancestor (identical to
      its reachability).

    Note that the character encoding of the contents of the diff is
    unspecified as Git and Mercurial do not track this, making it hard for
    Bitbucket to reliably determine this.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idrevisiondiff-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idrevisiondiff-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Revision Diff
  x-api-slug: snippetsusernameencoded-idrevisiondiff-parameters
  description: Parameters snippets username encoded  revision diff
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idrevisiondiff-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idrevisiondiff-parameters-openapi.md
- name: Bitbucket - Get Snippets Username Encoded  Revision Patch
  x-api-slug: snippetsusernameencoded-idrevisionpatch-get
  description: |-
    Returns the patch of the specified commit against its first
    parent.

    Note that this resource is different in functionality from the `diff`
    resource.

    The differences between a diff and a patch are:

    * patches have a commit header with the username, message, etc
    * diffs support the optional `path=foo/bar.py` query param to filter the
      diff to just that one file diff (not supported for patches)
    * for a merge, the diff will show the diff between the merge commit and
      its first parent (identical to how PRs work), while patch returns a
      response containing separate patches for each commit on the second
      parent's ancestry, up to the oldest common ancestor (identical to
      its reachability).

    Note that the character encoding of the contents of the patch is
    unspecified as Git and Mercurial do not track this, making it hard for
    Bitbucket to reliably determine this.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idrevisionpatch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idrevisionpatch-get-openapi.md
- name: Bitbucket - Parameters Snippets Username Encoded  Revision Patch
  x-api-slug: snippetsusernameencoded-idrevisionpatch-parameters
  description: Parameters snippets username encoded  revision patch
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Imports, Stack Network, Developers, Code, Technology, SaaS, Enterprise, Profiles,
    Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idrevisionpatch-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/encoded/master/_listings/bitbucket/snippetsusernameencoded-idrevisionpatch-parameters-openapi.md
x-common:
- type: x-api-gallery
  url: http://bigoven.api.gallery.streamdata.io
- type: x-api-stack
  url: http://bitbucket.stack.network
- type: x-crunchbase
  url: https://crunchbase.com/organization/bitbucket
- type: x-developer
  url: https://developer.atlassian.com/cloud/bitbucket/
- type: x-documentation
  url: https://confluence.atlassian.com/bitbucket/bitbucket-cloud-documentation-221448814.html?_ga=2.77295890.629375793.1519179030-1077111323.1516485126
- type: x-status
  url: https://status.bitbucket.org/?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-support
  url: https://support.atlassian.com/bitbucket-cloud/
- type: x-terms-of-service
  url: https://www.atlassian.com/legal/customer-agreement?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-twitter
  url: https://twitter.com/bitbucket
- type: x-website
  url: http://bitbucket.org
- type: x-website
  url: https://bitbucket.org/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---