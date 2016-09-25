# Assignment 2: Ontology Development with Protégé

#### Remko Boschker s1282603

## Description

This ontology models the domain of the seasoning of food. It contains cuisines, spices, herbs and mixtures. Because the model starts to grow very large very fast I have limited the ontology (for now) to the spicy mixtures found on [cooksmarts.com](http://www.cooksmarts.com/articles/ultimate-infographic-guide-spices/). Some of the classification is taken from chapter one in Handbook of Herbs and Spices edited by K.V. Peter, Woodhead Publishing 2001.

## Model

Because this ontology uses a lot of natural kinds (names of spices for instance), it becomes less clear what is an individual. In the case of a student with a particular number this seems pretty straight-forward. However with for instance _Cinnamon_ I am not talking about a particular stick of cinnamon in my hand or a batch of cinnamon with a particular number in the belly of some cargo ship. For all intents and purposes of this ontology the names of a particular plant, herb or spice is taken to instantiate the class it belongs to.

You can speak of a cuisine from a certain place, culture or religion. Cuisines from a particular place have a similar issue as the natural kinds in that they are grouped in ever larger regional areas. For instance the cuisine of let's say Rome is also a cuisine of Italy, South Europe and Europe. At each level there can be properties that apply.

I have stopped the classification a the level of countries and each cuisine from a particular country is an individual. For a few larger regions (Latin America, the Mediterranean and the Middle East) I have included a individual as well as a class [a method called punning](https://www.w3.org/2007/OWL/wiki/Punning). I did this to allow for the region to group cuisines and at the same time be the subject of a property. Although the Cajun cuisine is commonly classified as an American cuisine. It is in fact the cuisine of an ethnic group. The countries and ethnic groups that the cuisines relate to are taken from [dbpedia.org](https://dbpedia.org).

### Class Hierarchy

![image of class hierarchy](classHierarchy.png)

### Properties

| name | type | inverse | domain | range |
| :-- | :-- | :-- | :-- | :-- |
| uses | object | isUsedIn | Cuisine | Food |
| cuisineIsFromPlace | object | placeHasCuisine | Cuisine | dbo:PopulatedPlace |
| cuisineIsFromEthnicGroup | object | ethnicGroupHasCuisine | Cuisine | dbo:EthnicGroup |
| contains | object | isContainedIn | Mixture | Food |
| hasBotanicalName | data | - | PlantPart | xsd:String |

The dbo prefix stands for http://dbpedia.org/ontology/

| name | example |
| :-- |  :-- |
| uses | ThaiCuisine uses Basil |
| cuisineIsFromPlace |  ThaiCuisine cuisineIsFromPlace Thailand |
| cuisineIsFromEthnicGroup | CajunCuisine cuisineIsFromEthnicGroup Cajun |
| contains | CurryPowder contains Fenugreek |
| hasBotanicalName | Allspice hasBotanicalName "Pimenta dioica" |

### Example Individuals

| (super)type | examples |
| :-- | :-- |
| cuisine | ThaiCuisine, NorthAfricanCuisine, ItalianCuisine |
| Mixture | Soffrito, RasElHanout, HerbesDeProvance |
| Herb | Marjoram, Basil, Oregano |
| Spice | Nutmeg, Fenugreek, Cinnamon |
| AromaticVegetable | Carrot, Celery, Onion |
| Fat | Butter, Ghee, OliveOil |

## Queries

The queries are excuted with the following prefix.

````
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX owl: <http://www.w3.org/2002/07/owl#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX : <http://www.semanticweb.org/remkoboschker/ontologies/spice#>
````

### 1. Simple

List all foods used in the Thai cuisine.

````
SELECT ?food
WHERE {
  :ThaiCuisine :uses ?food
}
````

| food |
| :-- |
| GreenCardamom	|
| CoconutMilk	|
| Cumin	|
| ChilliPepper	|
| KaffirLime	|
| Lemongrass	|
| Cilantro	|
| Shallot	|
| Garlic	|
| CurryPowder	|
| Basil	|
| Galangal	|
| PeanutOil	|
| Turmeric	|
| Ginger|

### 2. Complex

List all foods used in both the Thai and the Indian cuisine.

````
SELECT ?food
WHERE {
  :ThaiCuisine :uses ?food .
  :IndianCuisine :uses ?food .
}
````

| food |
| :-- |
| GreenCardamom	|
| Cumin	|
| CurryPowder	|
| Turmeric	|
| Ginger|

### 3. Restrict to type

List all food used in the Thai cuisine whose type is Fats.

````
SELECT ?food
WHERE {
  :ThaiCuisine :uses ?food .
  ?food rdf:type :Fats .
}
````

| food |
| :-- |
| CoconutMilk |
| PeanutOil |

### 4. Restrict type to subclass of a type

List all food used in the Thai cuisine whose type is a direct subclass of the class Spice.

````
SELECT ?food ?type
WHERE {
  :ThaiCuisine :uses ?food .
  ?food rdf:type ?type .
  ?type rdfs:subClassOf :Spice
}
````

| food | type |
| :-- | :--- |
| Turmeric	| MildSpice |
| GreenCardamom	| AromaticSpice |
| Cumin	| AromaticSpice |		
| Lemongrass	| AromaticSpice |
| ChilliPepper	| HotSpice |
| Galangal	| HotSpice |		
| Ginger	| HotSpice |

### 5. Using feature of SPARQL 1.1

Using SPARQL 1.1 property paths to list all food used by the Thai cuisine with a type that is a (transitive) subclass of the class Seasoning.

````
SELECT ?food ?type
WHERE {
  :ThaiCuisine :uses ?food .
  ?food rdf:type ?type .
  ?type rdfs:subClassOf* :Seasoning
}
````

| food | type |
| :-- | :--- |
| GreenCardamom	|AromaticSpice	|
| Cumin	|AromaticSpice	|
| ChilliPepper	|HotSpice	|
| KaffirLime	|Herb	|
| Lemongrass	|AromaticSpice	|
| Cilantro	|Herb	|
| Shallot	|AromaticVegetable	|
| Garlic	|AromaticVegetable	|
| CurryPowder	|Mixture	|
| Basil	|Herb	|
| Galangal	|HotSpice	|
| Turmeric	|MildSpice	|
| Ginger	|HotSpice|
