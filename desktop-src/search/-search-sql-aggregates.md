---
description: Une fonction d’agrégation effectue un calcul sur un ensemble de valeurs et retourne une valeur. Cela permet de générer des statistiques de synthèse pour les groupes à plusieurs niveaux avec une faible surcharge.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Fonctions d’agrégation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d504a9343116bc23e847728716eeaa79fc2d26d993e962dd81ccd43669e22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094953"
---
# <a name="aggregate-functions"></a>Fonctions d’agrégation

Une fonction d’agrégation effectue un calcul sur un ensemble de valeurs et retourne une valeur. Cela permet de générer des statistiques de synthèse pour les groupes à plusieurs niveaux avec une faible surcharge.

## <a name="about-aggregate-functions"></a>À propos des fonctions d’agrégation

les fonctions d’agrégation dans Windows langage SQL de recherche (SQL) ont la syntaxe suivante :


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



La partie fonction peut inclure l’une des fonctions et la syntaxe suivantes :



| Fonction                                                              | Description                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Moy ( <column> )                                                   | Renvoie la moyenne des valeurs d'un groupe. S’applique uniquement aux nombres.                                                                                                                                      |
| BYFREQUENCY ( <column> , <N> )                                | Retourne les N valeurs de colonne les plus fréquentes des résultats dans le groupe. Comprend également le nombre de fois où chaque valeur s’est produite et les identificateurs de document pour les résultats qui contiennent chaque valeur retournée. |
| CHILDCOUNT ()                                                          | Retourne le nombre d’éléments d’un groupe (à l’exception des sous-groupes). S’il existe plusieurs niveaux de regroupement, retourne le nombre de groupes enfants immédiats.                                                  |
| COUNT ()                                                               | Retourne le nombre d’éléments dans un groupe et tous les sous-groupes.                                                                                                                                                   |
| DATERANGE ( <column> )                                             | Retourne les limites inférieure et supérieure des valeurs de colonne trouvées dans le groupe de résultats de groupe. Valide uniquement pour les propriétés FILETIME.                                                                               |
| PREMIER ( <column> , <N> )                                      | Retourne les N premières valeurs de colonne des résultats feuille trouvés dans un groupe.                                                                                                                                       |
| MAX ( <column> )                                                   | Retourne la valeur maximale de l'expression. S’applique uniquement aux nombres ou aux dates.                                                                                                                              |
| MIN ( <column> )                                                   | Retourne la valeur minimale de l'expression. S’applique uniquement aux nombres ou aux dates.                                                                                                                              |
| REPRESENTATIVEOF ( <column> , <idRepresentative> , <N> ) | Retourne N valeurs idRepresentative, chacune sélectionnée à partir de l’un des sous-ensembles de résultats qui a une valeur de colonne unique. Chaque valeur est également retournée avec un identificateur de document qui a la valeur idRepresentative. |
| SUM ( <column> )                                                   | Retourne la somme des valeurs d’un groupe. S’applique uniquement aux nombres.                                                                                                                                          |



 

 

> [!Note]  
> Les agrégats sont retournés en tant que colonnes individuelles. Il s’agit essentiellement de types simples, à l’exception de ByFrequency, First, DateRange et RepresentativeOf, qui sont retournés en tant que types composés.

 

Vous pouvez utiliser n’importe quelle colonne numérique ou de date pour les agrégations, et pas seulement celles qui se trouvent dans la clause SELECT. Toutefois, vous ne pouvez pas regrouper sur des agrégats. Une erreur de syntaxe est retournée si l’argument de colonne passé n’est pas un type numérique ou de date.

La partie étiquette est facultative et fournit un alias plus lisible pour l’étiquette. si vous n’incluez pas d’étiquette d’alias, Windows recherche transforme la fonction et le nom de colonne en étiquette. Par exemple, MAX (System.Document. WordCount) devient MAX \_ SystemDocumentWordCount.

## <a name="multi-level-groups-and-counting"></a>Groupes et décomptes à plusieurs niveaux

Les agrégats sont définis à travers les feuilles et sont dupliqués. Un agrégat prend comme entrée les feuilles du groupe qui le définit (documents), plutôt que les sous-groupes de ses enfants. Cette fonctionnalité est appelée regroupement à plusieurs niveaux.

En plus des agrégats définis sur les feuilles et dupliqués, ils ne sont comptés qu’une seule fois. Même si le même document peut être représenté plusieurs fois dans un groupe, les agrégats ne le considèrent qu’une seule fois. Le graphique suivant illustre ce concept.

![Diagramme montrant que les agrégats sont définis au-dessus des feuilles et dupliqués, et ne sont comptés qu’une seule fois](images/aggregates.png)

## <a name="aggregate-examples"></a>Exemples d’agrégats

Voici des exemples de fonctions d’agrégation dans la clause GROUP ON :


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a>Valeur renvoyée

La valeur de retour est une variante trouvée sur l’ensemble de lignes en tant que propriété personnalisée, en tant qu’alias spécifié ou en tant qu’agrégats si aucune étiquette d’alias n’est spécifiée.

 

 



