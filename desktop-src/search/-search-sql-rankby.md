---
description: Les résultats d’une requête incluent à la fois les lignes retournées par la requête et une valeur de classement pour chaque ligne si la colonne Rank est incluse dans la clause SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANK BY, clause
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201295"
---
# <a name="rank-by-clause"></a>RANK BY, clause

Les résultats d’une requête incluent à la fois les lignes retournées par la requête et une valeur de classement pour chaque ligne si la colonne Rank est incluse dans la clause SELECT. Les valeurs de classement sont calculées par le moteur de recherche et sont retournées sous forme d’entiers dans la plage de zéro à 1000. Pour que les résultats de classement soient plus significatifs, la requête peut contrôler la façon dont les valeurs de classement brutes sont calculées dans la clause RANK BY.

Cette rubrique est organisée comme suit :

-   [RANK BY, clause](#rank-by-clause)
-   [Fonction WEIGHT](#weight-function)
-   [Fonction de contrainte](#coercion-function)

## <a name="rank-by-clause"></a>RANK BY, clause

La syntaxe de la clause RANK BY est la suivante :


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



La clause RANK BY est appliquée à la condition de recherche qui la \_ précède immédiatement, en spécifiant en fait un rang inférieur ou supérieur pour les lignes retournées par cette condition de recherche que les lignes retournées par une autre condition de recherche. Les parenthèses entourant la condition de recherche \_ sont requises. Les parenthèses entourant la spécification de classement sont facultatives.

Plusieurs clauses RANK BY peuvent être appliquées à une seule condition. Vous pouvez inclure des clauses rang BY supplémentaires une après l’autre en utilisant des parenthèses.

> [!Note]  
> Les prédicats de texte intégral retournent des valeurs de classement comprises dans la plage 0 à 1000. Les valeurs de classement de tous les documents correspondant à un prédicat de texte non intégral sont 1000. Les modifications apportées aux valeurs de classement doivent tenir compte de ces informations.

 

La \_ partie spécification de classement de la clause RANKBY identifie une ou plusieurs fonctions à appliquer aux valeurs de classement. La fonction WEIGHT applique un multiplicateur à la valeur de classement brute d’une ligne retournée. Plus le multiplicateur est petit, plus la valeur de classement qui en résulte est faible. La fonction de forçage peut être utilisée pour multiplier, ajouter ou définir une valeur de classement spécifique pour une ligne retournée. Chaque spécification de classement peut inclure zéro ou une fonction de pondération et zéro ou plusieurs fonctions de forçage de type. Si les fonctions de pondération et de contrainte sont incluses dans une clause RANK BY, la fonction WEIGHT doit être la première.

## <a name="weight-function"></a>Fonction WEIGHT

La syntaxe de la fonction WEIGHT est la suivante :


```
WEIGHT ( <weight_multipler> ) 
```



Le multiplicateur doit être un nombre décimal compris entre 0,001 et 1,000. La valeur de classement brute retournée par le prédicat de condition de recherche est multipliée par le multiplicateur de pondération pour définir une nouvelle valeur de classement.

Dans l’exemple suivant, la fonction WEIGHT donne des documents avec le mot « Theresa » dans le ument System.Doc. Champ LastAuthor de la moitié de la valeur de classement des documents avec « Theresa » dans le champ System. Author :


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> Les fonctionnalités de pondération de colonne de prédicat CONTAINs et FREETEXT prennent en charge un format abrégé à l’aide d’un signe deux-points entre le terme de recherche et le multiplicateur (« Software » : 0.25). La clause RANK BY ne prend pas en charge la forme abrégée.

 

Il existe une limitation lors de l’utilisation du classement par poids : il ne fonctionne pas avec les clauses CONTAINs qui utilisent des conditions booléennes ; par exemple, l’exemple suivant n’est pas autorisé :


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a>Fonction de contrainte

La fonction de forçage de rang peut être utilisée pour modifier la valeur de classement retournée par addition ou multiplication ou en lui assignant une valeur spécifique.

La syntaxe de la fonction de forçage est la suivante :


```
COERCION ( <coercion_operation> , <coercion_value> )
```



La valeur de forçage de type est une valeur entière.

Le tableau suivant décrit les paramètres d’opération de forçage disponibles.



| Opération de contrainte | Description                                                                                    | Plage de valeurs  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| ABSOLUTE           | La valeur de classement retournée est la valeur spécifiée dans la valeur de forçage de la valeur.                          | 0 à 1000    |
| ADD                | La valeur de classement retournée est la somme de la valeur de classement brute et de la valeur de forçage spécifiée.     | 0,001 à 1,0 |
| MULTIPLY           | La valeur de classement retournée est le produit de la valeur de classement brute et la valeur de forçage spécifiée. | 0,001 à 1,0 |



 

 

> [!IMPORTANT]
> La recherche peut retourner des valeurs de classement uniquement dans la plage comprise entre 0 et 1000.

 

 

L’exemple suivant utilise la fonction de forçage pour définir tous les documents dont le titre contient « Computer » pour avoir un rang de 1000, tout en réduisant d’un quart le rang des documents contenant à la fois « Computer » et « Software » dans le titre.


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



