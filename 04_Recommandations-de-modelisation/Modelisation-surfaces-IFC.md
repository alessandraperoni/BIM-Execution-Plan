# Propriétés des surfaces dans les IFC extraits

L'article suivant présente les recommandations à respecter pour les IFC extraits depuis les modèles architecturales en matière de surfaces.

## Surface Hors Œuvre Brut \(SHOB\) et Surface de Plancher \(SDP\)

### Généralités

Les Surface Hors Œuvre Brut \(SHOB\), Surface Hors Œuvre Nette \(SHON\) et Surface de Plancher \(SDP\) sont calculées en additionnant les différents types de surfaces du projet. De plus, la représentation des surfaces de parkings extérieurs est attendue.

### Décomposition des surfaces

Les surfaces du projet sont décomposées suivant ces valeurs:

| Nom | Description |
| :--- | :--- |
| Façade | Surface correspondante à l’emprise horizontale de la façade \(la SDP est calculée au nu intérieur de la façade\) |
| Gaine Ascenseur Et Escaliers | Surfaces des vides et trémies qui se rattachent aux escaliers et ascenseurs |
| Gaine Technique | Surfaces des vides et trémies qui se rattachent aux gaines techniques |
| 180 | Surfaces d'une hauteur sous plafond inférieure ou égale à 1,80 mètre |
| Parking | Surfaces aménagées en vue du stationnement des véhicules motorisés, hors rampes d'accès et aires de manœuvres |
| Parking Vélo | Surfaces aménagées en vue du stationnement des vélo |
| Circulation | Surfaces des circulations des véhicules et aires de manœuvres |
| Rampe | Surfaces des rampes d’accès des véhicules au parking |
| Allée | Surfaces des allées piétonnes autour du bâtiment |
| Voirie | Surfaces de voirie |
| Espace vert | Surfaces de pelouses, allées, zones plantées, … |
| Local technique | Surfaces des locaux techniques nécessaires au fonctionnement d'un groupe de bâtiments ou d'un immeuble autre qu'une maison individuelle, y compris les locaux de stockage des déchets |
| Cave | Surfaces des caves ou des celliers, annexes des logements, dès lors que ces locaux sont desservis uniquement par une partie commune |
| Palier | Surface des paliers en infrastructure |
| Livraison | Surfaces des aires de livraisons couvertes et fermées |
| Terrasse | Surfaces des balcons, terrasses, loggia, … |
| SDP | Surfaces restantes |

### Paramètres des IFC

L’ensemble des surfaces SHOB/SHON/SDP est représenté à l’aide d’IfcSpaces ayant les propriétés suivantes :

| PropertySet | Property | Valeurs possibles | Explication |
| :--- | :--- | :--- | :--- |
| Pset\_SpaceCommon | Category | Areas | Cette propriété permet d’identifier les surfaces nécessaires au calcul de la SHOB. |
| Pset\_SpaceCommon | Reference | Superstructure, Infrastructure, Extérieur | Cette propriété permet d’identifier l’emplacement de ces surfaces. \(Voir II.3 Valeurs possibles\) |
| QuantitySets |  |  |  |
| BaseQuantities | GrossFloorArea | M² | Cette propriété indique l’aire de la surface. |
| Propriétés standards IFC |  |  |  |
|  | LongName | Façade, Gaine Ascenseur Et Escaliers, Gaine Technique, 180, Parking, Parking Vélo, Circulation, Rampe, Allée, Voirie, Espace vert, Local technique, Cave, Palier, Livraison, Terrasse, SDP | Cette propriété indique le type de surface, suivant la décomposition décrite ci-dessus. \(Voir II.3 Valeurs possibles\) |



## Surface Utile Brute Locative \(SUBL\), Surface Utile Brute Bureaux \(SUBB\), Surface Utile Nette \(SUN\) et Surface Nette Bureaux \(SNB\)

### Généralités

Les Surfaces Utiles Brutes Locatives \(SUBL\), Surfaces Utiles Brutes Bureaux \(SUBB\), Surfaces Utiles Nettes \(SUN\) et Surfaces Nettes Bureaux \(SNB\) sont calculées à partir de la modélisation des locaux du projet.

L’ensemble des locaux du projet doivent être présents dans la maquette numérique. En plus des locaux « nobles » du programme, cette modélisation doit inclure tous les autres types de locaux, tel que les circulations, les locaux techniques, les gaines techniques, …

Les locaux doivent être représentés et décomposés en locaux fonctionnels \(Bureau, Salle de Réunion, Hall, …\), même si ces locaux appartiennent à un espace physique plus important. Par exemple, un hall et une cafétéria partageant le même espace physique devront être représentés comme deux locaux distincts.

Les locaux doivent être modélisés depuis le sol fini jusqu’au plafond fini. En l’absence de faux-plafonds, les locaux doivent être modélisés jusqu’à la hauteur libre prévue par le programme. Les locaux doivent être identifiés par leur nom, en suivant les valeurs du tableau Décomposition des locaux.

### Décompositions des locaux

| **Eléments de construction** |  |
| :--- | :--- |
|  | TERRASSES |
|  | GAINES ASCENSEURS ET ESCALIERS |
|  | GAINES TECHNIQUES |
| **Partie Communes Nobles** |  |
|  | HALL |
|  | SALLE DE RESTAURANT ET DISTRIBUTION |
|  | CUISINES |
|  | CAFETERIA |
|  | SANITAIRES SGX |
|  | AUDITORIUM / SALLE POLYVALENTE |
|  | FITNESS |
|  | PALIERS D'ETAGES |
|  | PALIERS D'ESCALIERS |
|  | CIRCULATIONS COMMUNES |
| Parties Privatives |  |
|  | LOCAUX ET ARMOIRES TECHNIQUES UTILISATEURS |
|  | CIRCULATIONS DE BUREAUX |
|  | SANITAIRES PRIVATIFS |
|  | LOCAUX MENAGES D'ETAGES |
|  | TISANERIES |
|  | LOCAUX BRASSAGE |
|  | SALLES DE REUNIONS |
|  | ZONES DE SURCHARGES RENFORCEES |
|  | SURFACES BUREAUX |
| **Back of house** |  |
|  | ARCHIVES CENTRALES |
|  | LOCAUX DIVERS COMMUNS |
|  | LOCAUX VESTIAIRES VELO |
|  | LOCAUX DECHETS |
|  | LOCAUX TECHNIQUES |
| **Stationnement** |  |
|  | PARKING VOITURES ET DEUX MOTORISES |
|  | LOCAUX VELO PARKING |
|  | PALIERS INFRA |
|  | AIRES DE LIVRAISONS COUVERTES ET FERMEES |



### Représentation en IFC

L’ensemble des locaux sont représentées à l’aide d’IfcSpaces, du niveau finit au plafond finit, avec les propriétés suivantes :

| PropertySet | Property | Valeurs possibles | Explication |
| :--- | :--- | :--- | :--- |
| Pset\_SpaceCommon | Category | Room | Cette propriété permet d’identifier les d’IfcSpaces nécessaires au calcul des SUBL, SUBB, SUN et SNB. |
| QuantitySets |  |  |  |
| BaseQuantities | GrossFloorArea | M² | Cette propriété indique l’aire du local. |
| Propriétés standards IFC |  |  |  |
|  | LongName | Voir «Décompositions des locaux» | Cette propriété indique le type de local, suivant la décomposition décrite ci-dessus. \(Voir II.3 Valeurs possibles\) |



