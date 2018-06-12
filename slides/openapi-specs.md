## OpenAPI<!-- .element: class="open-api-color" -->

#### Spécifications : Les différences

-##-

#### Spécifications : Les différences

![](images/swagger2-vs-OpenApi3.png)<!-- .element: style="border: none; box-shadow: none; background-color: rgba(0,0,0,0);" -->

-##-

## OpenAPI<!-- .element: class="open-api-color" -->

#### Spécification : Format

* JSON
* YAML

-##-

## OpenAPI<!-- .element: class="open-api-color" -->

#### Spécification : Format JSON

```json
...
"/user/":{
    "get":{
    "tags":[
        "user"
    ],
    "summary":"get user informations",
    "description":"",
    "operationId":"getUser",
    "produces":[
        "application/xml",
        "application/json"
    ],
...
```
*Swagger 2 & OpenAPI 3*<!-- .element: class=" highlight2" -->

-##-

## OpenAPI<!-- .element: class="open-api-color" -->

#### Spécification : Format YAML

```yaml
...
  /user/:
    get:
      tags:
      - "user"
      summary: "get user informations"
      description: ""
      operationId: "getUser"
      produces:
      - "application/xml"
      - "application/json"
...
```

*Mais seulement a partir de OpenAPI 3*<!-- .element: class="fragment highlight2" -->
