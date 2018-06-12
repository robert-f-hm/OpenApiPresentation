## Swagger<!-- .element: class="open-api-color" -->

#### Implementation d'OpenAPI<!-- .element: style="text-transform: none; " -->

-##-

## Swagger<!-- .element: class="open-api-color" -->

Une serie d'outillage

De la génération à la visualisation ...

... et aux tests

-#-

## Swagger<!-- .element: class="open-api-color" -->

*Mais avant de parler outillage*

***Parlons méthodologie***

-##-

## Swagger<!-- .element: class="open-api-color" -->

#### Génération du fichier

Deux principes : 

* Bottom-top
* Top-bottom

-##-

## Swagger<!-- .element: class="open-api-color" -->

#### Génération du fichier : *Bottom-Top*<!-- .element: style="text-transform: none;" -->

Écriture des spécification de l'API REST d'abord pour ensuite générer le code.

***Specification as code***<!-- .element: class="highlight2" -->

-##-

#### Génération du fichier : *Bottom-Top*<!-- .element: style="text-transform: none;" -->

Pour cela, il existe **Swagger editor**

![](images/swagger-editor-01.jpg)<!-- .element: class="image-simple" -->

-##-

## Swagger<!-- .element: class="open-api-color" -->

#### Génération du fichier : *Bottom-Top*<!-- .element: style="text-transform: none;" -->

#### Swagger Editor<!-- .element: style="text-transform: none;" -->

Permet l'écriture des spécifications (au format YAML ou JSON) et de générer le code source correspondant (serveur & client, langages & framework)

[https://editor.swagger.io/](https://editor.swagger.io/)    

-##-

#### Génération du fichier : *Bottom-Top*<!-- .element: style="text-transform: none;" -->

![](images/swagger-editor-02.jpg)<!-- .element: class="image-simple" -->

-##-

## Swagger<!-- .element: class="open-api-color" -->

#### Génération du fichier : *Top-Bottom*<!-- .element: style="text-transform: none;" -->

***Code as specification***<!-- .element: class="highlight2" -->

Différents tools existe (pour différent langages & framework) qui permette d'interpreter une API REST exposer et d'en générer le fichier OpenAPI (ou swagger selon la version).

-##-

## Swagger<!-- .element: class="open-api-color" -->

#### Génération du fichier : *Top-Bottom*<!-- .element: style="text-transform: none;" -->

```java
@RequestMapping(value = ..., produces = {APPLICATION_JSON_VALUE})
@Api(value = "Utilisateurs", description = "Gestion des utilisateurs")
public class UserEndpoint extends ... {
...
  @ApiOperation(
      value = "Liste des utilisateurs", 
      notes = "Renvoi la liste des utilisateurs", code = 206,
      response = User.class, responseContainer = "List"
  )
  @ApiResponses({
      @ApiResponse(code = 200, message = "La liste contient tous les éléments possible"),
      @ApiResponse(code = 206, message = "La liste contient les éléments de la page courante"),
      @ApiResponse(code = 204, message = "La liste ne contient aucun éléments")
  })
  @GetMapping(produces = {APPLICATION_JSON_VALUE})
  public ResponseEntity<List<UserDTO>> getUserList(
    ...
```

-##-

|  Specification as code | Code as specification  |
|---|---|
| **Pro**  | **Pro**  |
| Facile a initier | Au plus proche du code  |
| **Cons**  | **Cons**  |
| Désynchronisation  | Adhérence au code  |
