---
swagger: "2.0"
x-collection-name: Google Play
x-complete: 0
info:
  title: Google Play Get Review
  version: 1.0.0
  description: Returns a single review.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{packageName}/reviews:
    get:
      summary: Get Reviews
      description: Returns a list of reviews. Only reviews from last week will be
        returned.
      operationId: androidpublisher.reviews.list
      x-api-path-slug: packagenamereviews-get
      parameters:
      - in: query
        name: maxResults
      - in: path
        name: packageName
        description: Unique identifier for the Android app for which we want reviews;
          for example, com
      - in: query
        name: startIndex
      - in: query
        name: token
      - in: query
        name: translationLanguage
      responses:
        200:
          description: OK
      tags:
      - Reviews
  /{packageName}/reviews/{reviewId}:
    get:
      summary: Get Review
      description: Returns a single review.
      operationId: androidpublisher.reviews.get
      x-api-path-slug: packagenamereviewsreviewid-get
      parameters:
      - in: path
        name: packageName
        description: Unique identifier for the Android app for which we want reviews;
          for example, com
      - in: path
        name: reviewId
      - in: query
        name: translationLanguage
      responses:
        200:
          description: OK
      tags:
      - Reviews
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