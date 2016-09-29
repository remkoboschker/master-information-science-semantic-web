# Assignment 3: OWL ontologies with Protégé

#### Remko Boschker s1282603

## Modifications of the spice ontology from assignment 2

* I redefined ``Herb`` as an intersection between ``Seasoning`` and ``Leaf`` and made all the herbs an instance of seasoning.

````
Herb EquivalentTo Leaf and Seasoning
````

* I added unions to the ``PlantPart``, ``Cuisine`` and ``EdibleSeed`` classes consisting of all their subclasses

````
Cuisine EquivalentTo CulturalCuisine or EthnicCuisine or RegionalCuisine or ReligiousCuisine or StyleOfCuisine
````

````
PlantPart EquivalentTo Aril or Bark or Berry or Bud or Bulb or Kernel or Leaf or Pericarp or Pistil or Rhizome or Root or Seed
````

````
EdibleSeed EquivalentTo Cereal or Legume or Nut or Pseudocereal
````

* I added a class of food called ``FlavorBase`` consisting of mixtures containing aromatic vegetables and Fat

````
Mixture and (contains some Fat) and (contains some AromaticVegetable)
````

* I added a symmetric relation between foods ``goesWellWith``

````
:goesWellWith a owl:ObjectProperty , owl:SymmetricProperty ;
	rdfs:domain :Food ;
	rdfs:range :Food .

:Coriander a owl:NamedIndividual , :MildSpice , :Seed ;
	:goesWellWith :Cumin ;
	:hasBotanicalName "Coriandrum sativum" ;
	rdfs:label "Coriander" .
````

## Inference

1. All individuals that belong to ``Seasoning`` and ``Leaf`` are inferred to be ``Herb``, because ``Herb EquivalentTo Leaf and Seasoning`` for example ``Sage`` or ``Basil``.

2. ``Mirepoix``, ``Soffrito`` and ``LatinSoffrito`` are inferred to be in the class ``Flavorbase`` defined as ``FlavorBase EquivalentTo Mixture and (contains some Fat) and (contains some AromaticVegetable)``.

3. Given ``:RasElHanout :contains :Turmeric`` and ``:contains owl:inverseOf :isContainedIn`` it is inferred that ``:Turmeric :isContainedIn :RasElHanout``.

4. Given the symmetric property ``goesWellWith`` and the statement ``:Coriander :goesWellWith :Cumin`` the reasoner added the statement ``:Cumin :goesWellWith :Coriander`` to the ontology.
