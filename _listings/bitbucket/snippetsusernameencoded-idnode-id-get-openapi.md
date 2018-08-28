---
swagger: "2.0"
x-collection-name: Bitbucket
x-complete: 0
info:
  title: Bitbucket Get Snippets Username Encoded  Node
  description: |-
    Identical to `GET /snippets/encoded_id`, except that this endpoint
    can be used to retrieve the contents of the snippet as it was at an
    older revision, while `/snippets/encoded_id` always returns the
    snippet's current revision.

    Note that only the snippet's file contents are versioned, not its
    meta data properties like the title.

    Other than that, the two endpoints are identical in behavior.
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
    get:
      summary: Get Snippets Username Encoded
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
      operationId: getSnippetsUsernameEncoded
      x-api-path-slug: snippetsusernameencoded-id-get
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
    parameters:
      summary: Parameters Snippets Username Encoded
      description: Parameters snippets username encoded
      operationId: parametersSnippetsUsernameEncoded
      x-api-path-slug: snippetsusernameencoded-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
    put:
      summary: Update Snippets Username Encoded
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
      operationId: putSnippetsUsernameEncoded
      x-api-path-slug: snippetsusernameencoded-id-put
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
  /snippets/{username}/{encoded_id}/comments:
    get:
      summary: Get Snippets Username Encoded  Comments
      description: |-
        Used to retrieve a paginated list of all comments for a specific
        snippet.

        This resource works identical to commit and pull request comments.

        The default sorting is oldest to newest and can be overridden with
        the `sort` query parameter.
      operationId: getSnippetsUsernameEncodedComments
      x-api-path-slug: snippetsusernameencoded-idcomments-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
    parameters:
      summary: Parameters Snippets Username Encoded  Comments
      description: Parameters snippets username encoded  comments
      operationId: parametersSnippetsUsernameEncodedComments
      x-api-path-slug: snippetsusernameencoded-idcomments-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
    post:
      summary: Add Snippets Username Encoded  Comments
      description: |-
        Creates a new comment.

        The only required field in the body is `content.raw`.

        To create a threaded reply to an existing comment, include `parent.id`.
      operationId: postSnippetsUsernameEncodedComments
      x-api-path-slug: snippetsusernameencoded-idcomments-post
      parameters:
      - in: body
        name: _body
        description: The contents of the new comment
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
  /snippets/{username}/{encoded_id}/comments/{comment_id}:
    delete:
      summary: Delete Snippets Username Encoded  Comments Comment
      description: |-
        Deletes a snippet comment.

        Comments can only be removed by their author.
      operationId: deleteSnippetsUsernameEncodedCommentsComment
      x-api-path-slug: snippetsusernameencoded-idcommentscomment-id-delete
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
      - Comment
    get:
      summary: Get Snippets Username Encoded  Comments Comment
      description: Get snippets username encoded  comments comment
      operationId: getSnippetsUsernameEncodedCommentsComment
      x-api-path-slug: snippetsusernameencoded-idcommentscomment-id-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
      - Comment
    parameters:
      summary: Parameters Snippets Username Encoded  Comments Comment
      description: Parameters snippets username encoded  comments comment
      operationId: parametersSnippetsUsernameEncodedCommentsComment
      x-api-path-slug: snippetsusernameencoded-idcommentscomment-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
      - Comment
    put:
      summary: Update Snippets Username Encoded  Comments Comment
      description: |-
        Updates a comment.

        Comments can only be updated by their author.
      operationId: putSnippetsUsernameEncodedCommentsComment
      x-api-path-slug: snippetsusernameencoded-idcommentscomment-id-put
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
      - Comment
  /snippets/{username}/{encoded_id}/commits:
    get:
      summary: Get Snippets Username Encoded  Commits
      description: Returns the changes (commits) made on this snippet.
      operationId: getSnippetsUsernameEncodedCommits
      x-api-path-slug: snippetsusernameencoded-idcommits-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
    parameters:
      summary: Parameters Snippets Username Encoded  Commits
      description: Parameters snippets username encoded  commits
      operationId: parametersSnippetsUsernameEncodedCommits
      x-api-path-slug: snippetsusernameencoded-idcommits-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
  /snippets/{username}/{encoded_id}/commits/{revision}:
    get:
      summary: Get Snippets Username Encoded  Commits Revision
      description: Get snippets username encoded  commits revision
      operationId: getSnippetsUsernameEncodedCommitsRevision
      x-api-path-slug: snippetsusernameencoded-idcommitsrevision-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
      - Revision
    parameters:
      summary: Parameters Snippets Username Encoded  Commits Revision
      description: Parameters snippets username encoded  commits revision
      operationId: parametersSnippetsUsernameEncodedCommitsRevision
      x-api-path-slug: snippetsusernameencoded-idcommitsrevision-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
      - Revision
  /snippets/{username}/{encoded_id}/watch:
    delete:
      summary: Delete Snippets Username Encoded  Watch
      description: |-
        Used to stop watching a specific snippet. Returns 204 (No Content)
        to indicate success.
      operationId: deleteSnippetsUsernameEncodedWatch
      x-api-path-slug: snippetsusernameencoded-idwatch-delete
      parameters:
      - in: path
        name: encoded_id
        description: The snippet id
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Watch
    get:
      summary: Get Snippets Username Encoded  Watch
      description: |-
        Used to check if the current user is watching a specific snippet.

        Returns 204 (No Content) if the user is watching the snippet and 404 if
        not.

        Hitting this endpoint anonymously always returns a 404.
      operationId: getSnippetsUsernameEncodedWatch
      x-api-path-slug: snippetsusernameencoded-idwatch-get
      parameters:
      - in: path
        name: encoded_id
        description: The snippet id
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Watch
    parameters:
      summary: Parameters Snippets Username Encoded  Watch
      description: Parameters snippets username encoded  watch
      operationId: parametersSnippetsUsernameEncodedWatch
      x-api-path-slug: snippetsusernameencoded-idwatch-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Watch
    put:
      summary: Update Snippets Username Encoded  Watch
      description: Used to start watching a specific snippet. Returns 204 (No Content).
      operationId: putSnippetsUsernameEncodedWatch
      x-api-path-slug: snippetsusernameencoded-idwatch-put
      parameters:
      - in: path
        name: encoded_id
        description: The snippet id
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Watch
  /snippets/{username}/{encoded_id}/watchers:
    get:
      summary: Get Snippets Username Encoded  Watchers
      description: Returns a paginated list of all users watching a specific snippet.
      operationId: getSnippetsUsernameEncodedWatchers
      x-api-path-slug: snippetsusernameencoded-idwatchers-get
      parameters:
      - in: path
        name: encoded_id
        description: The snippet id
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Watchers
    parameters:
      summary: Parameters Snippets Username Encoded  Watchers
      description: Parameters snippets username encoded  watchers
      operationId: parametersSnippetsUsernameEncodedWatchers
      x-api-path-slug: snippetsusernameencoded-idwatchers-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Watchers
  /snippets/{username}/{encoded_id}/{node_id}:
    delete:
      summary: Delete Snippets Username Encoded  Node
      description: |-
        Deletes the snippet.

        Note that this only works for versioned URLs that point to the latest
        commit of the snippet. Pointing to an older commit results in a 405
        status code.

        To delete a snippet, regardless of whether or not concurrent changes
        are being made to it, use `DELETE /snippets/{encoded_id}` instead.
      operationId: deleteSnippetsUsernameEncodedNode
      x-api-path-slug: snippetsusernameencoded-idnode-id-delete
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
      - ""
      - Node
    get:
      summary: Get Snippets Username Encoded  Node
      description: |-
        Identical to `GET /snippets/encoded_id`, except that this endpoint
        can be used to retrieve the contents of the snippet as it was at an
        older revision, while `/snippets/encoded_id` always returns the
        snippet's current revision.

        Note that only the snippet's file contents are versioned, not its
        meta data properties like the title.

        Other than that, the two endpoints are identical in behavior.
      operationId: getSnippetsUsernameEncodedNode
      x-api-path-slug: snippetsusernameencoded-idnode-id-get
      parameters:
      - in: path
        name: encoded_id
        description: The snippets id
      - in: path
        name: node_id
        description: A commit revision (SHA1)
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Node
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