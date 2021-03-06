swagger: "2.0"
x-collection-name: Intrinio
x-complete: 1
info:
  title: Intrinio
  version: 1.0.0
host: api.intrinio.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /analysts:
    get:
      summary: Analysts
      description: Returns a list of analysts. TipRanks analysts are anonymized, but
        you will be able to reference them with the provided id field.
      operationId: analysts
      x-api-path-slug: analysts-get
      parameters:
      - in: query
        name: page_number
        description: an integer greater than or equal to 1 for specifying the page
          number for the return values
        type: string
      - in: query
        name: page_size
        description: an integer greater than 1 for specifying the number of results
          on each page
        type: string
      - in: query
        name: source
        description: 'The source of the data: tip'
        type: string
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Analysts