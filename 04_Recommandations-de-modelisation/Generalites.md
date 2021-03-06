# Généralités

L’ensemble des informations décrites ci-dessous devront être présentes dans les modèles déposés au format IFC.

La description comprend les informations au format IFC, ainsi qu’un exemple décrivant comment obtenir ces informations dans le logiciel Revit.

Si vous utilisez un logiciel différent, les informations demandées doivent apparaitre dans le modèle IFC déposé sur la plateforme d’échange.

## Découpage

Chaque intervenant produira à minima un modèle par bâtiment.

Chaque intervenant est ensuite libre de découper son modèle en plusieurs disciplines en fonction de ses contraintes de modélisations. Par exemple, un modèle Fluides peut ainsi être séparé en 3 modèles distincts, Climatisation, Plomberie et Electricité. De la même manière, un modèle Architecte peut être séparé en 2 modèles, Façades et Intérieur\). L'intervenant demandera alors au BIM Manager la création des modèles correspondants sur la plateforme d’échange.

## Niveaux

Les modèles déposés contiennent un et un seul niveau \(IfcBuildingStorey\) par étage du projet, afin de permettre le regroupement des éléments du modèle par étage du projet.

Tous les éléments du projet devront être modélisés au bon niveau. A l'exception des verticalités des réseaux, tous les composants seront découpés par niveau \(donc pas de voiles multi-tétages\)

On ne modélisera donc pas de niveaux supplémentaires \(niveau brut béton, paliers intermédiaires, …\), mais on utilisera, en fonction de son logiciel de modélisation, décalages par rapport aux niveaux ou plans de référence. Néanmoins, pour faciliter la modélisation des éléments structurels, il reste possible de ne dessiner que les niveaux bruts en lieu et place des niveaux finis.

Les niveaux sont préfixés à l'aide du schéma suivant : SS2, SS1, 00, 01, 02, 03, …, TT.

## Valeurs possibles

Lorsqu’une propriété doit contenir une valeur parmi plusieurs proposées, il est impératif de saisir précisément l’une des valeurs indiquées. Les valeurs autres que celle proposées seront refusées, et l’intervenant devra déposer un nouveau modèle.

